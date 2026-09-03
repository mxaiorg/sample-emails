# Build notes — `kelling-0284`

Seventh corpus in the series, after `harborpoint-marina` (insurance),
`riverwalk-garage` (engineering/AEC), `northfield-grain` (commercial lending),
`corbin-tower-632588` (interiors/architecture), `marchwood-0447` (US
securities regulation) and `shinonome-0392` (global patent prosecution).

**Vertical: private law practice**, seen from inside Prescott Vane LLP, a
fictitious ~240-lawyer full-service Pennsylvania firm — Litigation & Dispute
Resolution, Corporate & Commercial, Labor & Employment, Real Estate, and
Bankruptcy & Reorganization. Built for the general legal-industry use case: the
demo customer is a law firm, the archive whose value the demo proves is the
firm's own mail journal archive, and the system that gets the answer wrong is
the firm's document management system. The story is the firm's own nightmare —
a legal-malpractice demand against the firm — ended by the firm's own email.

No real firm, client, product, or person is named. The professional-conduct,
audit-response and limitations framework is real and is recorded in §7.

---

## 1. Why this vertical needs this needle

A law firm's crown jewels are engagements, and the sharpest thing that can go
wrong with an engagement is a dispute about what it covered. Scope is decided
in correspondence: engagement letters get amended by email, carve-outs get
"confirmed in writing" without ever becoming a profiled document, and fifteen
years later the DMS holds the letter but not the limitation. The needle is
therefore a **client's written scope carve-out under Pa. R.P.C. 1.2(c)** — an
instrument that exists, by the client's own choice, only as an email and its
attached signed letter. It is never public, it is dispositive on its face, and
it is exactly the class of record that survives in a mail journal archive
after every system of record has shed it.

The malpractice frame gives the demo its stakes for a law-firm audience: the
claim is against the firm itself, and the archive is the firm's defense. Every
lawyer watching has a matter like this somewhere in their past, and every
managing partner knows the September 2022 advice email that saved — or the
scope note that vanished.

---

## 2. Phase 0 — the design, as six sentences

1. **The needle.** June 9, 2011 — Rosalind Tenniel, General Counsel of Torvane
   Industrial Group, Inc. (Erie), writes to Arthur Pellum of Prescott Vane,
   attaching a signed letter: the engagement under Matter 2011-0284 is limited
   to the Ridgeline Constructors claims; Torvane has considered the Brandt
   Thermal Systems warranty claim and elected not to assert it; that claim "is
   expressly outside the scope of your engagement," with the firm asked to
   take no step to evaluate, preserve, or pursue it; the company accepts the
   limitations consequences after written advice; and the confirmation "is not
   limited to any period and stands unless I withdraw it in writing."
2. **Both systems lose it.** The February 27–28, 2016 Casebridge → Novarra
   migration carried profiled documents but excluded the legacy CommsStore
   module — all matter correspondence filed before January 1, 2014 — and
   populated Novarra's controlled "Matter Scope" field from the
   engagement-letter document class (NOV-2119, closed "works as designed"). So
   the DMS shows an unlimited engagement, confidently. Torvane's side lost the
   same correspondence to its own platform changes and the 2021 Copeland Ridge
   acquisition, which transferred contracts, not email.
3. **Everyone has left.** Pellum retired June 2018 (remembers the carve-out,
   kept no files); Tenniel left Torvane in March 2015; associate Caleb Wisner
   went in-house at the end of 2015; Torvane's VP Engineering Walt Hagerman
   died in 2020.
4. **The claim.** November 14, 2024 — Garvey Strom LLP demands **$3,675,000**
   ($2,140,000 excess fuel + $890,000 media replacement + $645,000 downtime,
   from Torvane's own August 2013 RTO performance study), on the premise that
   the April 4, 2011 engagement letter — "claims arising out of the Kelling
   Station Unit 2 expansion project" — covered the Brandt claim and the firm
   let it expire.
5. **The archive produces it — plus the precedent.** January 9, 2025 — the
   mail journal archive (journaling every message since October 2007, never
   migrated because it is an archive, not a system of record) returns the
   eleven-message 2011 matter sequence in a fourteen-minute search, signed
   confirmation intact and hash-verified. January 13 — a second pass surfaces
   **October 17, 2013**: Tenniel striking the Brandt matter from the firm's
   draft audit response to Caulfield Roth, citing her June 9, 2011
   confirmation by date — the client enforcing the carve-out against the
   firm's own draft, with no dispute pending.
6. **The claim collapses.** Response letter with production served January 21,
   2025; demand withdrawn in its entirety **February 24, 2025**; Keystone
   closes the claim file at indemnity $0 and defense cost **$92,400**.

## 3. What is new in this build

- **The customer is the archive's owner is the defendant.** In every earlier
  corpus the archive vindicated the host company against an outside
  counterparty. Here the archive defends the firm against its own former
  client — the loss-prevention frame every law firm buys insurance for.
- **The distractor file carries two full counter-stories.** Danforth
  Elastomers is the near-miss twin *with the opposite outcome*: a carve-out in
  almost the needle's words, but time-limited, lapsed, and worth $610,000 of
  settlement — the corpus's proof that the words "not limited to any period"
  are load-bearing. Ellard Marine is the anti-precedent: the same records
  director runs the same archive search in 2023, honestly finds nothing, and
  the firm pays $1,150,000 — the corpus's proof that the archive is a witness,
  not a defense fund.
- **The precision layer is legal-practice-native**: a second matter numbered
  2011-0284 (legacy numbering preserved through a law-firm merger), four
  unrelated companies named Torvane, two unrelated Kellings, the same GC
  writing the same style of letter for a new employer, and audit-response
  season traffic that reuses the ABA "engaged and devoted substantive
  attention" vocabulary annually across other clients.

## 4. Files

```
stories/
├── kelling-0284/
│   ├── kelling-0284.md                40 emails, 15 attachment refs   <- INGEST ONLY THIS
│   ├── grading-key.md                 4 queries, 24 points            <- NEVER INGEST
│   ├── BUILD-NOTES.md                 this file                       <- NEVER INGEST
│   ├── DESIGN-BRIEF.md                the authoring brief             <- NEVER INGEST
│   └── attachments/                   15 markdown documents
├── legal-practice-distractors/
│   ├── legal-practice-distractors.md  155 hard negatives
│   ├── CAST_AND_TRAP_SHEET.md         the authoring brief             <- NEVER INGEST
│   ├── merge_distractors.py           batch merge/renumber script     <- NEVER INGEST
│   └── part-A..D.md                   the four authored batches, merged and superseded  <- NEVER INGEST
└── legal-practice-bulk-filler/
    ├── legal-practice-bulk-filler.md  6,000 generated messages
    └── generate.py                    seeded, self-contained
tools/
├── validate_story.py                  unchanged (shinonome version)
├── audit_corpus.py                    ERA_TERMS matcher fixed: word-boundary match
│                                      ('PTAB' no longer fires inside 'acceptable')
├── rank_check.py                      unchanged (shinonome version)
└── check_grading_key.py               unchanged
```

**Corpus total: 6,195 messages.**

The indexer must take **only** `kelling-0284.md` from the signal folder. A
`*.md` glob puts the answer key in the searchable archive.

## 5. Reproducing the filler

```
python3 stories/legal-practice-bulk-filler/generate.py \
    --count 6000 --seed 284117 \
    --out stories/legal-practice-bulk-filler/legal-practice-bulk-filler.md
```

Seed **284117**, count **6000**, sha256 prefix **da9e0fdb862076ce**. Verified
byte-for-byte reproducible across two runs. The vertical lives in the CONFIG
block. Machinery changes from the reference implementation: the fixed
`nth_weekday(..., -1)` (shinonome build), role gating (`TEMPLATE_ROLES` — a
billing manager does not serve document productions), counterparty-kind gating
(`CP_FOR` — audit inquiries come only from the CPA firm, transcripts only from
the court reporter), one canonical matter number per filler matter in a
4-digit block ≥ 3000 (no filler number collides with, or contains, any
signal/distractor number), and `n_roots = count × 0.92` (this template set has
fewer reply-eligible categories than the AEC original, so the reference
formula under-produced).

## 6. Gate results

### Gate 1 — structural validation

```
kelling-0284.md:                       40 emails, 15 attachment references   PASS
legal-practice-distractors.md:        155 emails,  0 attachment references   PASS
legal-practice-bulk-filler.md:      6,000 emails,  0 attachment references   PASS
grading-key.md (check_grading_key.py)                                        PASS, no warnings
  Query 1: 14 must-cite,  85 must-not-cite
  Query 2:  9 must-cite,  16 must-not-cite
  Query 3: 11 must-cite,  33 must-not-cite
  Query 4: 11 must-cite,  26 must-not-cite
  4 queries x 3 axes x 2 points = 24 points; key references 40/40 signal emails
```

MUST-NOT-cite IDs were generated programmatically from the batch labels at
merge time and spot-verified by hand against the merged file (D-6 = the
Danforth confirmation, D-82 = the Halbrook confirmation, D-102 = the Glassport
legacy-number email, D-133 = the Ellard demand, etc.).

### Gate 2 — adversarial realism audit

`PASS` on all three files together. Notable lines:

```
ok    signal:era-gating          0 anachronistic term uses
ok    signal:holidays            0 emails sent on a US federal holiday
ok    signal:body-diversity      100.0% distinct
ok    distractors:holidays       0 emails sent on a US federal holiday
ok    distractors:body-diversity 100.0% distinct
ok    filler:body-diversity      87.9% distinct (target >=75%)
ok    filler:weekday-skew        busiest weekday holds 21.0% of weekday traffic
ok    filler:coverage            6000 emails, 2009-01-05 to 2025-12-31, 17 years
ok    cross:cast-leak            0 addresses appear in both the filler and a signal file
ok    cross:token-leak           0 signal tokens found in the filler
ok    cross:spelling             signal / distractors / filler all american
```

Advisory lines, all expected: weekday skew 37.5% (signal) and 54.2%
(distractors) — hand-authored narrative below the 200-message threshold;
2/40 and 1/155 subject-month warnings are hearing dates and deadlines
legitimately named months ahead. A toolkit fix was made during this gate:
`audit_corpus.py`'s ERA_TERMS check now matches on word boundaries — the
previous substring match flagged 'PTAB' inside the word "acceptable."

### Gate 3 — content consistency

Two adversarial passes were run — one over the signal plus all fifteen
attachments, one cross-checking the four distractor batches against each other
and against the signal. Together they returned **25 substantive findings plus
a set of nits**; all substantive ones are fixed. The ones worth recording:

| # | Defect | Fix |
|---|---|---|
| 1 | **Wisner claimed absence from discussions the corpus shows him inside.** The 2013 draft-audit email said he "was not with the firm when the scope discussions concluded" — but he wrote the May 2011 limitations memo and received the June instructions. | Both the email and the draft's bracket note now say he was "not on the client calls" and refuses to rely on memory. |
| 2 | Wisner's departure was 2014 in one email and end-2015 in another. | End of 2015 everywhere. |
| 3 | "Twenty-nine months later" (June 2011 → October 2013) was wrong and contradicted the correct "two years and four months" elsewhere. | Twenty-eight months in both places. |
| 4 | Email-30 counted "billing records" among the fourteen profiled documents; the Novarra record's 14-row table has none. | Billing data moved outside the count. |
| 5 | **The journal-archive volumes were incoherent by two orders of magnitude** — 46,000 messages/year firm-wide against a CommsStore filed subset of 2.1 million. | Archive rescaled: ~3 million messages/year in the 2011 era, ~19 million for the 2009–2014 slice; the distractor certification thread rescaled to match (3.4 million/year in 2022). |
| 6 | **The second archive pass could not have found anything new** — the first search's 2011–2014 window and terms already matched the October 2013 emails. | First pass narrowed to calendar 2011; the second pass extends the window over 2012–2014. |
| 7 | The demand-response letter's effective-date behavior ignored the auditor's requested mid-November effective date. | The final audit response now offers to update through the requested date. |
| 8 | The RTO study's 690 operating hours/month contradicted the commissioning-failure narrative. | The study now states the oxidizer fired throughout commissioning at line schedule under the temporary permit. |
| 9 | A distractor Keystone letter declared "both November 2024 claims resolved" on February 4, 2025 — the signal's claim was withdrawn February 24. | The letter now notes the other matter remains open pending the insured's record search. |
| 10 | A distractor placed Pellum's retirement reception two weeks before the signal's announcement of it. | Reworded to the future tense. |
| 11 | A distractor asserted all four Torvane companies are unrelated; the signal calls Torvane Logistics "their logistics affiliate." | The relatedness claim removed. |
| 12 | Help-desk ticket NOV-2087 was numbered below the signal's NOV-2119 but opened a month later. | Renumbered NOV-2287. |
| 13 | "At Easter" in an email dated five days before Easter 2014. | "At Sunday dinner." |
| 14 | A subpoena-count email dated Craddock correspondence from February 2011, four months before the Vollmer engagement existed. | June 2011. |
| 15 | The Danforth file review had pre-2014 correspondence in hand one day after the demand with no retrieval mechanism stated. | The review email now credits a journal-capture pull under the claims protocol. |
| 16 | The 2023 Ellard closing referred to a "tolled claim shell" no email had established, and the 2019 changes were mislabeled claims-intake. | Both corrected. |
| 17 | Pennsylvania CLE group 1 was given group 2's August 31 deadline. | Group 2. |
| 18 | A conflicts email described a 2007 matter as adverse to "a Ridgeline subcontractor"; the report says the company was later acquired by Ridgeline. | Email matches the report. |
| 19 | The three-week gap between search authorization (Dec 17) and the run (Jan 8) was unexplained while a carrier deadline loomed. | Attributed to the archive platform's year-end processing freeze. |
| 20 | The 2011 Glassport thread was authored under a partner who only joins the firm at the 2014 merger. | The 2011 emails now belong to Roger Quillen of Aldous & Crane, who retired at the merger; the validator's one-address-per-name rule is satisfied. |

Also corrected: "same date, same words" overstating the email/letter match
(same substance, different pronouns); a quoted-sentence position ("two
sentences later" → "in the next paragraph"); an interim ruling described as in
an audit draft that never mentioned it; a "Markup to you Thursday" sent on a
Thursday; a fifteen-month repair timeline called eighteen; a missing "Claims
Attorney" signature line; and verbatim-vocabulary gaps ("statutes of
limitations," "audit response") closed so the trap identifiers exist in the
noise as designed.

Two things were **not** changed and are documented as intentional: the
Email-38 "ten emails" miscount (§8), and the unremarked blown response
windows on both sides of the 2024–2025 exchange (real correspondence slips
deadlines without comment).

### Gate 4 — retrieval reality check (`rank_check.py`, BM25 over all 6,195)

| Query | Needle | Rank | First filler | Top-20 |
|---|---|---|---|---|
| Q1 — "did Torvane ever confirm in writing that the Brandt claim was outside the engagement?" | `Email-10` | **1** | 72 | 16 signal / 4 distractor — **PASS** |
| Q2 — "Novarra shows the engagement unlimited — is that the whole record?" | `Email-30` | **2** | 41 | 16 signal / 4 distractor — **PASS** |
| Q3 — the bare identifier "matter 2011-0284" | `Email-10` | **8** | 51 | 11 signal / 9 distractor — **PASS** |
| Q4 — "what went wrong and who is responsible?" | `Email-40` | **5** | 74 | 14 signal / 6 distractor — **PASS** |

The distractor presence in every top-20 (four to nine hits) is the designed
shape: the Danforth confirmation, the Ellard demand, the Halbrook letters and
the Glassport 2011-0284 all compete lexically and lose only on entity.

Per §13 of the process specification the primary query was tested with and
without the matter number. `2011-0284` appears verbatim in 16 signal messages,
19 distractor messages and **zero** filler messages, so the live tool's
verbatim-identifier filter eliminates the filler entirely and leaves the two
matters that share the number competing on equal weight — which is the point
of Query 3.

### Gate 5 — blind evaluation

Not run. Requires the corpus built to `.eml` and ingested. See §9.

---

## 7. Verified legal facts this corpus depends on

Checked at the level of generality the corpus uses. Do not "correct" these.

- **Pa. R.P.C. 1.2(c)** — a lawyer may limit the scope of the representation
  if the limitation is reasonable under the circumstances and the client gives
  informed consent. The needle is drafted as exactly that: a limitation
  proposed after written advice, confirmed in writing and by signed letter by
  the client's chief legal officer. (The rule does not itself require a
  writing; the writing is what makes the story provable, and the corpus never
  claims otherwise.)
- **ABA Statement of Policy Regarding Lawyers' Responses to Auditors' Requests
  for Information (December 1975)** — audit responses address matters "as to
  which the lawyer has been engaged and to which he has devoted substantive
  attention"; unasserted claims are addressed by the lawyer only where the
  client has specifically identified them. This is the real mechanism that
  makes the October 2013 precedent beat work: an unpursued, carved-out claim
  properly comes OUT of the lawyer's letter, and the client's instruction to
  remove it is an application of the 2011 confirmation.
- **Limitations for the underlying claim** — 13 Pa. C.S. § 2725 (UCC): four
  years from tender of delivery for goods, breach at tender regardless of
  knowledge, with the § 2725(b) future-performance exception; 42 Pa. C.S.
  § 5525: four years for contract actions generally. The memo treats the
  purchase order as mixed goods/services, notes the predominance question, and
  fixes a prudent outer boundary rather than resolving accrual — which is how
  a competent 2011 memo would put it.
- **Legal-malpractice limitations in Pennsylvania** — two years in tort
  (§ 5524(7)), four in contract, with the discovery rule; the 2024 demand
  pleads post-acquisition discovery. The firm's response deliberately rests on
  scope, not on limitations, so the corpus never has to resolve the harder
  accrual questions.
- **Law-firm mechanics** — matter-number series preserved through mergers;
  conflicts clearance before engagement letters; audit-inquiry season keyed to
  fiscal year-ends; LPL carrier notice, reserves, and claim-file practice;
  litigation holds on claim intake; journal archives as email retention
  copies distinct from DMS filing. All standard practice, rendered generically.

## 8. Deliberate in-world inaccuracy

Email-38 describes the production served with the response letter as "the ten
emails from the 2011 matter sequence." The sequence is **eleven** — Email-35,
the search report's exhibit table (A-1 through A-11), and the response letter
itself all say eleven. Gate 3 confirmed this is the only miscount in the
corpus. An evaluator that notices the discrepancy and reports it is behaving
correctly and should be credited.

## 9. What is left to do

```bash
# 1. attachments -> PDF
tools/md_to_pdf.sh stories/kelling-0284/attachments

# 2. build .eml  (only kelling-0284.md from the signal folder)
go run . -create -md stories/kelling-0284/kelling-0284.md -out stories/kelling-0284/emls
go run . -create -md stories/legal-practice-distractors/legal-practice-distractors.md -out stories/legal-practice-distractors/emls
go run . -create -md stories/legal-practice-bulk-filler/legal-practice-bulk-filler.md -out stories/legal-practice-bulk-filler/emls

# 3. send
go run . -send stories/kelling-0284/emls
go run . -send stories/legal-practice-distractors/emls
go run . -send stories/legal-practice-bulk-filler/emls
```

Then confirm the indexer took **only** `kelling-0284.md` from the signal
folder — not `grading-key.md`, `BUILD-NOTES.md`, or `DESIGN-BRIEF.md` — and
run five blind-evaluator passes, recording each as
`test-results-<date>-run<N>.md`.

**Demo-ready** = Query 1 scores full on recall, precision and verdict.

## 10. Demo script, in five moves

1. **"Show me every email on matter 2011-0284."** Two matters come back — a
   Pittsburgh industrial dispute and a Harrisburg shopping-center refinance —
   because the 2014 merger preserved legacy numbers, and the firm's own
   conflicts memo (`D-149`'s cousin, Email-2) warned about exactly this. The
   tool has to say so, not merge them.
2. **"Novarra says the Torvane engagement was unlimited — engagement letter,
   no amendment, scope field to match. So we were on the hook for the Brandt
   claim?"** No — and here is where that field came from: a 2016 migration
   that dropped every pre-2014 email and derived the scope description from
   the engagement letter alone, over a ticket closed "works as designed."
3. **"Did the client ever say otherwise, in writing?"** Yes. June 9, 2011.
   Show the email, then the signed letter attached to it — the claim
   "expressly outside the scope of your engagement," the confirmation "not
   limited to any period." Fourteen minutes of archive search against a
   thirteen-year silence.
4. **"Did anyone ever act on it?"** October 17, 2013. The client's own
   general counsel, unprompted, striking the Brandt matter from the firm's
   audit response and citing the confirmation by date, with no dispute
   pending. That is the beat that ends the argument.
5. **"We had a letter like that from Danforth and it still cost us
   $610,000. Why is this one different?"** The last sentence of each letter.
   Danforth's ran "for the term of the standstill agreement," which expired
   December 31, 2012; Torvane's "is not limited to any period and stands
   unless I withdraw it in writing." One is a gate, one is a wall — and the
   archive holds both, which is why the firm can tell them apart under
   pressure.

The number to say out loud at the end is **$3,675,000 — withdrawn in full**,
and the sentence to say with it is Evelyn Stanhope's from Email-40: **"Our
defense was not in our file. It was in our email."**
