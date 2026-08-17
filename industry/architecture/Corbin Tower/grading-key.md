# Demo Grading Key — Corbin Tower 632588 Interiors + Architecture Corpus

Use this to score a live AI-chat demo objectively. The corpus is the
**40-email signal thread** (`corbin-tower-632588.md`) plus the **155 hard-negative
distractors** (`architecture-distractors.md`), salted into 6,000 emails of bulk
filler (`architecture-bulk-filler.md`). Total 6,195 messages.

A correct answer is judged on three axes:

1. **Recall** — did it surface the specific signal emails and attachments it needed?
2. **Precision** — did it *avoid* the look-alikes? The collision axes are the
   **document number ASI-031** (16 other projects carry one), the **project number
   632588** (two unrelated projects share it), the **client name Ardsley** (four
   unrelated entities), the **building name Corbin** (three unrelated entities),
   and the **subject matter** — six other moisture-mitigation deletion threads,
   each of which resolves differently.
3. **Verdict** — is the final natural-language answer correct, especially where the
   firm's own project system alone would mislead?

Unprefixed IDs (e.g. `Email-12`) refer to `corbin-tower-632588.md`.
IDs prefixed `D-` refer to `architecture-distractors.md`.

**This file must never be ingested into the corpus.** The indexer takes only
`corbin-tower-632588.md` from the signal folder. A `*.md` glob puts the answer key
in the searchable archive and every subsequent evaluation is worthless.

---

## Signal reference map

| ID | What it is | Role |
|---|---|---|
| Email-1 | Oct 14, 2010 — Section 09 05 61 issued with the 100% CD set, 142,000 SF, 85% RH threshold | Supporting |
| Email-2 | Feb 8, 2011 — Callenbach ASTM F2170 report: 92.1–96.4% RH across 14 probes | The causation seed |
| Email-4 | Mar 2, 2011 — Thackston Bell SR-014, priced at Ardsley's request, $347,900 credit and 18 days | Supporting |
| Email-5 | Mar 9, 2011 — Prewitt's calcium chloride memo, 2.9–3.4 lb, "mitigation not required" | The trap the tool must overcome |
| Email-7 | Mar 15, 2011 — Ashcombe's rebuttal: F1869 reads the top half inch, F2170 reads the slab | Causation |
| Email-9 | Apr 6, 2011 — VAA's formal written recommendation **against** deletion, predicting adhesive failure in eight to fifteen years in the office areas and two to four in the wet-use rooms, and refusing to issue the ASI absent written owner direction | Supporting / the obligation |
| Email-11 | May 5, 2011 — Kilcoyne: the allowance is exhausted, the 18 days matter more than the money | Supporting |
| **Email-12** | **May 17, 2011 — Dana Truscott's written directive: "Ardsley Financial Group directs VAA to delete Section 09 05 61 in its entirety… Ardsley acknowledges that this is an owner-directed deletion made over VAA's written recommendation of April 6, 2011… Ardsley accepts responsibility for the consequences of the deletion, including any future flooring performance issues arising from slab moisture." Attachment `Ardsley_Directive_Deletion_090561_May2011.pdf`** | **THE needle** |
| Email-13 | May 19, 2011 — ASI-031 issued on that written direction, owner-direction language on its face | The formal instrument |
| Email-14 | Jun 3, 2011 — Finish Schedule Rev 4, the document the current system holds and the plaintiff's exhibit | The trap the tool must overcome |
| Email-15 | Aug 26, 2011 — installer notes the adhesive warranty drops to 5 years with a moisture exclusion | Supporting |
| Email-17 | Sep 17, 2013 — Level 19 pantry flooring lifting, 94% RH at depth | Precedent setup |
| **Email-18** | **Oct 8, 2013 — Marcus Threadgill (Ardsley risk) applies the 2011 direction, funds the $88,400 repair, makes no claim against VAA, and predicts the rest of Levels 12–19 will fail: "That is our exposure, not yours."** | **Precedent** |
| Email-19 | Nov 9, 2016 — Corvantis migration: correspondence, minutes and the ASI log excluded for projects last active before Jan 1, 2014 | Cross-year link |
| Email-20 | Oct 30, 2024 — Ardsley's notice with the Kestenbaum forensic report, 93–96% RH, no vapor barrier found | Present-day thread start |
| Email-21 | Nov 12, 2024 — Hollingsworth Vane demand, **$2,150,000**, resting on Finish Schedule Rev 4 | Causation |
| Email-24 | Nov 14, 2024 — Corvantis holds no correspondence, no ASI log; the firm's own record is the plaintiff's best exhibit | The trap the tool must overcome |
| Email-25 | Nov 15, 2024 — why: the 2016 migration scope; Docuvault decommissioned, tapes destroyed 2021 | The trap the tool must overcome |
| Email-26 | Nov 18, 2024 — everyone who negotiated it has left; Ashcombe retired 2019, Okonkwo left 2015, Truscott retired 2018 | Supporting |
| Email-29 | Nov 25, 2024 — defense counsel: without a contemporaneous writing there is no defense | Causation |
| Email-31 | Dec 5, 2024 — the GC's records were destroyed at the 2019 acquisition; "there was a letter" | Supporting |
| Email-32 | Dec 18, 2024 — the question nobody asked for five weeks: was the *mail archive* in the migration? | Product setup |
| **Email-33** | **Jan 6, 2025 — the mail archive was never in scope, is continuous back to March 2008, and produces the April 6 letter, the May 17 directive and ASI-031. Also warns that 632588 returns two projects.** | **The product moment** |
| Email-34 | Jan 7, 2025 — counsel's assessment: "that is not a firm that breached the standard of care, that is a firm that met it and was overruled" | Formal rebuttal |
| Email-35 | Jan 9, 2025 — the 2013 sequence recovered; Ardsley already applied the direction once | Precedent recovery |
| Email-37 | Jan 21, 2025 — production letter to Hollingsworth Vane, all four documents | Formal rebuttal |
| Email-38 | Feb 3, 2025 — authentication: original headers, unbroken custody since 2008, two independent VAA-side journal copies of each determinative message | Supporting |
| **Email-39** | **Feb 21, 2025 — Ardsley withdraws the claim in its entirety; the $2,150,000 demand is withdrawn** | **Outcome** |
| Email-40 | Mar 6, 2025 — Northmark closes claim NMD-C-24-2207, indemnity $0, defense cost $61,400, not chargeable | Outcome |

**Full 2010–2011 trail:** Email-1 – Email-5, Email-7 – Email-9, Email-11 – Email-15.
**Full 2013 trail:** Email-17 – Email-18.
**Full present-day trail:** Email-20 – Email-26, Email-28 – Email-35, Email-37 – Email-40.

**In-file noise that is NOT part of any trail:** Email-6 (chapter design awards
submissions, March 2011), Email-10 (Revit workstation refresh, April 2011),
Email-16 (Iselin studio relocation, June 2012), Email-27 (open enrollment,
November 2024), Email-36 (healthcare interiors photography, January 2025).
Citing any of these as part of the claim record is a precision failure.

---

## Deliberate in-world inaccuracies — do NOT grade as corpus defects

**1. Counsel miscounts the 2011 sequence.** In Email-34, Odette Marchbanks writes
"I have read the **eleven** emails from the 2011 sequence." The 2011 sequence is
**twelve** messages (Email-2 through Email-5, Email-7 through Email-9, Email-11
through Email-15), preceded by the October 2010 specification transmittal
(Email-1). Teodoro Villanueva states the correct count in Email-33 and in the
production index. Real archives contain human counting errors. An evaluator that
*notices the discrepancy and reports it* is exhibiting correct behavior and should
be credited, not penalized. An evaluator that repeats "eleven" as fact has simply
copied counsel and loses nothing.

**2. Prewitt's 2011 opinion is wrong but honestly reasoned.** Email-5 and its memo
are technically defensible on their own terms and were relied on in good faith.
They are not a forgery and should not be read as one.

---

## Query 1 — Primary ("prove the value")

> *"We're being sued for two point one five million over the flooring at the Ardsley
> headquarters at Corbin Tower. Did anyone ever authorize taking the moisture
> mitigation system out of that job, and if so who?"*

**Correct verdict:** Yes. On **May 17, 2011**, **Dana Truscott**, Ardsley Financial
Group's Director of Corporate Real Estate, directed VAA **in writing, on Ardsley
letterhead**, to delete Specification Section 09 05 61 in its entirety from project
632588, accepting a credit of **$347,900** and 18 calendar days of schedule. The
directive expressly records that the deletion was **owner-directed**, that it was
made **over VAA's written recommendation of April 6, 2011**, that Ardsley relied on
its own consultant Prewitt Building Science, and that **Ardsley accepts
responsibility for future flooring performance issues arising from slab moisture**.
VAA issued **ASI-031** on May 19, 2011 carrying that language on its face.

The answer must also state the system-of-record gap: **VAA's project information
system has no record of any of this.** The 2016 Docuvault-to-Corvantis migration
excluded correspondence, minutes and the ASI log for projects last active before
January 1, 2014, and project 632588 closed out in 2011. All Corvantis holds is
Finish Schedule Rev 4 dated June 3, 2011, issued under VAA's seal and showing no
mitigation system — which is precisely the document the plaintiff is suing on. The
documents were recovered from the firm's continuous mail journal archive, which was
never part of that migration.

**MUST cite (recall):**

- `Email-12` — the May 17, 2011 Truscott directive and its attachment **(non-negotiable)**
- `Email-9` — VAA's April 6, 2011 written recommendation against the deletion
- `Email-13` — ASI-031, the instrument issued on that direction
- `Email-2` — the ASTM F2170 readings that made the system necessary
- The present-day trail: `Email-20` – `Email-26`, `Email-29`, `Email-32` – `Email-35`, `Email-37`, `Email-39`
- **Bonus (full credit):** `Email-18` — Ardsley already honored the direction once, funding the 2013 pantry repair at $88,400 and making no claim
- **Bonus (full credit):** `Email-14` and `Email-24` — naming Finish Schedule Rev 4 as the misleading system-of-record artifact

**MUST NOT cite (precision fails):**

- Any **other ASI-031** — sixteen other VAA projects carry one:
  `D-7`, `D-8`, `D-17`, `D-28`, `D-45`, `D-53`, `D-62`, `D-64`, `D-85`, `D-91`,
  `D-100`, `D-117`, `D-121`, `D-128`, `D-132`, `D-138`
- **The near-miss twin** — Halloway Center Lobby, spring 2011, same vocabulary, same
  testing lab, same peer reviewer, but the readings came back at 79–83% RH, VAA
  *concurred* with the deletion, and no acceptance of responsibility was ever given
  because none was needed: `D-21` – `D-25`. This is the closest look-alike in the
  corpus and citing it as the authorization is a hard precision failure.
- **The qualified twin** — Delmarco Culver Hotel, where an owner-directed deletion
  *was* accepted in writing but **only for Phase 1 floors 3–8 and only for the 2014
  season**, and Section 09 05 61 was reinstated in full for Phase 2:
  `D-54`, `D-56`, `D-57`, `D-63`, `D-66` – `D-68`, `D-71`, `D-80`
- **The inverted premise** — Tessmer Biosciences, where the mitigation system was
  never specified at all because the slab is on grade over a 15-mil retarder, so
  nothing was ever deleted: `D-34`, `D-37`, `D-38`
- **The anti-precedent** — Halloway Center Trust's 2021 terrazzo claim, where VAA
  also blamed the 2016 migration, the mail archive *was* searched, **no directive
  existed**, and the claim settled against VAA at $470,000:
  `D-102`, `D-104`, `D-105`, `D-107`, `D-109`, `D-110`, `D-112`, `D-113`, `D-115`
- **The refusal** — Corbin Ridge Business Park, 2024, where VAA declined to issue an
  ASI deleting Section 09 05 61 because the owner would not put an acceptance in
  writing: `D-133` – `D-136`
- Any **project 632588 (Iselin series)** message — a different job entirely:
  `D-10`, `D-12`, `D-16`, `D-20`, `D-27`, `D-32`, `D-33`, `D-41`, `D-43`, `D-48`,
  `D-51`, `D-52`, `D-55`, `D-76`, `D-98`, `D-99`, `D-118`, `D-125`, `D-126`, `D-129`
- Any **Ardsley or Corbin name collision** — Ardsley Park Medical Center, Ardsley
  Commons, Ardsley Group Realty, Corbin Center, Corbin Ridge:
  `D-13`, `D-15`, `D-19`, `D-30`, `D-44`, `D-46`, `D-49`, `D-65`, `D-74`, `D-78`,
  `D-88`, `D-95`, `D-101`, `D-106`, `D-111`, `D-116`, `D-120`, `D-124`, `D-131`,
  `D-152`
- **Right person, wrong project** — Dana Truscott and Bernard Kilcoyne on the
  Ardsley Pasadena Regional Office: `D-35`, `D-36`, `D-39`, `D-42`, `D-47`, `D-58`
- In-file noise framed as part of the claim record: `Email-6`, `Email-10`,
  `Email-16`, `Email-27`, `Email-36`

**Scoring:** Cites `Email-12` **and** answers "yes, the client directed it in writing
and accepted responsibility" = pass. Misses `Email-12`, or answers "no authorization
was ever given" / "the architect removed it" = fail. Any trap citation presented as
part of the authorization chain = precision deduction.

---

## Query 2 — The system-of-record gap

> *"Our project system has no ASI log for 632588 and the finish schedule we issued
> in June 2011 shows no moisture mitigation. Did we delete it on our own authority?"*

**Correct verdict:** No. The premise is an artifact of the 2016 migration, not of
the historical record. VAA deleted Section 09 05 61 **only** on Ardsley's written
direction of May 17, 2011, and only after recommending against it in writing on
April 6, 2011 and stating that it would not issue the ASI without written owner
direction accepting responsibility. Finish Schedule Rev 4 was issued **seventeen
days after** the directive and reflects the client's instruction, not VAA's
judgment. The reason the system looks otherwise is that the Docuvault-to-Corvantis
migration excluded correspondence, minutes and ASI logs for projects last active
before January 1, 2014, Docuvault was decommissioned in 2018 and its tapes were
destroyed in 2021. The record survives in the mail archive, which was never
migrated. A correct answer must contradict the premise rather than accept it.

**MUST cite (recall):**

- `Email-12` — the written direction **(non-negotiable)**
- `Email-9` — the condition VAA placed on issuing the ASI
- `Email-13` — ASI-031, which exists even though the ASI log does not
- `Email-14` — Rev 4 issued after, and because of, the directive
- `Email-24`, `Email-25` — why the system is empty
- `Email-33` — where the record actually was
- **Bonus (full credit):** `Email-19` — the 2016 migration scope memo itself

**MUST NOT cite (precision fails):**

- `D-107`, `D-109`, `D-112`, `D-115` — the Halloway anti-precedent, where the same
  "lost in the migration" argument was made, the archive was searched, and **nothing
  was found**. Reasoning by analogy from that matter to this one produces the wrong
  verdict.
- `D-75`, `D-76`, `D-99`, `D-118`, `D-125` — other projects' migration complaints
- `D-148` – `D-151` — the unrelated 2025 records-retention review
- Concluding "there is no record, so it never happened", or "VAA deleted it without
  authorization", is a **verdict fail** regardless of what was cited.

---

## Query 3 — The disambiguation trap

> *"Show me every email on project 632588."*

The corpus contains **two projects numbered 632588 by design**. Before the October
2013 numbering consolidation the Iselin studio ran an independent six-digit series,
so **632588 (Culver City)** is the Ardsley headquarters at Corbin Tower and
**632588 (Iselin)** is Meridian Health Partners' Edison Ambulatory Center. There are
also three transposed-digit near misses in daily use: 632568, 632858 and 635288.

**Correct behavior:** either scope to the Ardsley matter from conversation context,
or explicitly report that two unrelated projects share the number and disambiguate
before answering. **Silently merging them is a failure even if the Ardsley emails
are all present.**

**MUST cite (recall):**

- The Culver City 632588 record: `Email-1` – `Email-5`, `Email-7` – `Email-9`,
  `Email-11` – `Email-15`, `Email-17`, `Email-18`, `Email-20` – `Email-26`,
  `Email-28` – `Email-35`, `Email-37` – `Email-40`
- **Bonus (full credit):** `Email-33`, which states the collision in the record
  itself and is the cheapest way for a tool to discover it

**MUST NOT cite (precision fails):**

- Any **632588 (Iselin)** message: `D-10`, `D-12`, `D-16`, `D-20`, `D-27`, `D-32`,
  `D-33`, `D-41`, `D-43`, `D-48`, `D-51`, `D-52`, `D-55`, `D-76`, `D-98`, `D-99`,
  `D-118`, `D-125`, `D-126`, `D-129`
- **632568** — Ardsley Park Medical Center Imaging Suite: `D-13`, `D-19`, `D-44`,
  `D-74`, `D-120`
- **632858** — Corbin Center Owners Association Lobby: `D-15`, `D-30`, `D-46`,
  `D-88`, `D-124`
- **635288** — Ardsley Commons Building C Interiors: `D-49`, `D-131`
- In-file noise, which is in the signal file but is not project traffic:
  `Email-6`, `Email-10`, `Email-16`, `Email-27`, `Email-36`

**Scoring:** Disambiguates or scopes correctly = pass. Returns a merged set spanning
both projects without noting the collision = fail on precision **and** verdict, even
if recall is complete.

---

## Query 4 — Causation / responsibility

> *"Why did the flooring at Corbin Tower fail, and who is responsible for it?"*

**Correct verdict:** It failed because the adhered flooring on Levels 12–19 was
installed directly over lightweight concrete fill on metal deck at 92–96% relative
humidity with **no moisture vapor barrier**, causing alkaline hydrolysis of the
adhesive. It was installed that way because the specified mitigation system was
deleted at Ardsley's written direction. Responsibility is Ardsley's, and it is
Ardsley's by their own instrument: they were told in writing on April 6, 2011 that
this exact failure would appear in **eight to fifteen years** — it appeared in year
twelve — they directed the deletion anyway on May 17, 2011 accepting responsibility,
and they applied that acceptance themselves in October 2013 by funding the Level 19
pantry repair at $88,400 and expressly making no claim against VAA.

The reasoning step no single email states: the two 2011 test results were not in
conflict. ASTM F1869 reads the top half inch of slab and reads low on a substrate
that dries from one face; ASTM F2170 reads the slab at depth. Ardsley chose the
method that gave the answer it wanted, and its own consultant's memo disclaims
long-term performance.

**MUST cite (recall):**

- `Email-20` — the Kestenbaum forensic finding: no vapor barrier, 93–96% RH,
  alkaline hydrolysis
- `Email-9` — the prediction of this failure in this assembly in eight to fifteen years
- `Email-12` — the directive that caused it **(non-negotiable)**
- `Email-2` — the 2011 readings
- **Bonus (full credit):** `Email-5` and `Email-7` — the F1869 versus F2170 dispute,
  which is what makes the causation argument complete
- **Bonus (full credit):** `Email-18` — Ardsley's own 2013 application of the direction

**MUST NOT cite (precision fails):**

- `D-92`, `D-93`, `D-94`, `D-96`, `D-97` — the Cordray Wealth Management flooring
  failure, where Section 09 05 61 *was* installed and the cause was a **failed
  condensate drain**. Attributing the Corbin Tower failure to a leak, a roof or a
  plumbing failure is a verdict fail.
- `D-102`, `D-110` — the Halloway terrazzo failure, which VAA specified itself
- `D-21` – `D-25` — the Halloway lobby deletion, where the readings were *below* the
  threshold and deletion was appropriate
- `D-34`, `D-37`, `D-38` — Tessmer, where no mitigation system ever existed to delete
- Attributing the failure to VAA's specification, to installer workmanship, or to a
  building water intrusion event is a **verdict fail**.

---

## Quick scoring rubric (per query)

| Axis | Full (2) | Partial (1) | Fail (0) |
|---|---|---|---|
| **Recall** | All required IDs plus the key attachment | Misses a supporting email but has the core needle | Misses `Email-12` / the core needle |
| **Precision** | Zero trap citations | 1 minor look-alike, not presented as the answer | Cites another ASI-031, the other 632588, a name collision, or another project's deletion decision as the authorization |
| **Verdict** | Correct **and** explains the system-of-record gap | Correct but shallow — finds the directive, does not explain why the project system disagrees | Wrong (e.g. "no authorization was found", "VAA deleted it on its own", "the failure was caused by a leak") |

**Arithmetic:** 4 queries × 3 axes × 2 points = **24 points available**.

**Demo passes** when Query 1 scores full on all three axes: it finds the one
historical email out of 6,195, ignores sixteen other ASI-031s and six other
moisture-deletion threads, and returns the answer the firm's own project system
would get wrong.
