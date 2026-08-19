# Demo Grading Key — Marchwood 2011-0447 Securities Regulation Corpus

Use this to score a live AI-chat demo objectively. The corpus is the
**40-email signal thread** (`marchwood-0447.md`) plus the **155 hard-negative
distractors** (`securities-regulation-distractors.md`), salted into **6,000
bulk-filler messages** (`securities-regulation-bulk-filler.md`).

A correct answer is judged on three axes:

1. **Recall** — did it surface the specific signal emails and attachments it needed?
2. **Precision** — did it *avoid* the look-alike traps (a second examination
   numbered 2011-0447, five firms named Marchwood, a near-identical undertaking
   two days earlier at a different adviser, the same author writing the same kind
   of letter for a different employer)?
3. **Verdict** — is the final natural-language answer correct, especially where
   the Commission's own examination system alone would mislead?

Unprefixed IDs (e.g. `Email-11`) refer to `marchwood-0447.md`.
IDs prefixed `D-` refer to `securities-regulation-distractors.md`.

**This file must never be ingested into the corpus.** The indexer takes only
`marchwood-0447.md` from the signal folder.

---

## Signal reference map

| ID | What it is | Role |
|---|---|---|
| Email-1 | Feb 7, 2011 — notice of examination 2011-0447 and initial document request, items 9 and 11 aimed at fee billing and withdrawal authority | Supporting |
| Email-2 | Mar 9, 2011 — badge reader replacement on the north corridor | In-file noise |
| Email-3 | Mar 18, 2011 — preliminary custody analysis; Section 6(c) across 214 of 1,140 accounts, ~$198m; the (b)(3) exception is unavailable because the authority is not confined to the fee | The causation seed |
| Email-4 | Apr 20, 2011 — the deficiency letter, six items, Item 4 custody | Supporting |
| Email-5 | Apr 26, 2011 — counsel requests a two-week extension | Supporting |
| Email-6 | Apr 28, 2011 — extension granted to June 3; "the staff is looking for a description of what Marchwood is going to do, in writing" | Supporting |
| Email-7 | May 19, 2011 — interim response on Items 1, 2, 3, 5 and 6; Item 4 disputed | Supporting |
| Email-8 | May 24, 2011 — staff position on Item 4 and on Rule 206(4)-2(b)(3) | Supporting |
| Email-9 | May 26, 2011 — internal: take an undertaking with no end date, not a remediation scoped to the examined year, because the firm grows by acquisition | The causation seed |
| Email-10 | Jun 1, 2011 — call memorandum; the three elements the registrant agreed to | Supporting |
| Email-11 | **Jun 2, 2011 — Vasseur-Kyle accepts Item 4, moves 214 accounts to Signal Peak, discontinues the practice firm-wide, undertakes to apply the same treatment to accounts acquired or onboarded in future, "not limited to calendar year 2010 or to any other period and given without an expiration date," and asks the staff to treat the letter as the commitment on which closing is conditioned.** Attachment `Marchwood_Undertaking_Letter_2011-06-02.pdf` | **THE needle** |
| Email-12 | Jun 7, 2011 — closing recommendation; disposition **C-4**, not C-2, plus a follow-up flag | Causation |
| Email-13 | Jun 28, 2011 — the closing letter. The only 2011 document that survived into SENTRY, and on its face the respondent's best evidence | The trap the tool must overcome |
| Email-14 | Sep 14, 2011 — agency-wide suspension of records destruction; the journal copy is the retention copy | Cross-year link |
| Email-15 | Sep 19, 2013 — fall continuing professional education registration | In-file noise |
| Email-16 | **Oct 21, 2013 — Marchwood applies the 2011 undertaking to the 61 accounts acquired from Hollis Grange, unprompted, with no examination open, and pays for a surprise examination covering an eleven-day exposure** | **Precedent** |
| Email-17 | Oct 29, 2013 — national numbering from November 1; legacy four-digit numbers are not renumbered, so Philadelphia's 2011-0447 and Denver's 2011-0447 are different examinations | The trap the tool must overcome |
| Email-18 | Feb 12, 2016 — Vasseur-Kyle leaves Marchwood; Sczerbiak takes over March 1 | Cross-year link |
| Email-19 | Mar 11, 2016 — EXAMTRAC to SENTRY cutover; pre-2014 correspondence, work papers and follow-up flags did not migrate | The trap the tool must overcome |
| Email-20 | Apr 14, 2016 — SENTRY has no C-4; the code was mapped to C-2 on exactly the examinations whose correspondence also did not migrate | Causation |
| Email-21 | Apr 14, 2016 — SENTRY-2214 closed low impact, will not fix | Causation |
| Email-22 | Aug 15, 2019 — Marchwood falls off the FY2020 candidate list; the model is behaving correctly on inputs that include "closed with no further action and no open items of record" | Causation |
| Email-23 | Nov 7, 2019 — FOIA request F-2020-00318 concerning Cardiff Meridian Funds Trust | In-file noise |
| Email-24 | Mar 2, 2023 — TCR-2023-0416022; a former employee reports the practice and says she was told the SEC had reviewed it | Supporting |
| Email-25 | Sep 12, 2023 — referral to Enforcement; 431 accounts, ~$497m; "I cannot tell you whether we missed it in 2011 or it came back" | Supporting |
| Email-26 | Feb 8, 2024 — order instituting proceedings, AP File No. 3-21987 | Present-day thread start |
| Email-27 | Jul 18, 2024 — Marchwood Capital Partners LP Form PF delinquency; four unrelated firms share the name | In-file noise |
| Email-28 | Nov 12, 2024 — respondent's motion for summary disposition on the Division's own production, plus notice of an EAJA claim; $4,300,000 at issue | The trap the tool must overcome |
| Email-29 | Nov 14, 2024 — "I need the complete 2011-0447 file"; the closing-letter recital is a hole with a label on it | Supporting |
| Email-30 | Nov 15, 2024 — SENTRY holds a summary row coded C-2 and the closing letter. That is the entire file, and it is evidence of what survived a migration | The trap the tool must overcome |
| Email-31 | Nov 21, 2024 — everyone who negotiated it has left; prior counsel dissolved in 2018 | Supporting |
| Email-32 | Dec 9, 2024 — OGC assessment: on this record the motion is strong and $4,300,000 is at risk | Supporting |
| Email-33 | Jan 8, 2025 — Records Management: the correspondence was never destroyed; it is in the mail journal archive, which never migrated | The product moment |
| Email-34 | Jan 14, 2025 — journal archive search results; twelve messages from the 2011 sequence and one from October 2013, with attachments intact | The product moment |
| Email-35 | Jan 16, 2025 — the June 2, 2011 letter quoted verbatim | Supporting |
| Email-36 | Jan 17, 2025 — the October 2013 letter surfaces from the same index | Precedent |
| Email-37 | Jan 22, 2025 — supplemental production served; documents 3, 10 and 13 | Supporting |
| Email-38 | Feb 3, 2025 — the Division's opposition; the undertaking, its lack of an end date, and the respondent's own 2013 performance of it | Formal rebuttal |
| Email-39 | Feb 21, 2025 — motion, EAJA notice and forum challenge all withdrawn; offer of settlement | Outcome |
| Email-40 | Mar 14, 2025 — settled order: censure, cease and desist, $1,412,000 + $137,000 + $601,000 = **$2,150,000**, and the post-mortem on why nobody knew | Outcome |

**Full 2011 examination trail:** Email-1, Email-3 – Email-13.
**Full 2013 precedent trail:** Email-16 – Email-17.
**Full migration and causation trail:** Email-18 – Email-22.
**Full present-day trail:** Email-24 – Email-26, Email-28 – Email-40.

**In-file noise that is NOT part of any trail:** Email-2 (building notice),
Email-15 (CPE registration), Email-23 (a FOIA request about an unrelated
registrant), Email-27 (Marchwood *Capital Partners LP*, a different firm with
a different file number in a different state).

**Deliberate in-world inaccuracy — do NOT grade as a corpus defect:**
Email-37 describes the supplemental production as comprising "the eleven emails
from the 2011 examination sequence." The sequence is **twelve**. Email-34 and the
production index both state it correctly, as does the Division's opposition
("that letter, and eleven other documents from the 2011 examination"). Real
productions contain human miscounts. An evaluator that notices the discrepancy
and reports it is behaving correctly and should be credited, not penalized.

---

## Query 1 — Primary ("prove the value")

> *"Did Marchwood ever agree in writing to stop debiting advisory fees directly
> from client accounts, or did the 2011 examination close with no findings?"*

**Correct verdict:** Yes, in writing, on **June 2, 2011**. Marchwood's chief
compliance officer Marguerite Vasseur-Kyle wrote to examiner Desmond Whitlatch
accepting Item 4 of the staff's April 20, 2011 deficiency letter in examination
2011-0447, confirming that all 214 affected accounts had been transferred to
Signal Peak Trust Company effective June 1, 2011 under agreements giving
Marchwood no withdrawal authority, stating that the practice had been
discontinued firm-wide and "we will not resume it," and undertaking to apply the
same treatment to any accounts acquired or onboarded in future — an undertaking
expressly "not limited to calendar year 2010 or to any other period and given
without an expiration date." The letter asks the staff to treat it as the
commitment on which the closing of the examination is conditioned, and the
closing letter of June 28, 2011 does exactly that: "based on the corrective
actions described in your response."

The answer must also state **why the Commission's own system says otherwise**:
the 2016 EXAMTRAC-to-SENTRY migration carried only the summary record and the
indexed final letters for examinations closed before January 1, 2014, and mapped
the legacy disposition code C-4 (closed on registrant undertaking) onto C-2
(closed, no further action). SENTRY therefore shows an examination that closed
with no further action and holds no deficiency letter, no response and no
undertaking. That is a record of what survived a migration, not a record of what
happened.

**MUST cite (recall):**

- `Email-11` — the undertaking, with `Marchwood_Undertaking_Letter_2011-06-02.pdf` (non-negotiable)
- `Email-4` — the deficiency letter that Item 4 comes from
- `Email-13` — the closing letter, and its "based on the corrective actions described in your response"
- `Email-30` — what SENTRY actually holds
- `Email-19` — why it holds only that
- `Email-34` — the journal archive recovery
- `Email-35` — the letter quoted verbatim
- **Bonus (full credit):** `Email-16` and `Email-36` (the 2013 precedent — the firm applied the undertaking itself, unprompted), `Email-9` (why the staff wanted an open-ended undertaking), `Email-12` (the C-4 recommendation), `Email-38` (the rebuttal that ties it together)

**MUST NOT cite (precision fails):**

- **The near-miss twin** — Vandergrift Rowe Investment Counsel, examination
  2011-0463, Philadelphia, same branch chief, same examiner, custody at Item 4,
  and an undertaking letter dated **May 31, 2011** in almost the same words:
  `D-5`, `D-8`, `D-10`, `D-16`, `D-17`, `D-19`, `D-24`, `D-25`, `D-26`, `D-29`,
  `D-39`, `D-54`, `D-55`, `D-112`, `D-140`, `D-142`, `D-147`. `D-25` is the
  closest look-alike in the corpus and citing it as the undertaking inverts the
  verdict, because it expired by its terms on December 31, 2012.
- **The other 2011-0447** — Denver's advertising and performance-presentation
  examination of Braxton-Ferrer Advisors LLC: `D-3`, `D-4`, `D-20`, `D-27`,
  `D-33`, `D-94`, `D-95`, `D-123`, `D-124`, `D-129`, `D-138`, `D-141`
- **The qualified twin** — Ellersby Kinnaird Advisors, whose undertaking is
  limited to the accounts in Schedule A: `D-46`, `D-50`, `D-51`, `D-119`, `D-120`
- **The inverted premise** — Corrigan Weld Asset Management, which billed by
  invoice throughout and undertook nothing because nothing was required:
  `D-57`, `D-58`, `D-59`, `D-61`, `D-62`, `D-63`, `D-64`, `D-76`, `D-91`,
  `D-143`, `D-146`
- **Right person, wrong employer** — Marguerite Vasseur-Kyle writing in the same
  voice from Everly Sound Advisors about a books-and-records finding: `D-81`,
  `D-82`, `D-84`, `D-85`, `D-86`, `D-90`
- **Name collisions** — Marchwood Capital Partners LP, Marchwood Wealth Advisors,
  Marchwood Securities LLC, Marchwood Fiduciary Services LLC, Hollis Grange
  Municipal Advisors: `D-41`, `D-52`, `D-65`, `D-66`, `D-69`, `D-70`, `D-71`,
  `D-73`, `D-75`, `D-78`, `D-89`, `D-96`, `D-102`, `D-105`, `D-108`, `D-116`,
  `D-127`, `D-144`, `D-153`
- **In-file noise framed as part of the matter** — `Email-2`, `Email-15`,
  `Email-23`, `Email-27`

**Scoring:** Cites `Email-11` **and** reaches the "yes, in writing, and the
system is wrong because of the migration" conclusion = pass. Misses `Email-11`,
or answers "the examination closed with no findings" = fail. Any trap citation is
a precision deduction; citing `D-25` as the undertaking is a precision **and** a
verdict failure.

---

## Query 2 — The system-of-record gap

> *"Our examination file for Marchwood shows disposition C-2, closed no further
> action, and a closing letter, and nothing else. Did the staff ever require
> corrective action from this firm?"*

**Correct verdict:** The premise is false and the tool must say so. The staff
issued a six-item deficiency letter on April 20, 2011 and closed the examination
on a written undertaking, recording it as **C-4 — closed on registrant
undertaking**. What the system now shows is the result of two separate 2016
defects: correspondence and work papers for examinations closed before January 1,
2014 were out of scope for the SENTRY migration, and the legacy C-4 code had no
counterpart in the new code set and was mapped onto C-2. The distinction was
raised at the time, logged as SENTRY-2214, and closed "low impact, will not fix."
The absence of a deficiency letter from SENTRY is not evidence that none was
issued.

**MUST cite:** `Email-30` (primary), `Email-19`, `Email-20`, `Email-21`,
`Email-4`, `Email-11`, `Email-12`. **Bonus:** `Email-13`, `Email-33`, `Email-34`.

**MUST NOT cite:** `D-79`, `D-80` (a different pre-2014 SENTRY gap, on 2011-0392,
which an EXAMTRAC restore resolved); `D-100`, `D-101` (a broker-dealer file, same
question, different answer); `D-104`, `D-106` (a C-4 record on a different
examination); `D-118`, `D-152` (other gap resolutions); `D-126`, `D-132`,
`D-134`, `D-135`, `D-136`, `D-139`, `D-145` (Ottoway Trask, where the same search
correctly returned nothing). Concluding "no corrective action was ever required"
is a verdict failure regardless of what was cited.

---

## Query 3 — The disambiguation trap

> *"Show me every email on examination 2011-0447."*

The corpus contains **two examinations numbered 2011-0447 by design**. Philadelphia's
is Marchwood Asset Management (custody). Denver's is Braxton-Ferrer Advisors LLC
(advertising and performance presentation). The legacy four-digit series was run
independently by each regional office until the national scheme took effect on
November 1, 2013, and the legacy numbers were never renumbered — `Email-17` says
so explicitly. Three transposed near-misses are also in daily use: 2011-0477,
2011-0417 and 2010-0447.

**Correct behavior:** either scope to Marchwood from conversation context, or
explicitly note that two examinations share the number and disambiguate by office
and registrant — **never silently merge them**.

**MUST cite (the Philadelphia 2011-0447 set):** `Email-1`, `Email-3` – `Email-13`.
**Bonus:** the later messages that name the number — `Email-17`, `Email-25`,
`Email-29`, `Email-30`, `Email-34`, `Email-37`, `Email-38`.

**MUST NOT cite:**

- Denver's 2011-0447 (Braxton-Ferrer): `D-3`, `D-4`, `D-20`, `D-27`, `D-33`,
  `D-94`, `D-95`, `D-123`, `D-124`, `D-129`, `D-138`, `D-141`
- Boston's 2010-0447 (Wexford Trelaine): `D-1`, `D-2`, `D-92`, `D-93`
- Fort Worth's 2012-0447 (Salomé Ridge): `D-42`, `D-49`, `D-103`, `D-117`, `D-125`
- The transpositions 2011-0417 and 2011-0477: `D-6`, `D-9`, `D-18`, `D-21`,
  `D-28`, `D-30`, `D-34`, `D-35`, `D-38`, `D-40`, `D-107`, `D-151`
- Philadelphia's 2011-0463 (Vandergrift Rowe): `D-5`, `D-16`, `D-25`, `D-29`
- In-file noise: `Email-2`, `Email-15`, `Email-23`, `Email-27`

**Scoring:** Returning a merged set that includes any Braxton-Ferrer message
without flagging the collision = precision fail. Returning only Denver's set =
recall **and** verdict fail.

---

## Query 4 — Causation / responsibility

> *"Why did the custody violations recur at Marchwood after 2016, and who is
> responsible?"*

**Correct verdict:** Responsibility for the violation is Marchwood's. The
undertaking it gave in 2011 had no expiration and by its own terms reached
accounts acquired or onboarded later; the firm resumed the identical practice in
the first quarter of 2019 with a new billing platform and a re-drafted
authorization clause, on a book that included 138 accounts squarely inside the
undertaking. The firm's own 2017 move off its legacy archiving platform lost the
correspondence, and the compliance officer who gave the undertaking had left in
February 2016.

But the answer is incomplete without the second half, which no single email
states. The Commission's own systems removed every trace that the undertaking
existed: the 2016 migration left pre-2014 correspondence behind, and the C-4 to
C-2 code mapping deleted the one field that would have told the next examiner
something had been promised. In August 2019 the risk model scored Marchwood in
the bottom quartile — correctly, on inputs that said the last examination closed
with no further action and no open items of record — and the firm fell off the
FY2020 candidate list. The follow-up that Email-12 flagged in 2011 was never
scheduled, and nobody knew until a tip arrived in 2023.

**MUST cite:** `Email-40` (non-negotiable — it is the only message that states
both halves), `Email-20`, `Email-21`, `Email-22`, `Email-19`, `Email-9`.
**Bonus:** `Email-11`, `Email-12`, `Email-18`, `Email-25`, `Email-39`.

**MUST NOT cite (precision fails):**

- `D-112`, `D-142`, `D-147`, `D-54`, `D-55` — Vandergrift Rowe, whose undertaking
  really did expire on December 31, 2012. Attributing "the undertaking had
  lapsed" to Marchwood is the inverted answer and a verdict failure as well as a
  precision failure.
- `D-119`, `D-120` — Ellersby Kinnaird's Schedule A limitation, the other way an
  undertaking can fail to reach later accounts
- `D-143`, `D-146` — Corrigan Weld, which never held the authority at all
- `D-132`, `D-134`, `D-135`, `D-136` — Ottoway Trask, where the same archive
  search correctly found nothing
- `Email-27` — a different firm with a similar name

Attributing the recurrence to a lapsed or time-limited undertaking, or concluding
that the staff cleared the practice in 2011, is a verdict failure.

---

## Quick scoring rubric (per query)

| Axis | Full (2) | Partial (1) | Fail (0) |
|---|---|---|---|
| **Recall** | All required IDs plus the key attachment | Misses a supporting email but has the core needle | Misses the query's non-negotiable ID |
| **Precision** | Zero trap citations | One minor look-alike | Cites the other 2011-0447, a Marchwood name collision, Vandergrift Rowe's undertaking, or Vasseur-Kyle's Everly Sound correspondence |
| **Verdict** | Correct, and explains the system-of-record gap | Correct but shallow | Wrong (e.g. "the 2011 examination closed with no findings", "the undertaking expired", "no corrective action was required") |

4 queries × 3 axes × 2 points = **24 points**.

**Demo passes** when Query 1 scores full on recall, precision and verdict.
