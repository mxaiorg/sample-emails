# Build notes — `corbin-tower-632588`

Fourth corpus in the series, after `harborpoint-marina` (insurance),
`riverwalk-garage` (engineering/AEC) and `northfield-grain` (commercial lending).
Vertical: **interiors + architecture**, modeled on SAA interiors + architecture —
a four-studio design practice with a numeric project-ID convention.

---

## 1. Phase 0 — the design, as six sentences

1. **The needle.** May 17, 2011 — Dana Truscott, Director of Corporate Real Estate at
   Ardsley Financial Group, directs VAA in writing to delete Specification Section
   09 05 61 (epoxy moisture vapor mitigation) from project **632588**, accepts the
   $347,900 credit and 18 days of schedule, records the deletion as owner-directed
   and made over VAA's written recommendation, and **accepts responsibility for
   future flooring performance issues arising from slab moisture.**
2. **Both systems lose it.** VAA's November 2016 Docuvault → Corvantis migration
   excluded correspondence, minutes and the ASI log for projects last active before
   January 1, 2014. Ardsley's own 2017 consolidation did the same to theirs.
3. **Everyone has left.** Ashcombe retired 2019, Okonkwo left 2015, Truscott retired
   2018, Kilcoyne left 2016, Threadgill retired 2021.
4. **The claim.** November 12, 2024 — Hollingsworth Vane demands **$2,150,000** for
   flooring failure on Levels 12–17, resting on Finish Schedule Rev 4, the one
   document the firm's system still holds, issued under VAA's own seal.
5. **The archive produces it — plus the precedent.** January 2025 — the mail journal
   archive, never migrated, produces the April 6 letter, the May 17 directive and
   ASI-031, and then the October 8, 2013 letter in which Ardsley **already applied**
   the direction, funding an $88,400 repair and expressly making no claim.
6. **The claim collapses.** February 21, 2025 — withdrawn in full. March 6, 2025 —
   claim NMD-C-24-2207 closed, indemnity $0, defense cost $61,400, not chargeable.

**Trap identifiers.** `ASI-031` (16 other projects carry one) and project number
`632588`, which identifies **two** unrelated projects because the Iselin studio ran
an independent six-digit series until the October 2013 consolidation. Plus three
transposed-digit near misses in daily use: 632568, 632858, 635288.

---

## 2. Files

```
stories/
├── corbin-tower-632588/
│   ├── corbin-tower-632588.md         40 emails, 18 attachment refs   <- INGEST ONLY THIS
│   ├── grading-key.md                 4 queries, 24 points            <- NEVER INGEST
│   ├── BUILD-NOTES.md                 this file                       <- NEVER INGEST
│   └── attachments/                   18 markdown documents
├── architecture-distractors/
│   ├── architecture-distractors.md    155 hard negatives
│   ├── CAST_AND_TRAP_SHEET.md         the authoring brief             <- NEVER INGEST
│   └── part-A..D.md                   authoring batches, concatenated <- NEVER INGEST
└── architecture-bulk-filler/
    ├── architecture-bulk-filler.md    6,000 generated messages
    ├── generate.py                    seeded, self-contained
    └── _config_block.py               the CONFIG block alone, for the next port
```

**Corpus total: 6,195 messages.**

The indexer must take **only** `corbin-tower-632588.md` from the signal folder. A
`*.md` glob puts the answer key in the searchable archive.

---

## 3. Reproducing the filler

```
python3 stories/architecture-bulk-filler/generate.py \
    --count 6000 --seed 831207 \
    --out stories/architecture-bulk-filler/architecture-bulk-filler.md
```

Seed **831207**, count **6000**, sha256 prefix **6c1879009a02f98a**. Verified
byte-for-byte reproducible across three runs.

Vertical-specific configuration lives entirely in the CONFIG block at the top.
Two machinery changes were made below the line and are commented in place:
an `asi_no` placeholder, and an `"asi": 40` sequence start so a generated ASI
number can never collide with ASI-031.

---

## 4. Gate results

### Gate 1 — structural validation (`validate_story.py`)

```
corbin-tower-632588.md:        40 emails, 18 attachment references   PASS
architecture-distractors.md:  155 emails,  0 attachment references   PASS
architecture-bulk-filler.md: 6000 emails,  0 attachment references   PASS
grading-key.md (check_grading_key.py)                                PASS, no warnings
  Query 1: 20 must-cite,  97 must-not-cite
  Query 2:  8 must-cite,  13 must-not-cite
  Query 3: 34 must-cite,  37 must-not-cite
  Query 4:  7 must-cite,  15 must-not-cite
  4 queries x 3 axes x 2 points = 24 points; key references 40/40 signal emails
```

Every query enumerates its traps by ID. There are no prose-only MUST-NOT lists,
which is the defect that made the riverwalk key's Queries 2 and 3 unscorable.

### Gate 2 — adversarial realism audit (`audit_corpus.py`)

`PASS` on all three files together. Notable lines:

```
ok    signal:era-gating          0 anachronistic term uses
ok    signal:body-diversity      100.0% distinct
ok    distractors:holidays       0 emails sent on a US federal holiday
ok    filler:body-diversity      77.7% distinct (target >=75%)
ok    filler:coverage            6000 emails, 2009-01-07 to 2026-06-30, 18 years
ok    cross:cast-leak            0 addresses appear in both the filler and a signal file
ok    cross:token-leak           0 signal tokens found in the filler
ok    cross:spelling             signal / distractors / filler all american
```

Two advisory `info` lines, both expected: `signal:weekday-skew` 30% and
`distractors:weekday-skew` 51.6%. Both files are hand-authored narrative below the
200-message threshold at which the distributional checks become meaningful — a
crisis week really is mostly Tuesday to Thursday.

`distractors:holidays` is **0**, which the riverwalk engineering distractor file
never achieved (it shipped 8).

### Gate 3 — content consistency

A dedicated adversarial pass over the signal plus all 18 attachments returned 20
findings; all substantive ones are fixed. The ones worth recording, because they
are the class of defect that falsifies a demo:

| # | Defect | Fix |
|---|---|---|
| 1 | "Twelve of fourteen probes exceed **90%**" was false — all fourteen do. Repeated in four documents. | Threshold restated as 93%, at which exactly twelve qualify. |
| 2 | 14 probes is ~10% of the F2170 sampling density the spec itself states, yet the report certified compliance. | Report relabeled as the **preliminary screening series** ahead of the full compliance series. |
| 3 | Authentication certificate claimed four byte-identical journal copies, three of whose recipients are **external** to VAA and cannot be journaled by VAA's transport. | Reduced to two VAA-side copies; `Received:` chains stated to differ, as they must. |
| 4 | ASI-031 stated a change in Contract Sum and Contract Time, which an ASI cannot do. | Restated as no change by the instruction, with a proposed change order directed. |
| 5 | The 8–15 year failure prediction was falsified by the corpus's own year-two precedent. | April 6 letter now carries the wet-use-room exception (2–4 years), which is technically correct and makes the precedent *support* the prediction. |
| 6 | Prewitt's 5.0 lb MVER limit is the carpet-tile adhesive limit; resilient products publish 3.0, and five of Prewitt's nine kits were at or above 3.0. | Added, and given to Ashcombe as a rebuttal — it strengthens VAA's position. |
| 7 | Email-35 "discovered" the 2013 letter that Email-33's own index had already listed. | Reframed as pulling it out of the index, not finding it. |
| 8 | Closure notice released a $2,150,000 reserve that had already been stepped down twice. | Reserve history recited. |

Also corrected: an ICRI guideline designation that postdates the 2010 spec, a
"first 16 bytes" label on 8-byte digests, a Level 19 lobby exclusion that
contradicted the area table, a "three months later" that was seven, a "fourteen
months" that was twelve, a spec-to-finish-schedule coverings mismatch, a
test-report signatory who was also the technician, and two title/quotation nits.

### Gate 4 — retrieval reality check (`rank_check.py`, BM25 over all 6,195)

| Query | Needle rank | First filler | Top-20 |
|---|---|---|---|
| "Who authorized removing the moisture mitigation from the Ardsley headquarters flooring?" | **9** | 37 | 14 signal / 6 distractor — **PASS** |
| "Did anyone ever authorize deleting the moisture mitigation system … project 632588?" | **15** | 53 | 17 signal / 3 distractor — **PASS** |
| "Our system has no ASI log for 632588 … did we delete it on our own authority?" | **17** | 28 | 12 signal / 8 distractor — **PASS** |
| "Why did the flooring at the Ardsley headquarters fail and who is responsible?" | **9** | 79 | 14 signal / 6 distractor — **PASS** |

Per §13, the primary query was tested **both with and without the identifier**.
Both pass, which the riverwalk build never verified.

**Gate 4 caught a real defect and it changed the filler.** The first filler build
put 15 of the top 20 on the identifier-free phrasing, because the filler templates
used the exact bigram "moisture mitigation" in short bodies and three filler
projects were named "… Headquarters". Fixes: renamed those projects, replaced
"authorization" with "approval" in the fee template, lengthened and reworded the
two flooring/moisture templates, split the moisture traffic across two templates,
and left the exact bigram "moisture mitigation" to the signal and the eight
distractors that use it. Vocabulary proximity is still carried in volume —
`ASTM F2170` ×123, `finish schedule` ×385, `ASI-` ×324, `RFI-` ×287, plus ~300
slab-relative-humidity and substrate-retest messages.

**Known limitation, by design.** `"Show me every email on project 632588"` fails
`rank_check` — pure BM25 has only one rare token in that query and scores the rest
on "project", which thousands of filler messages contain. This is an artifact of
the gate, not of the corpus: **632588 appears verbatim in 28 signal and 20
distractor messages and in zero filler messages**, and the live `email_search`
build hard-restricts results to verbatim identifier matches, which eliminates the
filler entirely. That restriction is exactly what makes Query 3 a precision test
rather than a recall test — the two 632588 projects both survive the filter.

### Gate 5 — blind evaluation

Not run. Requires the corpus built to `.eml` and ingested. See §6.

---

## 5. Deliberate in-world inaccuracy

Email-34: defense counsel writes "the **eleven** emails from the 2011 sequence."
The 2011 sequence is **twelve** (Email-2–5, 7–9, 11–15). Email-33 and the
production index both state twelve correctly. Documented in the grading key as
intentional. An evaluator that notices and reports the discrepancy is behaving
correctly and should be credited.

Gate 3 confirmed this is the **only** miscount in the corpus.

---

## 6. What is left to do

```bash
# 1. attachments -> PDF
tools/md_to_pdf.sh stories/corbin-tower-632588/attachments

# 2. build .eml  (only <slug>.md from the signal folder)
go run . -create -md stories/corbin-tower-632588/corbin-tower-632588.md -out stories/corbin-tower-632588/emls
go run . -create -md stories/architecture-distractors/architecture-distractors.md   -out stories/architecture-distractors/emls
go run . -create -md stories/architecture-bulk-filler/architecture-bulk-filler.md   -out stories/architecture-bulk-filler/emls

# 3. send
go run . -send stories/corbin-tower-632588/emls
go run . -send stories/architecture-distractors/emls
go run . -send stories/architecture-bulk-filler/emls
```

Then confirm the indexer took **only** `corbin-tower-632588.md` from the signal
folder — not `corbin-tower-632588/grading-key.md`, not `BUILD-NOTES.md` — and run five blind-evaluator
passes, recording each as `test-results-<date>-run<N>.md`.

**Demo-ready** = Query 1 scores full on recall, precision and verdict.
