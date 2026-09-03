# Design brief — `kelling-0284` — NEVER INGEST

Seventh corpus in the series, after `harborpoint-marina` (insurance),
`riverwalk-garage` (engineering/AEC), `northfield-grain` (commercial lending),
`corbin-tower-632588` (interiors/architecture), `marchwood-0447` (US securities
regulation) and `shinonome-0392` (global patent prosecution).

**Vertical: private law practice**, seen from inside a US full-service law firm —
Litigation & Dispute Resolution, Corporate & Commercial, Labor & Employment,
Real Estate, and Bankruptcy & Reorganization. The archive whose value the demo
proves is the firm's own mail journal archive; the system that gets the answer
wrong is the firm's document management system (DMS). The demo customer is a law
firm: the story is the firm's own nightmare — a legal-malpractice demand against
the firm — ended by the firm's own email archive.

No real firm, client, product, or person is named. The professional-conduct and
limitations framework is real and is recorded in §7 of the build notes.

---

## Phase 0 — the six beats

1. **The needle.** June 9, 2011 — Rosalind Tenniel, General Counsel of Torvane
   Industrial Group, Inc. (Erie, PA), writes to relationship partner Arthur
   Pellum of Prescott Vane LLP, attaching a signed confirmation letter
   (`Torvane_Scope_Confirmation_2011-06-09.pdf`): the firm's engagement under
   matter **2011-0284** is limited to Torvane's claims against Ridgeline
   Constructors; Torvane has considered and **elected not to assert** the
   warranty claim against Brandt Thermal Systems; that claim is **expressly
   outside the scope of the engagement**; the firm is **not asked to take any
   step to evaluate, preserve, or pursue it**; and the confirmation "is not
   limited to any period and stands unless withdrawn by me in writing."
2. **Both systems lose it.** The February 27–28, 2016 **Casebridge → Novarra**
   DMS migration carried profiled documents but excluded the legacy CommsStore
   module, where all matter correspondence filed before January 1, 2014 lived.
   Novarra's controlled "Matter Scope" field was derived from the
   engagement-letter document class — so matter 2011-0284 reads "claims arising
   out of the Kelling Station Unit 2 expansion project," the April 2011
   engagement letter's broad wording, with no trace of the June 2011 limitation
   (which was never papered as an amendment — Tenniel confirmed by letter
   attached to email, at her own insistence, "no need to re-paper the
   engagement"). Torvane's side lost it too: legal filed email to a matter
   workspace retired in its 2017 legal-ops platform change, and the 2021 sale to
   Copeland Ridge Partners transferred contracts, not correspondence.
3. **Everyone has left.** Pellum retired June 2018 (recalls a carve-out, has no
   documents); Tenniel left Torvane in March 2015; associate Caleb Wisner went
   in-house in 2014; Torvane's VP Engineering Walt Hagerman died in 2020.
4. **The claim.** November 14, 2024 — Garvey Strom LLP, for Torvane under new GC
   Corinne Ashby, demands **$3,675,000**: the value of the Brandt warranty claim
   the firm allegedly let die ($2,140,000 excess fuel + $890,000 replacement
   media + $645,000 unplanned downtime, per Torvane's own 2013 RTO performance
   study). Premise: the firm was engaged on "claims arising out of the Kelling
   Station Unit 2 expansion project" — the engagement letter in Novarra says
   exactly that — and never advised on the Brandt limitations deadline.
5. **The archive produces it — plus the precedent.** January 9, 2025 — the mail
   journal archive (journaling every message since October 2007, never migrated
   because it is an archive, not a system of record) returns the eleven-message
   2011 matter sequence with the signed confirmation letter intact. January 13 —
   a second pass surfaces **October 17, 2013**: Tenniel, unprompted, striking
   the Brandt matter from the firm's draft audit response to Caulfield Roth,
   citing her June 9, 2011 confirmation **by date** — the client applying the
   carve-out itself, with no dispute pending.
6. **The claim collapses.** Response letter served January 21, 2025. Demand
   withdrawn in full **February 24, 2025**. Carrier file closed: indemnity $0,
   defense cost **$92,400**.

## The needle test

- Verbatim-quotable: "That claim is expressly outside the scope of your
  engagement, and Prescott Vane is not asked to take any step to evaluate,
  preserve, or pursue it."
- Attached document: `Torvane_Scope_Confirmation_2011-06-09.pdf`.
- Discriminated by an identifier that exists on wrong entities: **matter
  2011-0284** (the legacy Aldous & Crane real-estate matter carries the same
  number after the 2014 merger preserved legacy numbering) plus near-misses
  2011-0248, 2011-0824, 2011-0384, 2012-0284; and "scope confirmation" /
  engagement-limitation letters on ~10 other clients.
- Contradicted by the system of record: Novarra's Matter Scope field and the
  only engagement document it holds both say the engagement was unlimited.

## Cast — signal file (byte-exact address book)

Host firm: **Prescott Vane LLP** (`prescottvane.com`), ~240 lawyers,
Pittsburgh (HQ), Philadelphia, Harrisburg. Merged with Aldous & Crane
(Harrisburg) on January 1, 2014; legacy A&C matters kept their numbers.

```
Arthur Pellum <a.pellum@prescottvane.com>            Partner, Litigation, Pittsburgh (1987–ret. June 2018)
Caleb Wisner <c.wisner@prescottvane.com>             Associate, Litigation (2008–2014)
Evelyn Stanhope <e.stanhope@prescottvane.com>        General Counsel & Loss Prevention Partner (2012–)
Theodore Brannock <t.brannock@prescottvane.com>      Partner, Litigation (2009–)
Miriam Vogelsang <m.vogelsang@prescottvane.com>      Managing Partner (2019–; partner 2001–)
Howell Grady <h.grady@prescottvane.com>              Director, Records & Information Governance (2010–)
Anika Chaudhry <a.chaudhry@prescottvane.com>         Director, Practice Technology (2013–)
Lucille Ames <l.ames@prescottvane.com>               Docketing & Calendar Manager (2005–)
Dora Kraljic <d.kraljic@prescottvane.com>            Conflicts Counsel (2006–)
Sam Uram <s.uram@prescottvane.com>                   Associate, Litigation (2019–)
Renata Voss-Whitely <r.vosswhitely@prescottvane.com> Partner, Corporate (2011–)  [one BD email only]
PV Facilities <facilities@prescottvane.com>          (noise)
PV Professional Development <profdev@prescottvane.com> (noise)
```

Client and counterparties:

```
Rosalind Tenniel <rtenniel@torvaneindustrial.com>    GC, Torvane Industrial Group, Inc. (2004–Mar 2015)
Walt Hagerman <whagerman@torvaneindustrial.com>      VP Engineering, Torvane (d. 2020)
Corinne Ashby <cashby@torvaneindustrial.com>         GC, Torvane (2022–)
Alan Garvey <agarvey@garveystrom.com>                Garvey Strom LLP (claimant's counsel, 2024)
Janet Osei <josei@caulfieldroth.com>                 Caulfield Roth LLP (Torvane's auditors)
Denise Wachter <dwachter@keystonecounselmutual.com>  Claims attorney, Keystone Counsel Mutual Ins. Co.
Nora Feldkamp <nfeldkamp@dilworthhaynes.com>         Dilworth Haynes LLP (Ridgeline's counsel) [brief]
Torvane Logistics: Gil Prosky <gprosky@torvanelogistics.com>  (in-file noise; unrelated company & client)
```

Fictitious entities: Torvane Industrial Group, Inc. (Erie PA; specialty glass
and mineral-wool manufacturer); Kelling Station Unit 2 (its plant expansion,
2008–2011, incl. a regenerative thermal oxidizer, "the RTO"); Ridgeline
Constructors, Inc. (EPC contractor; arbitration respondent); Brandt Thermal
Systems, Inc. (RTO supplier; the carved-out claim); Caulfield Roth LLP
(auditors); Garvey Strom LLP; Dilworth Haynes LLP; Keystone Counsel Mutual;
Copeland Ridge Partners (PE buyer, 2021); Casebridge (legacy DMS, deployed
2004) and Novarra (successor DMS, cutover Feb 27–28, 2016); ticket NOV-2119.

## Signal email map (40)

Era 1 — the matter (2011–2014):
1.  Mar 24, 2011 — Tenniel → Pellum: Kelling Unit 2 commissioning failures; engage on Ridgeline claims. Thread start.
2.  Mar 25, 2011 — Pellum → Kraljic (conflicts): run check; Ridgeline, Brandt Thermal named. Attach: Conflict_Check_Report. (Brandt named = seed)
3.  Apr 04, 2011 — Pellum → Tenniel: engagement letter, matter 2011-0284 opened. Attach: Engagement_Letter (broad wording).
4.  Apr 07, 2011 — Tenniel returns countersigned letter. Supporting.
5.  May 10, 2011 — PV ProfDev: CLE compliance reminder. IN-FILE NOISE #1.
6.  May 17, 2011 — Wisner → Pellum: assessment; flags Brandt warranty claim + limitations. Attach: Limitations_Memo. Causation seed.
7.  May 19, 2011 — Pellum → Tenniel: raises Brandt claim; recommends tolling agreement or joinder; asks for instructions.
8.  May 26, 2011 — Tenniel → Pellum: commercial context (sole-source supplier across three plants); taking it to the CEO.
9.  Jun 08, 2011 — Pellum → Wisner cc Ames: call memo — Torvane elects not to pursue; written confirmation requested. Attach: Call_Memo.
10. Jun 09, 2011 — **THE NEEDLE.** Tenniel → Pellum cc Hagerman + signed letter. Attach: Torvane_Scope_Confirmation.
11. Jun 10, 2011 — Pellum → Wisner, Ames: acknowledge; close the Brandt limitations tickler; scope note updated in Casebridge. Causation.
12. Jul 19, 2011 — Pellum → Tenniel: arbitration demand filed against Ridgeline. Supporting.
13. Sep 08, 2011 — PV Facilities: Pittsburgh office 31st-floor move. IN-FILE NOISE #2.
14. May 22, 2012 — Pellum → Tenniel: hearing dates; Ridgeline's counsel (Feldkamp) proposal. Supporting.
15. Oct 10, 2013 — Osei → Pellum cc Tenniel: FY2013 audit inquiry letter. Attach: Audit_Inquiry + Draft_Audit_Response (draft lists Brandt from the old memo — prepared by Sam? no, by Wisner). Supporting.
16. Oct 17, 2013 — **PRECEDENT.** Tenniel: strike Brandt from the response; cites the June 9, 2011 confirmation by date.
17. Oct 18, 2013 — Pellum → Osei: revised response, Ridgeline arbitration only. Attach: Audit_Response_Final.
18. Nov 12, 2013 — PV Marketing: holiday card list. IN-FILE NOISE #3.
19. Feb 13, 2014 — Pellum → Tenniel: Ridgeline settled at $4,850,000; closing letter; matter closed.

Era boundary (2015–2021):
20. Mar 12, 2015 — Pellum → litigation group: Tenniel leaving Torvane; relationship note. Cross-year link.
21. Feb 26, 2016 — Chaudhry: Novarra cutover this weekend; CommsStore pre-2014 correspondence OUT OF SCOPE; journal archive remains the retention copy. Migration.
22. Mar 15, 2016 — Chaudhry → Grady: NOV-2119 — Matter Scope derived from engagement-letter class; closed-matter scope notes not carried; ticket closed "works as designed." Causation.
23. Jun 15, 2018 — Vogelsang: Pellum retirement announcement. Cross-year link.
24. Aug 13, 2019 — PV Facilities: parking garage access change. IN-FILE NOISE #4.
25. Oct 05, 2021 — Voss-Whitely → Brannock: Torvane acquired by Copeland Ridge Partners; relationship dormant since 2014. Cross-year link.

Era 2 — the claim (2024–2025):
26. Nov 14, 2024 — Ashby/Garvey demand arrives (forwarded by Stanhope): $3,675,000. Attach: Demand_Letter + RTO_Performance_Study excerpt. Present-day thread start.
27. Nov 14, 2024 — Stanhope: litigation hold; carrier notice to Wachter; Brannock assigned.
28. Nov 15, 2024 — Stanhope → Grady/Chaudhry: pull the complete 2011-0284 file.
29. Nov 18, 2024 — Chaudhry: Novarra results — engagement letter (broad), pleadings, settlement; NO limitation anywhere; Matter Scope field quoted. Attach: Novarra_Matter_Record. THE TRAP.
30. Nov 21, 2024 — Stanhope: on this record the demand letter's premise holds; Pellum recalls a carve-out but has nothing; Tenniel gone 2015; Wisner in-house; Hagerman deceased. Supporting.
31. Dec 09, 2024 — Wachter: reserves set on the current record; requests evaluation of early resolution. Supporting (stakes).
32. Dec 16, 2024 — Grady: the mail journal archive — journaling since Oct 2007, never migrated; propose targeted search. Product moment (setup).
33. Jan 09, 2025 — Grady: search results — the eleven-message 2011 sequence, attachments intact, incl. the signed confirmation. Attach: Journal_Archive_Search_Report. PRODUCT MOMENT.
34. Jan 09, 2025 — Brannock → Stanhope: the June 9, 2011 email quoted verbatim. Supporting.
35. Jan 13, 2025 — Grady: second pass — the Oct 17, 2013 audit-response email surfaces. Precedent recovery.
36. Jan 16, 2025 — Brannock: draft response letter — RPC 1.2(c) limited scope w/ informed consent confirmed in writing; the client's own 2013 application of it; limitations posture. Supporting.
37. Jan 21, 2025 — Stanhope → Garvey: response letter + supplemental production ("the ten emails from the 2011 sequence" — DELIBERATE MISCOUNT, it is eleven). Attach: Response_Letter. Formal rebuttal.
38. Dec 10, 2024 — wait, NO: noise #5 must be in range. Replace: Gil Prosky (Torvane Logistics LLC, unrelated) re a warehouse lease — Dec 10, 2024, slotted between 31 and 32. IN-FILE NOISE #5. (Renumber emails accordingly when writing.)
39. Feb 24, 2025 — Garvey: demand withdrawn in full. Attach: Withdrawal_Letter. OUTCOME.
40. Mar 10, 2025 — Stanhope → Vogelsang: post-mortem — both halves of causation; indemnity $0, defense $92,400; recommend journal-archive search in the claims workflow. OUTCOME.

(Exact numbering fixed at write time; noise #5 slots at Dec 10, 2024.)

## Attachments (15)

Conflict_Check_Report_2011-0284.pdf · Engagement_Letter_Torvane_2011-04-04.pdf ·
Wisner_Limitations_Memo_2011-05-17.pdf · Pellum_Call_Memo_2011-06-08.pdf ·
Torvane_Scope_Confirmation_2011-06-09.pdf · Caulfield_Roth_Audit_Inquiry_2013-10-10.pdf ·
Draft_Audit_Response_Torvane_FY2013.pdf · Audit_Response_Torvane_FY2013_Final.pdf ·
Novarra_Migration_Scope_Notice_2016-02-26.pdf · Garvey_Strom_Demand_Letter_2024-11-14.pdf ·
Kelling_RTO_Performance_Study_Excerpt_2013.pdf · Novarra_Matter_Record_2011-0284_2024-11-18.pdf ·
Journal_Archive_Search_Report_2025-01-09.pdf · PV_Response_Letter_2025-01-21.pdf ·
Torvane_Withdrawal_Letter_2025-02-24.pdf

## Load-bearing numbers (computed once)

- Demand: $2,140,000 (excess natural-gas consumption, FY2011–FY2013) +
  $890,000 (ceramic media replacement, 2012) + $645,000 (unplanned downtime,
  11 days) = **$3,675,000**. The RTO study and the demand letter must agree.
- Ridgeline settlement to Torvane: **$4,850,000** (Feb 2014).
- Defense cost: **$92,400**; indemnity **$0**.
- Journal archive: journaling since **October 2007**; ~**3 million** messages/year
  firm-wide in 2011; the 2009–2014 slice is ~**19 million** messages;
  the matter-scoped hit set returns in **14 minutes**.
- The 2011 matter sequence = **eleven** messages (Email-1,3,4,6,7,8,9,10,11,12 + one
  internal transmittal recorded in the search report); Email-37's cover letter
  says **ten** — the deliberate in-world inaccuracy. Email-33's report and the
  response letter state eleven correctly.

## Legal facts (verified level-of-generality; see BUILD-NOTES §7)

- **Pa. R.P.C. 1.2(c)**: a lawyer may limit the scope of the representation if
  the limitation is reasonable and the client gives informed consent. The 2011
  letter is drafted to be exactly that, in writing, signed by the GC.
- **ABA Statement of Policy Regarding Lawyers' Responses to Auditors' Requests
  for Information (1975)**: audit responses address matters as to which the
  lawyer has been engaged and to which he has devoted substantive attention.
  This is what makes the October 2013 beat mechanically real.
- **42 Pa. C.S. § 5525** four-year contract limitations; **13 Pa. C.S. § 2725**
  (UCC) four years from tender of delivery for goods; the Brandt purchase order
  is mixed goods/services and the memo notes the accrual dispute rather than
  resolving it. The Brandt claim expired at the latest in 2015.
- Legal-malpractice limitations in PA: two years (tort, § 5524(7)) / four years
  (contract), with the discovery rule; the demand letter pleads 2024 discovery.
  The firm's response does not rest on limitations — it rests on scope.

## Distractor architecture (155, file `legal-practice-distractors.md`)

Trap classes (details in CAST_AND_TRAP_SHEET.md):
- Same matter number, wrong matter: legacy Aldous & Crane **2011-0284**
  (Glassport Realty Partners — Harrisburg shopping-center refinance).
- Near-miss numbers: 2011-0248 (employment), 2011-0824 (Chapter 11),
  2011-0384 (estate/probate? corporate), 2012-0284 (real estate).
- ~10 other scope-limitation / engagement-amendment confirmations on other
  clients across practice groups.
- **Near-miss twin (inverts the verdict): Danforth Elastomers** — May 25, 2011
  scope carve-out in near-identical words but expressly "for the term of the
  standstill agreement," which ended December 31, 2012; claim later revived,
  missed, and the firm's carrier paid **$610,000** in 2019.
- **Qualified twin: Maunsell Paper Company** — carve-out limited to the claims
  listed on Schedule 1.
- **Inverted premise: Vollmer Foundry** — full-scope engagement, nothing ever
  carved out; the firm docketed and tolled everything.
- **Anti-precedent: Ellard Marine** — 2023 demand; the same journal-archive
  search honestly finds no confirmation; carrier settles **$1,150,000**.
- Right person, wrong matter: Tenniel on other Torvane matters (employment,
  lease, customs?) and, from 2016, as GC of Halbrook Fasteners writing the
  same kind of instruction letter.
- Name collisions: Torvane Marine Group, Torvane Capital Partners, Torvane
  Logistics LLC; Kelling Ridge Apartments; Kelling County IDA; Brandt Paving.
- Adjacent-date collision: a second, unrelated demand against the firm
  (employment matter) in the same week of November 2024.
- DMS-gap resolved-elsewhere: two pre-2014 correspondence gaps recovered by a
  Casebridge cold-restore in 2017 (so "the migration lost it" is not always
  the answer).

## Filler (6,000, seeded)

Port of the shinonome/riverwalk generator CONFIG: ~18 staff with career
windows across five practice groups + admin; ~10 client/counterparty entities
disjoint from signal and distractors; matters as the unit of work with derived
docket numbers in a 4-digit block ≥ 3000 (no collision or substring of any
signal/distractor number); templates: engagement/conflict/billing/prebill,
docketing and limitations ticklers, depositions and discovery, closings,
leases, plan-confirmation, audit-response season (Jan–Mar + Oct), CLE, IT/HR,
adverse slice (past-due AR, write-offs, deadline near-misses caught in time,
declined engagements). ~250 routine mentions of "engagement letter", "scope of
engagement", "statute of limitations", "audit response", "conflict check".
FORBIDDEN tokens: Torvane, Kelling, Brandt, Ridgeline, Tenniel, Pellum,
Stanhope, Brannock, Wisner, 2011-0284, 2011-0248, 2011-0824, 2011-0384,
2012-0284, Danforth, Maunsell, Vollmer, Ellard, Halbrook, Glassport, Garvey,
Caulfield, Copeland Ridge, Hagerman, Ashby, NOV-2119.
(Casebridge/Novarra are permitted era-gated vocabulary — routine IT traffic.)
