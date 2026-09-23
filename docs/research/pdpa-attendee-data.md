# PDPA obligations for collecting attendee data

- **Ticket:** #8 (map: #1)
- **Researched:** 2026-09-23
- **Question:** What does Thailand's Personal Data Protection Act B.E. 2562 (PDPA) require of a conference registration service that collects internal and external attendees' personal data? Cover the lawful basis, consent wording, privacy notice and retention. In particular: do dietary needs such as halal (which can reveal religion) or allergies (health data) count as sensitive data under Section 26 and need explicit consent?
- **Scope note:** Not legal advice. Every claim cites a primary source listed in [Sources](#sources). Where the sources do not settle a point, this is stated in [Open questions](#open-questions-and-uncertainties).

## Short answer

1. **Lawful basis.** If the organization is a public authority, name, position, organization and contact details can be collected **without consent**. The basis is "public task / official authority" (s.24(4)). The PDPC calls consent the *last* basis, to use only when no other basis applies [S3 §3]. Asking staff for consent to register for an official meeting would not be "freely given" [S2 s.19 ¶4; S3 §3.1 ex.2].
2. **Dietary data is the exception.** Allergies are **health data**, which is a listed Section 26 category. No Section 26 exception covers catering, so the organization needs **explicit consent** [S2 s.26]. A halal (or vegetarian/เจ) meal choice can reveal **religious belief**. No PDPC notification or guideline says whether data that only *reveals* religion is sensitive, so the point is unsettled. Treat it as sensitive: a separate, optional, unticked consent checkbox costs little. A Section 26 breach carries an administrative fine of up to THB 5 million [S2 s.84].
3. **Privacy notice.** The notice is mandatory whatever the lawful basis. Give it before or at collection. It can be delivered by URL or QR code, and it must state the retention period [S2 s.23; S4 §4.1, §6]. Some data does not come from the person themselves: a delegate named by the registrant, attendees the organizer adds, or invitees' emails from other agencies. Those people must get the notice by the first contact at the latest [S2 s.25; S4 §4.2].
4. **Retention.** The PDPA sets no fixed period. The organization must state one and erase the data when it ends [S2 s.23(3), s.37(3)]. Dietary data should be deleted soon after the event. The sign-in sheet may be an official or financial record under the government records regulation. If so, it can be kept longer: the PDPA allows retention for legal compliance and for s.24(4) tasks [S2 s.33 ¶2, s.37(3); S15 ข้อ 57].
5. **Government-specific duties.** A records-of-processing log (ROPA) is required, and no small-entity exemption applies [S12]. A DPO is required if the agency is on the PDPC's lists, which since 2568 include provinces, provincial administrative organizations, city municipalities and Pattaya [S10; S11]. The agency must also meet the Official Information Act's rules for personal-information systems [S14 s.23].

---

## 1. Does the PDPA apply?

- Name, position, organization, contact details and dietary needs all relate to an identifiable natural person, so they are "Personal Data" [S2 s.6].
- The PDPA's exemptions cover state security, courts, Parliament, mass media, credit bureaus and household use. None of them covers a registration service [S2 s.4].
- The PDPC has told a state agency that **all** personal data a state agency collects needs consent or a Section 24/26 basis, unless the activity is exempt under Section 4 [S5, ลำดับที่ 1, ประเด็นหารือที่ 6].
- Where a sector-specific law also protects personal data (for state agencies, the Official Information Act), that law applies. The PDPA's rules on collection, use, disclosure and data-subject rights still apply **in addition** [S2 s.3(1)].

## 2. Lawful basis

The six non-consent bases are listed in s.24: (1) archives/research/statistics, (2) vital interests, (3) contract, (4) public task or official authority, (5) legitimate interests, (6) legal obligation [S2 s.24]. The PDPC's consent guideline says consent is "the last lawful basis" a controller should use, only when no s.24 or s.26 exception fits (ความยินยอม...จึงเป็นฐานทางกฎหมายสุดท้าย) [S3 §3].

| Data / purpose | Recommended basis | Why |
|---|---|---|
| Name, position, organization, contact details, used to register, remind, and notify of booking changes | **s.24(4)** public task / official authority, if the organization is a public authority | Running the agency's official meetings is part of its functions [S2 s.24(4)]. |
| The same, if the controller is *not* a public authority (e.g. a state enterprise acting commercially, or a private body) | **s.24(5)** legitimate interests | The PDPC says employees or representatives of a counterparty organization are not parties to the contract, so the contract basis is unavailable; legitimate interests can be used, with care [S5, ลำดับที่ 9, ประเด็นหารือที่ 1]. |
| Sign-in sheet / attendance record kept as an official or financial record | s.24(4), and s.24(6) where a regulation requires retention | See [§6](#6-retention-and-erasure). |
| Dietary needs (allergies, halal, vegetarian) | **Explicit consent, s.26** | See [§4](#4-dietary-data-and-section-26). |
| Reuse of the contact list for *other* events or newsletters | New purpose: needs notice plus consent, or another basis | Data may not be used for a purpose different from the one notified unless the new purpose is notified and consented to, or the law allows it [S2 s.21]. |

**Internal staff and consent.** Consent must be "freely given". Consent must not be made a condition of a service when the data is not needed for that service [S2 s.19 ¶4]. The PDPC gives a direct government example: a state agency made people consent to giving an unrelated email address before they could use a road-maintenance service. The PDPC held that this consent was not freely given [S3 §3.1, ตัวอย่างที่ 2]. Do not rest core registration on staff consent. Use s.24(4), and keep consent for the optional dietary fields only.

## 3. Privacy notice (s.23)

**Content.** Before or at collection, the controller must tell the data subject [S2 s.23]:

1. the purpose, including any s.24 basis relied on instead of consent;
2. whether the data is required by law or contract, and what happens if it is not provided;
3. the data collected **and the retention period**, or, if a period cannot be specified, the expected period "according to the data retention standard";
4. the categories of persons or entities the data may be disclosed to;
5. the controller's contact details, and those of its representative or DPO where applicable;
6. the data subject's rights (withdrawing consent, access, portability, objection, erasure, restriction, rectification, complaint).

The PDPC notice guideline repeats this list. It adds the **lawful basis** and **cross-border transfers** as items to disclose. It says that when the retention period ends the data must be erased "immediately" (โดยทันที) [S4 §4.1(1)–(10) and หมายเหตุ].

**Delivery.** The notice may be given in writing, orally, by SMS or email, or "by stating the details in a URL or QR code". A layered approach (a short statement that links to the full notice) is acceptable if the link is prominent [S4 §6, §6.1]. This fits a form reached by QR code or link.

**Data not collected from the person themselves (s.25).** Collection from another source is allowed only if (1) the person is notified without delay, within 30 days, **and** consents, or (2) the collection falls under a s.24 or s.26 exception [S2 s.25 ¶1]. Where the data will be used to contact the person, the notice must be given **at the first contact** [S2 s.25 ¶3]. The PDPC's worked example is close to this project. Agency B received members' names, addresses and phone numbers from Agency C's secretary in order to invite them to a seminar. Agency B had to give the notice at its first contact with them [S4 §4.2, ตัวอย่าง]. In this service, s.25 covers:

- a **delegate (ผู้แทน)** named by the original registrant;
- attendees the **organizer adds** by hand;
- **external invitees** whose email addresses came from their own organizations.

**State agencies are not exempt.** The PDPC told a state agency that it must give a privacy notice for every activity not exempt under s.4. A separate internal privacy *policy* is not required by the PDPA, but the PDPC recommends one as an organizational measure [S5, ลำดับที่ 1, ประเด็นหารือที่ 5].

**Penalty.** Failure to comply with s.23 (including via s.25) carries an administrative fine of up to THB 1 million [S2 s.82].

## 4. Dietary data and Section 26

### 4.1 What Section 26 covers

Section 26 prohibits collecting personal data "pertaining to racial, ethnic origin, political opinions, cult, religious or philosophical beliefs, sexual behavior, criminal records, **health data**, disability, trade union information, genetic data, biometric data, or of any data which may affect the data subject in the same manner, as prescribed by the Committee" without **explicit consent**, unless an exception applies [S2 s.26 ¶1]. The PDPC's guideline gives the Thai wording as ข้อมูลส่วนบุคคล**เกี่ยวกับ**...ความเชื่อในลัทธิ ศาสนาหรือปรัชญา...ข้อมูลสุขภาพ ("data *about* ... religious belief ... health data") [S3 §3].

### 4.2 No exception fits catering

- s.26(1) covers danger to life or health **only where the data subject is incapable of giving consent**. It does not cover collecting allergy data in advance [S2 s.26(1)].
- s.26(5) needs processing "necessary for **compliance with a law**" for listed purposes: preventive or occupational medicine, public health, social protection, research, or substantial public interest. Arranging lunch is not one of them [S2 s.26(5)(a)–(e)].
- s.26(2) (non-profit bodies' own members) and s.26(3)–(4) (data made public; legal claims) do not apply [S2 s.26(2)–(4)].

### 4.3 Allergies: sensitive, explicit consent required

A food allergy or intolerance is information about a person's health, so it falls under "health data" [S2 s.26 ¶1]. With no applicable exception (§4.2), **explicit consent is required**.

### 4.4 Halal, vegetarian, เจ: unsettled, treat as sensitive

- A halal meal choice is not a statement of faith, but in a Thai context it strongly indicates one. Section 26 covers data "pertaining to" (เกี่ยวกับ) religious belief [S2 s.26; S3 §3].
- Section 26 lets the PDPC designate other "data which may affect the data subject in the same manner". The PDPC's notification index (all four pages, checked 2026-09-23) lists no such notification [S13].
- None of the PDPC guidelines reviewed discusses data that only *indicates* a sensitive category: the consent guideline [S3], the notice guideline [S4], the consultation casebook [S5], or the 2026 Basic Guidelines [S6]. A search of S6's text for ฮาลาล, มังสวิรัติ, แพ้อาหาร, อาหารเจ and ประเภทอาหาร returned no matches.
- **Conclusion:** the legal status is not settled in primary sources. Consent is cheap: one optional checkbox. Getting it wrong is expensive: up to THB 5 million for violating s.26 ¶1 [S2 s.84], and criminal liability if s.26 data is used or disclosed unlawfully in a way likely to cause damage [S2 s.79]. **Treat every dietary field as Section 26 data.**

### 4.5 What valid explicit consent looks like

From the Act [S2 s.19]:

- given before or at collection; requested explicitly **in writing or electronically**;
- states the purpose; is **clearly distinguishable from other matters**; is easy to access and understand; uses plain language; does not mislead;
- **freely given**: not a condition of a service for data the service does not need;
- can be **withdrawn at any time, as easily as it was given**. If withdrawal has consequences, the person must be told what they are.

From the PDPC consent guideline [S3]:

- **specific** purpose; no bundling of several purposes into one consent (§3.3, ตัวอย่างที่ 4);
- tell the person: who the controller is, the purpose, the types of data, and how to withdraw (§3.4);
- a **clear affirmative act** by the data subject, e.g. "clicking the checkbox to indicate 'consent' by the data subject themselves" (การคลิกใน checkbox...โดยเจ้าของข้อมูลส่วนบุคคลเอง) (§3.6);
- withdrawal no harder than giving consent, e.g. not "phone us during office hours" when consent was a click (§5, ตัวอย่างที่ 5).

The PDPC Basic Guidelines add: **no pre-ticked boxes** [S6, printed p.389, §7.7.1(4)].

### 4.6 Consequences for this service

- **Optional, and never a condition of registering.** Registration does not depend on the dietary fields, so consent can be freely given, including by internal staff [S2 s.19 ¶4].
- **The data subject must consent.** A registrant cannot consent on behalf of a delegate. Dietary data about another person is collection from another source, which needs notice and that person's own consent [S2 s.25 ¶1(1)]. **The delegate should enter their own dietary needs through their own link.**
- **Data minimisation** (s.22): collection must be "limited to the extent necessary" [S2 s.22]. Ask for a *meal type* (e.g. "no pork / halal-certified", "vegetarian", "เจ") and a free-text allergy note. Never ask for religion or the reason behind a choice.
- **QR check-in must not use face recognition.** Facial recognition data is biometric data under s.26 [S2 s.26 ¶2]. A QR token is fine.

## 5. Government-agency specifics

**DPO.** Public authorities "as prescribed and announced by the Committee" must appoint a DPO [S2 s.41(1)].

- The 2566 notification lists specific ministries' departments and other state bodies [S10, บัญชีท้ายประกาศ]. It took effect 90 days after publication on 18 July 2566 [S10 ข้อ 2].
- Notification No. 2 of 2568 adds **all provinces (จังหวัด), provincial administrative organizations (อบจ.), city municipalities (เทศบาลนคร) and Pattaya City** [S11 ข้อ 4]. It took effect 90 days after publication on 9 October 2568 [S11 ข้อ 2].
- If the organization is on either list, the notice must give the DPO's contact details [S2 s.23(5), s.41 ¶5].

**Records of processing (ROPA).** Every controller must keep the s.39 records [S2 s.39]. The 2567 small-entity exemption covers only: SMEs, community and social enterprises, cooperatives, foundations/associations/religious or non-profit bodies, condominium and housing-estate juristic persons, household businesses, and natural-person controllers. **Government agencies are not listed** [S12 ข้อ 4]. Even exempt entities must record processing of Section 26 data [S12 ข้อ 5 ¶2(3)].

**Official Information Act B.E. 2540 (OIA).** State agencies must [S14 s.23]:

- keep personal-information systems "only as relevant and necessary" to their objectives, and discontinue them when no longer needed;
- try to collect directly from the data subject;
- publish in the Royal Gazette the categories of persons, the types of system, normal uses, access and correction procedures, and data sources;
- keep the data accurate, and secure it appropriately;
- when collecting directly, tell the person, in advance or when requesting the data, the purpose, the normal uses, and whether providing it is voluntary or legally required.

Also note:

- Disclosure to other agencies or persons without the data subject's written consent is limited to the cases listed in s.24 [S14 s.24].
- Under the OIA, "person" means Thai nationals and non-Thai nationals resident in Thailand [S14 s.21].
- The PDPC has said that disclosing meeting minutes that name the officials who attended is governed by the OIA as the sector law under PDPA s.3 [S5, ลำดับที่ 11]. The same logic applies to requests to disclose attendance lists.

**Official records retention (Saraban regulation).** For official documents (หนังสือราชการ) [S15]:

- the normal minimum retention is **10 years**;
- routine, unimportant documents: at least **1 year**;
- finance-related documents that no longer serve as evidence: at least **5 years**, after the Office of the Auditor General has audited them without issue;
- documents governed by a special law or regulation follow that rule [S15 ข้อ 57];
- electronic official documents are kept indefinitely by default. The head of the agency may order non-archival ones destroyed after 10 years [S15 ข้อ 89/5].

These rules apply to "หนังสือราชการ" [S15 ข้อ 6]. Whether registration records count is an open question (see [Open questions](#open-questions-and-uncertainties)).

## 6. Retention and erasure

- **State a period.** The notice must state the retention period, or an expected period if an exact one cannot be given [S2 s.23(3)]. The PDPC suggests describing the criteria, e.g. "the period a specific law requires" [S4 §4.1 หมายเหตุ].
- **Erase at the end.** Controllers must have a system that erases data when the retention period ends, when it becomes irrelevant or exceeds the purpose, or when consent is withdrawn. Data kept for s.24(4) purposes, legal claims or legal compliance is exempt [S2 s.37(3)]. The same exemptions limit the right to erasure [S2 s.33 ¶2].
- **Erasure requests** must be carried out without delay and within **90 days** of the request. Erasure covers copies and backups [S9 ข้อ 3]. If backups cannot be purged at once, the data must be protected from use until it is erased [S9 ข้อ 4]. These rules also govern the s.37(3) end-of-retention system [S9 ข้อ 9].
- **Access requests** must be met without delay and within **30 days** [S2 s.30 ¶4]. The PDPC issued a new notification on access and copy requests, published 16 July 2569 [S16]. Its detailed rules were not read for this research (text extraction failed).
- **Withdrawal of dietary consent** removes the basis for that data, so it must be erased [S2 s.33 ¶1(2), s.37(3)].

## 7. Other obligations the build must meet

- **Security.** The 2565 security notification sets a minimum standard [S7 ข้อ 4]:
  - organizational, technical and, where needed, physical measures in proportion to risk;
  - access control on a need-to-know basis with least privilege;
  - user-access management;
  - audit trails of access, change and deletion;
  - staff awareness.
- **Breach notification.** Notify the PDPC Office without delay, within 72 hours where feasible, unless the breach is unlikely to create risk. Notify the affected people too if the risk is high [S2 s.37(4); S8].
- **Processors.** If a vendor or cloud host runs the service, the controller needs a data processing agreement [S2 s.40 ¶3]. The processor's security must meet the same minimum standard [S7 ข้อ 6].
- **Cross-border transfer.** If data leaves Thailand (e.g. foreign-hosted email or messaging), the s.28 rules apply [S2 s.28].
- **DPIA.** The PDPA text does not mandate a DPIA. The PDPC's 2026 Basic Guidelines use an **online seminar registration system** as their worked DPIA example: registrants' name, contact, organization and position, with mitigations such as role-restricted access, encryption in transit and at rest, and daily backups [S6, printed pp.598–600].
- **Penalty tiers** (administrative fines) [S2 s.82–s.84]:
  - notice or ROPA failures: up to THB 1M;
  - breaches of s.21, s.22, s.24, s.25 ¶1, s.37: up to THB 3M;
  - breaches of s.26: up to THB 5M.

## Open questions and uncertainties

1. **Is the organization a "public authority", and is it on a DPO list?** The s.24(4) recommendation and the DPO duty both depend on this. Check the org's legal form against [S10] and [S11].
2. **Halal/vegetarian as religious data** has no primary-source answer (§4.4). This research recommends the conservative choice; it has not found a ruling.
3. **Sign-in sheet retention.** Is the sign-in sheet an official document or a financial record (e.g. evidence for meal-expense disbursement)? If so, it may need to be kept for 1, 5 or 10 years under [S15 ข้อ 57], or for longer under Ministry of Finance or Auditor-General rules. Those rules were **not researched here**. Ask the organization's records (สารบรรณ) and finance officers.
4. **Language of the Act.** Quotations from the Act use the MDES **unofficial** English translation (marked "corrected to align with Thai version on June 20, 2021") [S2]. The authoritative text is the Thai Royal Gazette version [S1].
5. **The Basic Guidelines' sample privacy notice mislabels bases.** It lists "มาตรา 24 (3) – ประโยชน์โดยชอบด้วยกฎหมาย" and "มาตรา 24 (1) – การยินยอม" [S6, printed p.388]. In the Act, s.24(3) is contract, s.24(5) is legitimate interests, and consent is not a s.24 subsection [S2 s.24]. Do not copy that template's section numbers.
6. **The 2569 access-request notification** [S16] was not read in detail.

---

## Implications for the spec

### Registration form

- Split the form into two visibly separate parts.
  - **Registration:** name, position, organization, contact channel. Required. No consent checkbox. Its lawful basis is shown in the notice (s.24(4)).
  - **Meal arrangements (optional):** a meal-type choice ("regular", "no pork / halal", "vegetarian", "เจ", "other"), an allergy free-text field, and a separate **unticked** consent checkbox. The meal fields stay disabled until the box is ticked.
- Never ask for religion or the reason behind a meal choice.
- Show a short layered notice at the top of the form, with a prominent link to the full notice [S4 §6]. Record which notice version was shown.
- **Delegates (ผู้แทน):** the registrant enters only the delegate's name and contact. The system then sends the delegate their own link, with the notice, to confirm and to fill in their own meal section and consent. The registrant never enters a delegate's dietary data.
- **Organizer-added attendees and external email invitations:** the first message sent to the person must contain or link to the notice [S2 s.25 ¶3].
- **QR check-in** uses a token only. No face recognition.

### Consent text (draft, Thai first; the dietary section only)

> ☐ ข้าพเจ้ายินยอมให้ [ชื่อหน่วยงาน] เก็บรวบรวมและใช้ข้อมูลความต้องการด้านอาหารที่ข้าพเจ้าระบุข้างต้น (เช่น อาหารฮาลาล มังสวิรัติ อาหารเจ หรือการแพ้อาหาร) ซึ่งอาจบ่งบอกถึงความเชื่อทางศาสนาหรือข้อมูลสุขภาพ **เพื่อจัดเตรียมอาหารสำหรับการประชุม [ชื่อการประชุม] เท่านั้น** ข้อมูลนี้จะเปิดเผยเฉพาะเจ้าหน้าที่ผู้จัดการประชุมและผู้จัดเตรียมอาหาร และจะถูกลบภายใน [30] วันหลังวันประชุม การให้ข้อมูลส่วนนี้ไม่เป็นเงื่อนไขในการลงทะเบียน ท่านสามารถถอนความยินยอมได้ทุกเมื่อผ่าน [ลิงก์จัดการการลงทะเบียน] หากถอนความยินยอม เราจะไม่สามารถจัดอาหารตามความต้องการพิเศษของท่านได้

> ☐ I consent to [organization] collecting and using the dietary needs I entered above (e.g. halal, vegetarian, เจ, or food allergies), which may reveal religious belief or health information, **only to arrange meals for [meeting name]**. Only the meeting organizers and the caterer will see it, and it will be deleted within [30] days after the meeting. Giving this information is not a condition of registering. You can withdraw consent at any time at [manage-registration link]; if you do, we cannot arrange a special meal for you.

This text covers every element the PDPC requires: controller, specific purpose, data types, recipients, retention, freedom to refuse, a withdrawal route as easy as giving consent, and the consequence of withdrawal [S2 s.19; S3 §3.3–3.6, §5].

### Data model

- `Person`: fields as needed.
- `Registration`:
  - `source`: `self` | `named_by_registrant` | `added_by_organizer` | `invited`. This drives the s.25 notice-at-first-contact duty.
  - `notice_version`, `notice_delivered_at`.
- `DietaryRequirement`: a **separate table**, 1:1 with `Registration`, holding `meal_type`, `allergy_note` and `purge_after`.
- `Consent`: `purpose = dietary`, `text_version`, `given_at`, `given_by_person_id`, `withdrawn_at`. The system must reject a consent where `given_by_person_id` is not the data subject. On withdrawal, `DietaryRequirement` is hard-deleted.
- **Exports:**
  - The **sign-in sheet** export never includes dietary fields.
  - The **catering** export shows counts by meal type. It shows names only next to allergy notes and non-regular meals, because the caterer needs them.
- **Access control and audit** [S7 ข้อ 4(6)]:
  - Dietary data is visible only to the organizer of that meeting and the catering role.
  - Every read, export and delete of dietary data is logged.
- A ROPA entry per processing activity: registration, reminders, check-in, sign-in sheet, catering [S2 s.39; S12].

### Retention policy (to confirm with the organization's records and finance officers)

| Data | Proposed retention | Basis |
|---|---|---|
| Dietary needs and allergy notes | Delete **30 days after the meeting**, or at once on withdrawal or cancellation | Purpose spent [S2 s.37(3)]; consent withdrawn [S2 s.33 ¶1(2)] |
| Registration and contact details | Delete or anonymise **N months after the meeting** (N set by the organization, e.g. 12) unless it forms part of an official record | Purpose spent [S2 s.37(3)] |
| Sign-in sheet / attendance record | As the Saraban regulation or finance rules require (1, 5 or 10 years; see [Open question 3](#open-questions-and-uncertainties)) | Exempt from erasure for legal compliance and s.24(4) [S2 s.33 ¶2, s.37(3); S15 ข้อ 57] |
| Backups | Purged on the same schedule; protected until purged | [S9 ข้อ 3–4] |
| Audit logs | Organization's security policy | [S7 ข้อ 4(6)(ง)] |

The notice must state each period, or the criteria that set it [S2 s.23(3); S4 §4.1].

---

## Sources

All sources were accessed on 2026-09-23.

- **[S1]** Personal Data Protection Act B.E. 2562, official Thai text, Royal Gazette vol. 136, part 69 ก, 27 May 2562. https://www.ratchakitcha.soc.go.th/DATA/PDF/2562/A/069/T_0052.PDF
- **[S2]** Personal Data Protection Act B.E. 2562 (2019), unofficial English translation, Ministry of Digital Economy and Society (MDES), "corrected to align with Thai version on June 20, 2021". https://www.mdes.go.th/uploads/tinymce/source/%E0%B8%AA%E0%B8%84%E0%B8%AA/Personal%20Data%20Protection%20Act%202019.pdf
- **[S3]** PDPC, แนวทางการดำเนินการในการขอความยินยอมจากเจ้าของข้อมูลส่วนบุคคล ตามพระราชบัญญัติคุ้มครองข้อมูลส่วนบุคคล พ.ศ. ๒๕๖๒ (guideline on requesting consent, issued under s.16(3); PDF dated Sept 2022), hosted by MDES. https://www.mdes.go.th/uploads/tinymce/source/%E0%B8%AA%E0%B8%84%E0%B8%AA/%E0%B9%81%E0%B8%99%E0%B8%A7%E0%B8%97%E0%B8%B2%E0%B8%87%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%94%E0%B8%B3%E0%B9%80%E0%B8%99%E0%B8%B4%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%83%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%82%E0%B8%AD%E0%B8%84%E0%B8%A7%E0%B8%B2%E0%B8%A1%E0%B8%A2%E0%B8%B4%E0%B8%99%E0%B8%A2%E0%B8%AD%E0%B8%A1%E0%B8%AF.pdf
- **[S4]** PDPC, แนวทางการดำเนินการในการแจ้งวัตถุประสงค์และรายละเอียดในการเก็บรวบรวมข้อมูลส่วนบุคคลจากเจ้าของข้อมูลส่วนบุคคล (guideline on privacy notices, issued under s.16(3); PDF dated Sept 2022), hosted by MDES. https://www.mdes.go.th/uploads/tinymce/source/%E0%B8%AA%E0%B8%84%E0%B8%AA/%E0%B9%81%E0%B8%99%E0%B8%A7%E0%B8%97%E0%B8%B2%E0%B8%87%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%94%E0%B8%B3%E0%B9%80%E0%B8%99%E0%B8%B4%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%83%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%81%E0%B8%88%E0%B9%89%E0%B8%87%E0%B8%A7%E0%B8%B1%E0%B8%95%E0%B8%96%E0%B8%B8%E0%B8%9B%E0%B8%A3%E0%B8%B0%E0%B8%AA%E0%B8%87%E0%B8%84%E0%B9%8C%E0%B8%AF.pdf
- **[S5]** PDPC, แนวปฏิบัติสำหรับผู้ควบคุมข้อมูลส่วนบุคคลและผู้ประมวลผลข้อมูลส่วนบุคคล: กรณีศึกษาจากข้อหารือ (PDPC opinions answering state agencies' consultations, vol. 1, published 10 Feb 2566). https://www.pdpc.or.th/wp-content/uploads/2023/12/12pdpcbook.pdf (index page: https://www.pdpc.or.th/pdpc-book/pdpc-guidelines/)
- **[S6]** PDPC, แนวปฏิบัติพื้นฐานด้านการคุ้มครองข้อมูลส่วนบุคคล (ภาคส่วนทั่วไป) / Basic Guidelines for Personal Data Protection (General Sector), 2026. https://www.pdpc.or.th/wp-content/uploads/2026/02/Guidelines-PDPC-v1.pdf. "Printed p." means the page number printed on the page.
- **[S7]** ประกาศคณะกรรมการคุ้มครองข้อมูลส่วนบุคคล เรื่อง มาตรการรักษาความมั่นคงปลอดภัยของผู้ควบคุมข้อมูลส่วนบุคคล พ.ศ. ๒๕๖๕ (Royal Gazette 20 June 2565). https://www.pdpc.or.th/wp-content/uploads/2024/01/announcement-pdpc-05.pdf
- **[S8]** ประกาศฯ เรื่อง หลักเกณฑ์และวิธีการในการแจ้งเหตุการละเมิดข้อมูลส่วนบุคคล พ.ศ. ๒๕๖๕. https://www.pdpc.or.th/wp-content/uploads/2023/12/announce-15122565.pdf
- **[S9]** ประกาศฯ เรื่อง หลักเกณฑ์ในการลบหรือทำลาย หรือทำให้ข้อมูลส่วนบุคคลเป็นข้อมูลที่ไม่สามารถระบุตัวบุคคลได้ พ.ศ. ๒๕๖๗ (Royal Gazette 13 Aug 2567). https://www.pdpc.or.th/wp-content/uploads/2024/08/39218.pdf
- **[S10]** ประกาศฯ เรื่อง ผู้ควบคุมข้อมูลส่วนบุคคลและผู้ประมวลผลข้อมูลส่วนบุคคลที่เป็นหน่วยงานของรัฐ ซึ่งต้องจัดให้มีเจ้าหน้าที่คุ้มครองข้อมูลส่วนบุคคล พ.ศ. ๒๕๖๖ (Royal Gazette 18 July 2566). https://www.pdpc.or.th/wp-content/uploads/2023/12/announce-18072566.pdf
- **[S11]** The same notification, (ฉบับที่ ๒) พ.ศ. ๒๕๖๘ (Royal Gazette 9 Oct 2568). https://www.pdpc.or.th/wp-content/uploads/2025/10/PDPC-0110256801.pdf
- **[S12]** ประกาศฯ เรื่อง การยกเว้นการบันทึกรายการของผู้ควบคุมข้อมูลส่วนบุคคลซึ่งเป็นกิจการขนาดเล็ก พ.ศ. ๒๕๖๗ (Royal Gazette 8 Jan 2568; repeals the 2565 version). https://www.pdpc.or.th/wp-content/uploads/2025/01/-1--ROPA--.-39.pdf
- **[S13]** PDPC notification index (ประกาศคณะกรรมการฯ), pages 1–4. https://www.pdpc.or.th/category/pdpc-law/announce/announcement-pdpc/
- **[S14]** Official Information Act B.E. 2540 (พระราชบัญญัติข้อมูลข่าวสารของราชการ), Office of the Council of State consolidated text, hosted by the Ministry of Public Health. https://hss.moph.go.th/fileupload_doc_slider/2016-11-18-54-16-246524.pdf
- **[S15]** ระเบียบสำนักนายกรัฐมนตรีว่าด้วยงานสารบรรณ พ.ศ. ๒๕๒๖, consolidated through (ฉบับที่ ๔) พ.ศ. ๒๕๖๔, hosted by the Law Reform Commission. https://lawreform.go.th/uploads/files/1678240071-b99vw-cbccp.pdf
- **[S16]** ประกาศฯ เรื่อง หลักเกณฑ์เกี่ยวกับการเข้าถึงและการขอรับสำเนาข้อมูลส่วนบุคคล...พ.ศ. ๒๕๖๙ (Royal Gazette 16 July 2569). https://www.pdpc.or.th/27840/
