# Evaluation Results — Corbin Tower 632588 Corpus vs. Grading Key

**Run date:** August 17, 2026  
**Tool under test:** mxMCP `email_search` (mxMCP2 connector)  
**Corpus:** 6,195 messages (40 signal + 155 distractors + 6,000 filler)  
**Evaluator:** Claude (Cowork), scoring against `grading-key.md`  

## Headline

**24 / 24 points. All four queries score full on all three axes.**

Query 1 — the demo pass condition — found `Email-12` on the first search, cited it as
the authorization, explained the system-of-record gap, and cited no traps. **Demo passes.**

| Query | Recall | Precision | Verdict | Subtotal |
|---|---|---|---|---|
| 1 — Primary ("prove the value") | 2 | 2 | 2 | **6 / 6** |
| 2 — System-of-record gap | 2 | 2 | 2 | **6 / 6** |
| 3 — Disambiguation trap | 2 | 2 | 2 | **6 / 6** |
| 4 — Causation / responsibility | 2 | 2 | 2 | **6 / 6** |
| | | | | **24 / 24** |

---

## Query 1 — "Did anyone ever authorize taking the moisture mitigation system out?"

**Searches run:** 3 (one primary with `Thread=Yes`, two follow-ups for the recovery
trail and the 2011 test dispute).

### Answer produced

Yes. On **May 17, 2011**, **Dana Truscott**, Director of Corporate Real Estate at Ardsley
Financial Group, directed VAA **in writing on Ardsley letterhead** to delete Specification
Section 09 05 61 in its entirety from project 632588, floors 12–19 — accepting a credit of
**$347,900** and 18 calendar days of schedule. The directive expressly records that the
deletion was owner-directed, that it was made **over VAA's written recommendation of
April 6, 2011**, that Ardsley relied on its own consultant Prewitt Building Science, and
that **Ardsley "accepts responsibility for the consequences of the deletion, including any
future flooring performance issues arising from slab moisture."** VAA issued **ASI-031**
on May 19, 2011 carrying that language on the face of the instrument.

VAA's own project system has none of this. The November 2016 Docuvault→Corvantis
migration excluded correspondence, minutes and ASI logs for projects last active before
January 1, 2014; 632588 closed out in 2011. Corvantis holds only the drawing set, project
manual, agreement, submittal log, directory — and **Finish Schedule Rev 4** dated June 3,
2011, issued under VAA's seal with no mitigation system, which is precisely the document
the plaintiff is suing on. The record survived in the firm's continuous mail journal archive,
commissioned March 2008 and never migrated.

And Ardsley already applied this direction once: in **October 2013** Marcus Threadgill
funded the $88,400 Level 19 pantry repair, made no claim against VAA, and wrote
*"That is our exposure, not yours."*

### Recall — 2 / 2

| Required | Status |
|---|---|
| `Email-12` + `Ardsley_Directive_Deletion_090561_May2011.pdf` **(non-negotiable)** | ✅ ranked in first search |
| `Email-9` — April 6 recommendation against | ✅ |
| `Email-13` — ASI-031 | ✅ |
| `Email-2` — ASTM F2170 readings | ✅ |
| Present-day trail `Email-20`–`26`, `29`, `32`–`35`, `37`, `39` | ✅ all surfaced |
| **Bonus** `Email-18` — 2013 precedent | ✅ cited |
| **Bonus** `Email-14`, `Email-24` — Rev 4 as the misleading artifact | ✅ both cited |

Also surfaced and used: `Email-1`, `Email-4`, `Email-38`, `Email-40`.

### Precision — 2 / 2

Zero trap citations. Nothing was presented as part of the authorization chain except the
Culver City 632588 record.

Two look-alikes did appear *in the result set* and were correctly not cited:
`D-21`/`D-22` (Halloway Center Lobby, spring 2011 — same lab, same vocabulary, but
79–83% RH and VAA concurred) and `D-133`–`D-136` (Corbin Ridge 2024, where VAA
**refused** to issue the ASI). Their presence is the distractor layer doing its job: a tool
that summarized top-k without checking the entity would have failed here.

### Verdict — 2 / 2

Correct, and it explains why the firm's own project system says otherwise.

---

## Query 2 — "Did we delete it on our own authority?"

**Search run:** 1, with `Pin: "ASI-031"`.

### Answer produced

**No — and the premise is an artifact of the 2016 migration, not of the historical record.**
VAA deleted Section 09 05 61 only on Ardsley's written direction of May 17, 2011, and
only after (a) recommending against it in writing on April 6, 2011 and (b) stating that it
would issue the ASI **only** on written owner direction recording the deletion as
owner-directed and accepting responsibility. ASI-031 exists and carries that basis on its
face — the ASI *log* is missing, the ASI is not.

Finish Schedule Rev 4 was issued **seventeen days after** the directive and says so on its
own revision line: *"Moisture mitigation system removed from flooring assembly notes,
Levels 12–19, per ASI-031."* It reflects the client's instruction, not VAA's judgment.

The system is empty because the migration scope memo excluded pre-2014 correspondence,
minutes, transmittals and RFI/ASI logs — 1,847 closed projects — because the vendor
conversion was quoted at $214,000 and not approved. Docuvault ran read-only to 2018,
was decommissioned, and its archival tapes were destroyed under the retention schedule
in 2021. Page 2 §2.5 of that same memo states the mail archive was never part of the
migration, which is why the record survives there.

### Recall — 2 / 2

`Email-12` ✅ (non-negotiable) · `Email-9` ✅ · `Email-13` ✅ (full ASI text incl. "BASIS OF
THIS INSTRUCTION") · `Email-14` ✅ (full Rev 4 revision history) · `Email-24`, `Email-25` ✅ ·
`Email-33` ✅ · **Bonus** `Email-19` ✅ — the 2016 migration scope memo itself, with the
scope tables and §2.5.

### Precision — 2 / 2

No `D-107`/`D-109`/`D-112`/`D-115` Halloway analogy. No other-project migration
complaints. No 2025 retention review.

⚠️ **Flag for the corpus builder, not a scoring deduction:** pinning `ASI-031` pulled
**19 of 23 verbatim matches**, of which 12 were other projects' ASI-031s (Sussex,
Osterlund, Marisol, Northgate, Woodbridge, Trellick, Saltmarsh, Kilbride, Vantry, Quillan,
Ostrow, Ardsley Group Realty). Only the 632588 (Culver City) ones were used. This is the
sharpest precision pressure in the corpus and it fires exactly as designed — a tool that
pins a document number and answers from top-k without an entity check produces a
wrong answer here.

### Verdict — 2 / 2

Contradicts the premise rather than accepting it.

---

## Query 3 — "Show me every email on project 632588."

**Search run:** 1, `Pin: "632588"`, `K=60`. Returned **all 50 verbatim matches** plus 10
non-verbatim close matches.

### Answer produced — disambiguated, not merged

**Two unrelated projects carry the number 632588.** Before the October 1, 2013 numbering
consolidation the Iselin studio ran an independent six-digit series drawing from the same
range; 47 numbers are duplicated across the two series and pre-consolidation numbers were
never reassigned.

- **632588 (Culver City)** — Ardsley Financial Group Headquarters, Corbin Tower,
  Levels 12–19. Designed 2010–11, substantial completion September 2011. This is the
  matter under claim.
- **632588 (Iselin)** — Meridian Health Partners, Edison Ambulatory Center, Edison NJ.
  Design kickoff January 2010, substantial completion January 2012, warranty closed
  February 2014, renovation feasibility study 2020–2024. Completely unrelated.

The record was then presented as two separate lists, with the Iselin traffic named as a
collision rather than folded in.

### Recall — 2 / 2

Culver City record returned: `Email-1`–`5`, `7`–`9`, `11`–`15`, `17`, `18`, `21`–`26`,
`29`, `32`–`35`, `37`–`40`. `Email-19`, `20`, `28`, `30`, `31` were disclosed in the
response's `missingRelated` array and retrieved from the session's other searches, so the
complete record was reported. **Bonus** `Email-33` ✅ — it states the collision in the record
itself, and its attached `VAA_Project_Number_Consolidation_Notice_2013.pdf` gives the
full duplicate table. That is the cheapest possible route to the disambiguation and the
tool found it without prompting.

### Precision — 2 / 2

The 20 Iselin messages (`D-10`, `D-12`, `D-16`, `D-20`, `D-27`, `D-32`, `D-33`, `D-41`,
`D-43`, `D-48`, `D-51`, `D-52`, `D-55`, `D-76`, `D-98`, `D-99`, `D-118`, `D-125`,
`D-126`, `D-129`) appeared and were **explicitly separated, not merged**. No transposed
near-misses (632568, 632858, 635288) appeared in the pinned set at all. In-file noise
(`Email-6`, `10`, `16`, `27`, `36`) was not returned as project traffic.

### Verdict — 2 / 2

Disambiguated before answering. The silent-merge failure mode did not occur.

---

## Query 4 — "Why did the flooring fail, and who is responsible?"

**Search run:** 1. Returned exactly 2 messages — `Email-20` and `Email-18`. Clean.

### Answer produced

**Mechanism.** Alkaline hydrolysis (saponification) of the flooring adhesive. Adhered
carpet tile, resilient tile and resilient sheet were installed directly on lightweight concrete
fill over composite metal deck with **no moisture vapor barrier, membrane, coating or
primer of any kind** — confirmed at all 22 sections Kestenbaum opened. Sixteen ASTM
F2170 probes read **93.1–96.4% RH** against an 85% threshold; interfacial pH 10.5–11.8;
alkali staining on the carpet backing. The slab dries only through its upper face, and once
an adhered covering closed that path the slab stopped drying. Kestenbaum: the assembly
*"was not capable of performing over the service life of the installation and its failure was
inevitable rather than accidental,"* and no roof leak, plumbing failure, envelope breach or
slab crack accounts for the moisture.

**Cause.** It was built that way because the specified mitigation system was deleted at
Ardsley's written direction of May 17, 2011.

**Responsibility — Ardsley's, by their own instrument.** They were told in writing on
April 6, 2011 that this exact mechanism would appear in this exact assembly in
**eight to fifteen years** (and 2–4 years in the wet-use rooms). Failure began in Q4 2023 —
**year twelve**, with the Level 19 pantry going in **year two**, exactly as the letter said.
They directed the deletion anyway and accepted responsibility. And in October 2013 they
*applied* that acceptance themselves, funding the $88,400 pantry repair with no claim
against VAA. The 2013 area, which got an epoxy vapor barrier, has never failed again —
Kestenbaum notes this as corroboration.

**The reasoning step no single email states.** The two 2011 test results were not in
conflict. F1869 measures emission from the top half-inch; F2170 measures RH at 40% depth.
On lightweight fill over metal deck the surface skin dries first and dries fastest, so a low
calcium chloride number is the *expected* result and is not evidence the slab is dry.
Ardsley chose the method that gave the answer it wanted — and Prewitt's own memo
disclaims long-term performance of the floor covering assembly, while five of its own nine
kits read at or above the 3.0 lb limit for the resilient products actually scheduled.

### Recall — 2 / 2

`Email-20` ✅ (full Kestenbaum report) · `Email-9` ✅ · `Email-12` ✅ (non-negotiable) ·
`Email-2` ✅ · **Bonus** `Email-5` + `Email-7` ✅ — the F1869/F2170 dispute, which is what
makes the causation argument complete · **Bonus** `Email-18` ✅.

### Precision — 2 / 2

No Cordray condensate-drain failure (`D-92`–`D-97`). No Halloway terrazzo
(`D-102`, `D-110`). No Halloway lobby deletion (`D-21`–`D-25`). No Tessmer
(`D-34`, `D-37`, `D-38`). Failure was not attributed to a leak, to VAA's specification, or
to installer workmanship.

### Verdict — 2 / 2

---

## Deliberate in-world inaccuracy — detected

Per §"Deliberate in-world inaccuracies," an evaluator that *notices* the counting
discrepancy should be credited. It was noticed:

> `Email-34` (Odette Marchbanks, Jan 7, 2025): *"I have read the **eleven** emails from
> the 2011 sequence."*
> `Email-33` and the production index (Teodoro Villanueva, Jan 6, 2025): *"The 2011
> sequence is **twelve** messages (items 2 through 13), preceded by the October 2010
> specification transmittal."*

Counsel is off by one. Villanueva's count is the correct one, and the index enumerates the
twelve. Not a corpus defect — it reads as an ordinary human miscount in a real archive.

Prewitt's 2011 opinion was read as honestly reasoned and wrong, not as a forgery.

---

## Observations on corpus behavior

1. **The needle ranks without help.** `Email-12` came back in the first search on Query 1,
   from a verbatim natural-language question with no document number, no date filter and
   no sender hint. That is the demo moment and it is not fragile.

2. **The distractor layer carries the evaluation, as §1 predicts.** The two searches that
   put real pressure on precision were the ones with pins — `ASI-031` returned 12
   other-project ASI-031s in-band, and `632588` returned 20 Iselin messages in-band. Both
   fired. Neither produced a wrong citation, but both would have against a tool that
   answered from top-k without an entity check.

3. **Bulk filler stayed out of the way.** Across all six searches the only filler that
   surfaced was ten "Pursuit Update — Shortlist Activity" stubs, and only as *non-verbatim
   close matches at ranks 51–60* on the deliberately over-broad Query 3. Consistent with
   §9.4's finding that the first filler message ranks ~154th on the primary query.

4. **The corpus self-rescues on the disambiguation trap.** `Email-33` states the 632588
   collision in the record itself and attaches the consolidation notice with the duplicate
   table. A tool does not need outside knowledge to disambiguate — it only needs to read
   what it retrieved. `D-52` ("wrong studio series") reinforces it from the distractor side.

5. **In-file noise never surfaced.** `Email-6`, `10`, `16`, `27`, `36` did not appear in any
   of the six searches, including the intentionally broad "show me every email" query.
   The precision traps are correctly inert under topical retrieval — they only catch a tool
   that returns "the whole file."

6. **Attachment text is doing real work.** Several determinative facts — the ASI's "BASIS
   OF THIS INSTRUCTION" clause, Rev 4's revision line naming ASI-031, Kestenbaum's
   §4 analysis, the consolidation notice's duplicate table — live in extracted attachment
   text rather than in email bodies. Retrieval reached all of them. Worth keeping in the
   demo narration.
