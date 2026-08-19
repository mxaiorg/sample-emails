# Build notes — `marchwood-0447`

Fifth corpus in the series, after `harborpoint-marina` (insurance),
`riverwalk-garage` (engineering/AEC), `northfield-grain` (commercial lending) and
`corbin-tower-632588` (interiors/architecture).

**Vertical: US securities regulation, seen from inside the SEC.** Built for the
Securities and Exchange Commission as an email-to-Box management prospect. The
archive whose value the demo proves is the agency's own electronic mail journal
archive; the system that gets the answer wrong is the agency's examination case
system.

Everything in this corpus is fictitious. The registrants, the staff, the
examination numbers and the administrative proceeding are invented. The
regulatory framework, the two records-management facts the story turns on
(the September 2011 agency-wide suspension of records destruction, and the NARA
Capstone approach to email under the general records schedule) and the standard
deficiency-letter language are real and were verified against primary sources
during the build.

---

## 1. Phase 0 — the design, as six sentences

1. **The needle.** June 2, 2011 — Marguerite Vasseur-Kyle, Chief Compliance
   Officer of Marchwood Asset Management LLC, writes to the Philadelphia
   examination staff in examination **2011-0447** accepting **Item 4** of the
   April 20 deficiency letter, confirming that all **214** affected accounts have
   moved to Signal Peak Trust Company under agreements giving Marchwood no
   withdrawal authority, stating that the practice is discontinued firm-wide and
   "we will not resume it," and undertaking to apply the same treatment to
   accounts acquired or onboarded in future — **"not limited to calendar year
   2010 or to any other period and given without an expiration date."**
2. **Both systems lose it.** The March 2016 **EXAMTRAC → SENTRY** migration
   carried only the summary record and the indexed final letters for
   examinations closed before January 1, 2014, and had no target value for the
   legacy disposition code **C-4 (closed on registrant undertaking)**, which was
   mapped onto **C-2 (closed, no further action)**. Marchwood's own 2017 move off
   its legacy archiving platform lost everything before 2014.
3. **Everyone has left.** Whitlatch left in 2015, Vasseur-Kyle in February 2016,
   Raghunathan in 2017, Achterberg in 2019, Penhaligon in 2020, Okuma in 2021.
   Prior counsel dissolved in 2018.
4. **The claim.** November 12, 2024 — in AP File No. **3-21987** the respondent
   moves for summary disposition on the Division's own production, which
   consists of a summary row coded C-2 and a two-paragraph closing letter, and
   gives notice of an Equal Access to Justice Act claim. **$4,300,000** of relief
   is at risk on the motion.
5. **The archive produces it — plus the precedent.** January 14, 2025 — the mail
   journal archive, never migrated and with its retention clock frozen since the
   September 2011 moratorium, returns the twelve-message 2011 sequence with
   attachments intact, and then the **October 21, 2013** letter in which
   Marchwood applied the undertaking to the 61 accounts acquired from Hollis
   Grange **unprompted, with no examination open**, and paid for a surprise
   examination covering an eleven-day exposure.
6. **The claim collapses.** February 21, 2025 — motion, EAJA notice and forum
   challenge all withdrawn. March 14, 2025 — settled order: censure, cease and
   desist, disgorgement $1,412,000 + prejudgment interest $137,000 + civil
   penalty $601,000 = **$2,150,000**.

**Trap identifiers.** Legacy examination number **2011-0447**, which identifies
**two** unrelated examinations because each regional office ran an independent
four-digit series until the national scheme took effect on November 1, 2013 —
Philadelphia's is Marchwood (custody), Denver's is Braxton-Ferrer Advisors
(advertising). Plus deficiency-letter **Item 4**, which thirty distractor
messages carry on some other subject, and three transposed near-misses in daily
use: 2011-0477, 2011-0417, 2010-0447.

---

## 2. Files

```
stories/
├── marchwood-0447/
│   ├── marchwood-0447.md               40 emails, 16 attachment refs   <- INGEST ONLY THIS
│   ├── grading-key.md                  4 queries, 24 points            <- NEVER INGEST
│   ├── BUILD-NOTES.md                  this file                       <- NEVER INGEST
│   └── attachments/                    16 markdown documents
├── securities-regulation-distractors/
│   ├── securities-regulation-distractors.md   155 hard negatives
│   ├── CAST_AND_TRAP_SHEET.md          the authoring brief             <- NEVER INGEST
│   └── part-A..D.md                    authoring batches, merged       <- NEVER INGEST
└── securities-regulation-bulk-filler/
    ├── securities-regulation-bulk-filler.md   6,000 generated messages
    ├── generate.py                     seeded, self-contained
    └── _config_block.py                the CONFIG block alone, for the next port
tools/
└── audit_corpus.py                     ERA_TERMS extended for this vertical
```

**Corpus total: 6,195 messages.**

The indexer must take **only** `marchwood-0447/marchwood-0447.md` from the signal folder. A
`*.md` glob puts the answer key in the searchable archive.

---

## 3. Reproducing the filler

```
python3 stories/securities-regulation-bulk-filler/generate.py \
    --count 6000 --seed 604718 \
    --out stories/securities-regulation-bulk-filler/securities-regulation-bulk-filler.md
```

Seed **604718**, count **6000**, sha256 prefix **db1c6955715a3019**. Verified
byte-for-byte reproducible across three runs.

Vertical-specific configuration lives entirely in the CONFIG block at the top.
Four machinery changes were made below the line and are commented in place:

1. `PROJECTS` → `REGISTRANTS` and `{project}` → `{registrant}`; the unit of work
   in this vertical is the examined registrant, not a job.
2. **Registrant-facing templates now name the registrant they are addressed to.**
   The reference implementation samples the correspondent and the subject entity
   independently, which here produced a delinquency notice to one adviser about
   another adviser's filing.
3. **Role gating.** `TEMPLATE_ROLES` names the staff roles that may send each
   template. Without it the generator cast an HR generalist as the author of an
   enforcement referral.
4. **Direction-scoped opener and closer pools.** An internal aside ("Noting for
   the file:", "Raise it with me rather than with the branch directly") on a
   letter to a registrant is a register error, and register errors are what make
   a synthetic archive read as synthetic.

Identifier bases are chosen so a generated number can never contain a signal or
distractor identifier as a substring: examinations are `EX-YYYY-51xxx`, tips are
`TCR-YYYY-2xxxxx`, FOIA requests are `F-YYYY-4xxxx`.

`audit_corpus.py` `ERA_TERMS` was extended with twenty securities-regulation
terms (Division of Examinations from 2020, Regulation Best Interest and Form CRS
from 2019, the Marketing Rule from 2021, Form PF from 2011, SSAE 16/18, T+2/T+1,
Capstone from 2013, EDGAR Next from 2024, and others). `OCIE` is deliberately
open-ended at the top of its window: the office was renamed in December 2020, but
a 2025 message referring back to a 2011 examination legitimately still calls it
OCIE.

---

## 4. Gate results

### Gate 1 — structural validation

```
marchwood-0447.md:                        40 emails, 16 attachment references   PASS
securities-regulation-distractors.md:    155 emails,  0 attachment references   PASS
securities-regulation-bulk-filler.md:  6,000 emails,  0 attachment references   PASS
grading-key.md (check_grading_key.py)                                           PASS, no warnings
  Query 1: 12 must-cite,  74 must-not-cite
  Query 2: 10 must-cite,  15 must-not-cite
  Query 3: 12 must-cite,  41 must-not-cite
  Query 4:  6 must-cite,  14 must-not-cite
  4 queries x 3 axes x 2 points = 24 points; key references 40/40 signal emails
```

Every query enumerates its traps by ID. Query 4's MUST-NOT list had to be
rewritten as a bullet list: the checker's parser closes a list at any line
starting with `**`, and a continuation line beginning `**did** expire` silently
truncated the list to three IDs.

### Gate 2 — adversarial realism audit

`PASS` on all three files together. Notable lines:

```
ok    signal:era-gating          0 anachronistic term uses
ok    signal:body-diversity      100.0% distinct
ok    distractors:holidays       0 emails sent on a US federal holiday
ok    filler:body-diversity      82.1% distinct (target >=75%)
ok    filler:coverage            6000 emails, 2009-01-02 to 2025-12-31, 17 years
ok    cross:cast-leak            0 addresses appear in both the filler and a signal file
ok    cross:token-leak           0 signal tokens found in the filler
ok    cross:spelling             signal / distractors / filler all american
```

Three advisory `info` lines, all expected: weekday skew of 37.5% on the signal,
34.8% on the distractors — both hand-authored narrative below the 200-message
threshold at which the distributional checks become meaningful — and 20.3% on
the filler, which is the target.

The first filler build came in at 75.4% body diversity, one third of a point
above the threshold. Widening the opener pool by four and the closer pool by
seven took it to 82.1%.

### Gate 3 — content consistency

Two adversarial passes were run: one over the signal plus all sixteen
attachments, and one cross-checking the four independently authored distractor
batches against each other and against the signal. Together they returned 43
findings. All substantive ones are fixed. The ones worth recording, because they
are the class of defect that falsifies a demo:

| # | Defect | Fix |
|---|---|---|
| 1 | **The premise was legally wrong.** Rule 206(4)-2(b)(3) expressly relieves an adviser of the (a)(4) surprise examination where its custody arises *solely* from authority to withdraw its advisory fee. As first drafted, Section 6(c) was a pure fee-debit clause, so no surprise examination was ever required, Item 4 was not a deficiency, and the entire matter collapses. | Section 6(c) broadened to authorize withdrawal of funds or securities generally, not limited to the fee, in all eight documents that describe it. The (b)(3) analysis is now stated expressly in the findings memo, the deficiency letter, the call memorandum, the referral, the OIP, the opposition and the settled order. |
| 2 | The instruction to Form ADV Item 9 permits a "No" answer where custody arises solely from fee deduction, so the Section 207 count failed as pleaded. | Follows from #1; the OIP and settled order now say so expressly. |
| 3 | Item 9(A)/9(B) miscited throughout — 9.B is about *related persons*, and Marchwood's custodian is unaffiliated. | Restated as Items 9.A.(1)(a) and 9.A.(1)(b) in six documents. |
| 4 | The EAJA application was filed the same day as the dispositive motion. Rule 44 permits an application only once the applicant has prevailed. | Converted to a **notice of intent** to seek fees on prevailing, in the motion, in three emails and in the settled order. |
| 5 | The $2,150,000 was quoted as the Division's demand nine weeks *before* the archive search that identified the 138-account cohort defining it. | Pre-discovery demand raised to **$4,300,000**; the settled figure now reads as the negotiated reduction it is, and the settled order says so. |
| 6 | A calendar-2010 surprise examination cannot be performed in mid-2011. | The undertaking now engages the accountant for **calendar year 2011** and states that the 2010 examination cannot be reconstructed. |
| 7 | Nobody pulled the public Form ADV-E filing history, which would have shown filings for 2011 and 2013 and none after. | Added to the referral memorandum and to the OGC assessment, with the correct caveat that it proves the firm hired an accountant, not that the staff required it. |
| 8 | The Hollis Grange book held $37.4m in 2013, while the whole post-2011 cohort held $38.5m in 2023. | 2013 figure reduced to $12.3m. |
| 9 | "Eleven weeks" between the motion and the archive search was nine. | Corrected. |
| 10 | The C-4 → C-2 argument claimed C-2 means "nothing was found," but the same code set has C-1 for that. | Restated: the mapping does not invert a meaning, it deletes the one fact the next examiner needs. |
| 11 | The migration notice never explained why the closing letter survived and the deficiency letter did not. | Closing letters were indexed by the EXAMTRAC closing workflow; letters issued while an examination was open were indexed only by hand. |
| 12 | Both sides ignored the closing letter's own opening clause — "based on the corrective actions described in your response" — for fourteen months, although the 2023 referral memorandum had already flagged it. | Confronted in the motion and answered in Email-29. |
| 13 | A distractor asserted as fact that Philadelphia has no 2011-0447, and an IT test result enumerated every 2011-0447 in SENTRY and omitted Philadelphia's. Either could be cited to defeat demo query 3. | Both corrected. |
| 14 | The Vandergrift Rowe near-miss twin's recurrence was dated 2016, colliding lexically with demo query 4 and yielding the inverted verdict. | Moved to 2023, as the trap sheet specified. |
| 15 | Six examinations in the distractor file had two or three deficiency letters, or a deficiency letter issued after their own closing letter, because four batches reused the same numbers. | Nine examinations renumbered onto free numbers; the pre-2014 ambiguity that the demo depends on is untouched. |
| 16 | Administrative proceeding file numbers were not monotonic with institution date, and one fee application preceded its own proceeding by two months. | 3-22041 → 3-21418, 3-22106 → 3-21455; the 3-21985 arc moved so institution lands in the signal's own week (February 2024) and the fee application in 2025. |
| 17 | Two distractors broke frame and described the corpus's own purpose ("if the inventory is going to be used to test a retrieval approach"). | Rewritten in register. |

Also corrected: 2,417 archive hits across twelve mailbox-years (raised to
241,700), a search term list that could not have produced the false positives it
claimed, "a fifteen-day extension" that was fourteen days, a ticket that existed
a month before it was logged, a successor CCO who inherited in 2016 an archive
truncated in 2017, "Q1 Form PF section 4" for an annual filing, a civil penalty
sought under the wrong subsection, prior counsel nobody ever tried, a 2020s
idiom in a 2016 message, and a Wexford Trelaine file whose 2019 recollection
disagreed with the 2010 letter on both its date and two of its four items.

Post-*Jarkesy* realism is handled in-world rather than by refactoring the matter
into district court: the OGC assessment notes the pending forum challenge, gives
the Division's answer (206(4)-2 and 206(4)-7 are prophylactic rules with no
common-law analogue, and Section 207 is the exposed count), and the respondent
withdraws the challenge as part of the settlement.

### Gate 4 — retrieval reality check (`rank_check.py`, BM25 over all 6,195)

| Query | Needle | Rank | First filler | Top-20 |
|---|---|---|---|---|
| "Did Marchwood ever agree in writing to stop debiting advisory fees directly from client accounts?" | Email-11 | **8** | 31 | 12 signal / 8 distractor — **PASS** |
| "Did anyone at Marchwood accept the custody finding in examination 2011-0447, or did that examination close with no findings?" | Email-11 | **14** | 89 | 11 signal / 9 distractor — **PASS** |
| "Our examination file for Marchwood shows disposition C-2 … did the staff ever require corrective action?" | Email-11 | **15** | 22 | 10 signal / 10 distractor — **PASS** |
| "Show me every email on examination 2011-0447." | Email-11 | **10** | 26 | 9 signal / 11 distractor — **PASS** |
| "Why did the custody violations recur at Marchwood after 2016 and who is responsible?" | Email-40 | **1** | 54 | 17 signal / 3 distractor — **PASS** |

Per §13 of the process specification the primary query was tested **both with and
without the examination number**. Both pass. Query 3 is the strongest precision
test in the corpus: `2011-0447` appears verbatim in 22 signal and 26 distractor
messages and in **zero** filler messages, so the live tool's verbatim-identifier
filter eliminates the filler entirely and leaves the two examinations that share
the number competing on equal weight — which is exactly the point.

Query 4's needle is **Email-40**, not the C-4 mapping emails. Email-40 is the only
message that states both halves of the causation answer; Email-20 ranks 24th on
that query and Email-22 ranks 49th, so a key that named either as the needle
would have failed the gate while the corpus was fine.

### Gate 5 — blind evaluation

Not run. Requires the corpus built to `.eml` and ingested. See §6.

---

## 5. Deliberate in-world inaccuracy

Email-37: the Division's covering email describes the supplemental production as
"the **eleven** emails from the 2011 examination sequence." The sequence is
**twelve**. Email-34, the production index and the Division's own opposition all
state it correctly. Documented in the grading key as intentional. An evaluator
that notices and reports the discrepancy is behaving correctly and should be
credited.

Gate 3 confirmed this is the only miscount in the corpus.

---

## 6. What is left to do

```bash
# 1. attachments -> PDF
tools/md_to_pdf.sh stories/marchwood-0447/attachments

# 2. build .eml  (only <slug>.md from the signal folder)
go run . -create -md stories/marchwood-0447/marchwood-0447.md -out stories/marchwood-0447/emls
go run . -create -md stories/securities-regulation-distractors/securities-regulation-distractors.md -out stories/securities-regulation-distractors/emls
go run . -create -md stories/securities-regulation-bulk-filler/securities-regulation-bulk-filler.md   -out stories/securities-regulation-bulk-filler/emls

# 3. send
go run . -send stories/marchwood-0447/emls
go run . -send stories/securities-regulation-distractors/emls
go run . -send stories/securities-regulation-bulk-filler/emls
```

Then confirm the indexer took **only** `marchwood-0447/marchwood-0447.md` from the signal folder
— not `marchwood-0447/grading-key.md`, not `BUILD-NOTES.md` — and run five blind-evaluator
passes, recording each as `test-results-<date>-run<N>.md`.

**Demo-ready** = Query 1 scores full on recall, precision and verdict.

---

## 7. Demo script, in four moves

1. **"Show me every email on examination 2011-0447."** Two examinations come
   back. The tool has to say so. This is the query the customer will try first
   because it is the one their own system answers wrongest.
2. **"Our file shows the 2011 examination closed with no further action. Did we
   ever require anything of this firm?"** The archive contradicts the system of
   record and explains why — a migration scope decision and a disposition code
   with no target value.
3. **"Show me the letter."** Email-11, quoted verbatim, with the signed
   attachment, in the registrant's own words.
4. **"Did they ever act on it?"** Email-16. Two years later, unprompted, with no
   examination open, they applied it to a book they had just bought and paid for
   a surprise examination covering an eleven-day exposure. That is the beat that
   ends the argument.

The number to say out loud at the end is **$2,150,000**, and the sentence to say
with it is Camille Ostrowski's in Email-40: the case was won by two letters that
were in neither party's document system and in the email archive the whole time.
