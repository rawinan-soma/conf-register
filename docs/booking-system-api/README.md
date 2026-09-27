# Booking-system API: proposal for the booking-system team

**Status:** Proposal, v0.1 (2026-09-27)
**From:** Conference Registration service (`conf-register`)
**To:** Booking-system dev team
**Machine-readable spec:** [`openapi.yaml`](./openapi.yaml)

## Why we need this

We're building a conference registration service that runs alongside the room-booking system. When a staff member has booked rooms for a meeting, they can open online registration for it. From then on we handle the registration form, QR check-in, the sign-in sheet, lunch counts and reminder emails.

We don't store rooms or bookings ourselves. We read them from you. For that we need a small **read-only** API.

The API has two jobs:

1. **Open registration.** A logged-in staff member sees their upcoming bookings and picks the ones that make up their meeting.
2. **Follow changes.** We re-check those bookings every 15 minutes. If one moves, changes room or is cancelled, we email the people who registered.

That's the whole API: three read endpoints, and one of them is optional. We never write to the booking system.

## What we ask for, in short

| # | Endpoint | Required? | Used for |
|---|---|---|---|
| 1 | `GET /bookings/{id}` | Required | Following changes to one booking |
| 2 | `GET /bookings?booked_by=…&from=…` | Required | Showing a staff member their upcoming bookings |
| 3 | `GET /bookings?ids=…` | Optional | Following changes to many bookings in one call |

If you build only endpoint 1, we poll each booking one by one, which is slower but works. Endpoint 3 is a performance nicety.

## Authentication

- **Service-to-service.** Please issue us **one read-only credential** for our background jobs. The job runs every 15 minutes whether or not anyone is logged in. Use whatever you already support, such as an API key or OAuth 2.0 client credentials. We send it as `Authorization: Bearer <token>`.
- The credential must be able to **read any booking**. We check on our side that each staff member sees only their own bookings.
- **HTTPS only.** If you can, restrict the credential to our service's network or IP.
- **Human login is separate.** Staff log in to our service with the booking system's own login. That is covered in a separate conversation about staff identity, and nothing in this document depends on it except the shape of `booked_by` (see below).

## The Booking object

```json
{
  "id": "BK-2026-004512",
  "title": "ประชุมคณะกรรมการ ครั้งที่ 3/2569",
  "status": "active",
  "start": "2026-10-14T09:00:00+07:00",
  "end": "2026-10-14T12:00:00+07:00",
  "room": {
    "id": "R-301",
    "name": "ห้องประชุม 301",
    "location": "อาคาร 3 ชั้น 3"
  },
  "booked_by": "staff-00123"
}
```

| Field | Type | Rules |
|---|---|---|
| `id` | string | **Stable and never reused.** The same booking keeps the same id for its whole life, including after cancellation. |
| `title` | string, may be empty | Whatever the booker typed as the purpose or name. |
| `status` | `"active"` \| `"cancelled"` | See [Cancellations](#cancellations). |
| `start`, `end` | string, ISO 8601 date-time **with offset** | For example `+07:00`. `end` is after `start`. |
| `room.id` | string | Stable id of the room. |
| `room.name` | string | Display name that registrants can recognize. |
| `room.location` | string | Building and floor, or directions, so outside guests can find the room. |
| `booked_by` | string | The staff member who made the booking. **Shape TBD**: it must be the same identifier we get when that person logs in, so we can match them. We'll confirm this with you in the staff-identity conversation. |

If you have other fields, feel free to return them; we ignore them.

## Endpoints

### 1. Get one booking: `GET /bookings/{id}` (required)

- `200`: the Booking object. **This includes cancelled bookings** (`status: "cancelled"`).
- `404`: the id has never existed. We treat a 404 on a booking we already know about as an anomaly and show it to the organizer. We **don't** email registrants on a 404, so please don't use 404 to mean "cancelled".

### 2. List a person's upcoming bookings: `GET /bookings?booked_by={staff_id}&from={datetime}` (required)

- Returns bookings made by `booked_by` that are **active** and have `start ≥ from`.
- `from` is optional and defaults to now.
- Cancelled bookings are **not** included.
- Sort by `start`, ascending.
- Response: `{ "items": [Booking, …] }`. If a person can have more than about 200 upcoming bookings, add cursor pagination (`next_cursor`). Otherwise it isn't needed.

### 3. Get many bookings by id: `GET /bookings?ids={id},{id},…` (optional)

- Up to 100 ids per call.
- Response: `{ "items": [Booking, …], "not_found": ["id", …] }`.
- As with endpoint 1, this includes cancelled bookings.

### Errors

All errors use this shape:

```json
{ "error": { "code": "not_found", "message": "Booking BK-2026-004512 not found" } }
```

| Status | When |
|---|---|
| `400` | Bad parameter (for example, an unparseable `from`) |
| `401` | Missing or invalid credential |
| `403` | Credential valid but not allowed |
| `404` | Booking id never existed (endpoint 1 only) |
| `429` | Rate-limited. Please send `Retry-After`. |
| `5xx` | Your side is down. We retry on the next cycle. |

## Cancellations

This is the one rule we need you to hold to strictly:

> **A cancelled booking stays readable by id, with `status: "cancelled"`, for at least 30 days after its original `end`.**

We email registrants when their meeting is cancelled. If cancelled bookings just disappeared, we couldn't tell a real cancellation from a deleted record, a permissions glitch or a changed id. We'd either send wrong "cancelled" emails or send none at all.

If your system doesn't allow a booking to be reassigned to a different staff member, great. If it does, that's fine too: just update `booked_by`. We'll notice the change and flag it on our side.

## How we'll call you (expected load)

- **Polling:** every 15 minutes we fetch only the bookings that belong to meetings with registration open, and only until each meeting's last booking has ended. We expect roughly tens of bookings at any one time. We use endpoint 3 if it exists and endpoint 1 otherwise.
- **Listing:** endpoint 2 is called when a staff member opens our "start registration" screen, which is a few times a day.
- If your API is down, we retry quietly. After 2 hours of failures we show organizers a "last synced at…" warning. You don't need to do anything on your side.

## What we compare, so you know what matters

We store each booking and compare it with the next fetch:

| Field changes | What we do |
|---|---|
| `start`, `end`, `room.id`, `status` | A **booking change**: we notify registrants |
| `booked_by` | We flag it to the meeting's organizers only |
| `title`, `room.name`, `room.location` | Ignored for notifications (we still show the latest room name and location) |

## Open questions for you

1. What exactly is `booked_by`, and is it the same identifier your login gives us? This is pending the staff-identity conversation.
2. Can you keep cancelled bookings readable for 30 days after `end`? If your retention is shorter, tell us the number.
3. Which service-credential mechanism do you prefer?
4. Is endpoint 3 (batch) cheap for you to add? If not, skip it.
5. Base URL and environments (test and production)?
