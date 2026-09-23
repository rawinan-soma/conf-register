# Conference Registration

Registration, check-in and attendee logistics for meetings held in the org's rooms. It sits beside the org's room-booking system and draws its room and time data from there.

## Language

### Meetings and rooms

**Booking**:
A reservation of one room for one time slot, owned by the room-booking system. Most Bookings never become part of a Meeting.
_Avoid_: Reservation, slot

**Meeting**:
An event that people register for, made up of one or more Bookings, all made by the same Organizer. It exists only once that Organizer opens registration for it.
_Avoid_: Event, conference, seminar (as a model term)

**Organizer**:
The staff member who made the Bookings behind a Meeting; each Meeting has exactly one. Only the Organizer can open registration, which creates the Meeting.
_Avoid_: Owner, host, booker (as a model term)

**Co-organizer**:
A staff member the Organizer adds to a Meeting after registration opens, with the same rights to manage it.
_Avoid_: Assistant, delegate, secretary (as a model term)

### Attendance

**Attendee**:
A person who holds a Registration for a Meeting. The system knows only people who have registered, not who was invited. Someone attending in another person's place (ผู้แทน) is simply an Attendee with their own Registration; the system does not link them to the person they replace.
_Avoid_: Participant, guest, registrant, invitee, delegate (as a model term)

**Internal Attendee**:
An Attendee who counts as staff of the org.
_Avoid_: Staff attendee, employee

**External Attendee**:
An Attendee who is not staff of the org, including staff of other agencies in the same ministry.
_Avoid_: Guest, visitor, outsider

**Registration**:
One Attendee's sign-up for a Meeting, made by the Attendee through the Registration Link or added by the Organizer or a Co-organizer. It covers every Booking in the Meeting; nobody registers for only some of them. A Registration is either Active or Cancelled.
_Avoid_: Sign-up, enrolment, RSVP

**Cancelled Registration**:
A Registration withdrawn by its Attendee or removed by the Organizer or a Co-organizer. It is kept on record, not deleted.
_Avoid_: Deleted, withdrawn

**Registration Link**:
The link, and the QR code that encodes it, that opens a Meeting's registration form. The Organizer circulates it; the system does not track who received it.
_Avoid_: Invitation, form URL

**Check-in**:
The record that an Attendee arrived at one Booking of a Meeting. A multi-Booking Meeting has one Check-in per Booking the Attendee turns up to.
_Avoid_: Attendance, sign-in
