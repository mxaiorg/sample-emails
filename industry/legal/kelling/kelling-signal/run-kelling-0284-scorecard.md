# Gate 5 — Live Blind Eval Scorecard: Kelling 2011-0284

**Run date:** September 1, 2026
**Corpus:** `kelling-0284` — 40 signal + 155 distractors + 6,000 filler = 6,195 messages
**Tool under test:** mxMCP `email_search` (mxMCP2)
**Grading key:** `grading-key-kelling-0284.md`
**Method:** each of the four grading-key queries issued verbatim as `Query`, with
field population as a competent agent would infer it. Follow-up searches were
issued only where the tool's own response disclosed partiality and told the
caller what to do about it.

**Total: 23 / 24. Demo passes** (Query 1 full on recall, precision and verdict).

| Query | Recall | Precision | Verdict | Subtotal |
|---|---|---|---|---|
| Q1 — primary needle | 2 | 2 | 2 | **6** |
| Q2 — system-of-record gap | 2 | 2 | 2 | **6** |
| Q3 — disambiguation trap | 1 | 2 | 2 | **5** |
| Q4 — causation | 2 | 2 | 2 | **6** |
| | | | | **23 / 24** |

---

## Query 1 — "Did Torvane ever confirm in writing…"

**Searches:** 3 (primary with `Pin=2011-0284`; 2013 audit window; migration mechanics).

**Recall — 2.** Every non-negotiable ID returned, most in the first call.

- `Email-10` — **rank 15 of the pinned block on call 1, full body plus complete
  extracted text of `Torvane_Scope_Confirmation_2011-06-09.pdf`.** The four
  operative clauses (limited to Ridgeline; "expressly outside the scope of your
  engagement"; limitations consequences accepted; "not limited to any period")
  all present verbatim in both the email body and the signed letter.
- `Email-6` ✓ (call 1), `Email-7` ✓ (recovered on the `Thread=Yes` pass),
  `Email-9` ✓, `Email-11` ✓ — the Casebridge Scope Note text quoted in full.
- `Email-30` ✓ with the complete Novarra matter-record attachment.
- `Email-22` ✓ with the complete migration scope notice, including §4's
  field-mapping note.
- `Email-35` ✓ with the full archive search report (all eleven exhibits A-1–A-11).
- `Email-17` ✓ (call 2) — the precedent, with `Email-16` and `Email-18` around it.
- Bonus swept: `Email-3`, `Email-23`, `Email-36`, `Email-37`, `Email-38`,
  `Email-39`, `Email-40`.

**Precision — 2.** Zero trap contamination on the cited set.

- No Danforth, no Maunsell, no Vollmer, no Ellard, no Berrisford, no
  Tenniel/Halbrook letters, no Torvane or Kelling name collisions.
- **All five in-file noise emails absent** (`Email-5`, `13`, `19`, `25`, `33`).
- Four Glassport messages (`D-3`, `D-4`, `D-18`, `D-103`) entered the pinned
  block — unavoidable, they carry the number verbatim — but the response
  disclosed the split *before* the documents: `"PARTIES: … garveystrom.com +
  prescottvane.com + torvaneindustrial.com (19), aldouscrane.com +
  glassportrealty.com (3) … An identifier is unique only within the office that
  issued it, so a number shared by two matters returns both — confirm the party
  before treating these as one file."` That is disclosure, not merge. No
  deduction.

**Verdict — 2.** Fully constructible from call 1 alone, and complete after call 3:
yes, in writing, June 9 2011, no time limit, never withdrawn; the firm had
identified the claim and recommended preserving it; the client applied the
carve-out itself in October 2013; and the DMS says otherwise because of the
February 2016 migration plus NOV-2119. Both halves available.

---

## Query 2 — "Is that the whole record of what the firm was engaged to do?"

**Recall — 2.** `Email-30` (with the full matter-record PDF text — the "Scope
field provenance: populated at migration from engagement-letter document class
(see NOV-2119)" row is right there in the extract), `Email-22`, `Email-23`,
`Email-10`, `Email-35` all returned. Bonus `Email-11`, `Email-29`, `Email-34`,
`Email-40` present.

**Precision — 2 (with one observation).** The dedicated Q2 search returned none
of the forbidden IDs. However, the *migration-mechanics* search — the natural
second call for this question — surfaced the 2017 cold-restore cluster
(`D-87`, `D-88`, `D-92`, `D-93`) and the 2022 certification thread
(`D-131`, `D-132`). This is the corpus working as designed rather than a
failure: those same messages state that the Casebridge backups were destroyed
September 29 2017 and that the journal archive has been the sole source since,
so they reinforce the correct verdict instead of inverting it. An answer that
presented the cold restore as *the* recovery path here would be wrong, but
nothing in the retrieved text invites that. Flagged as a demo-narration risk,
not scored down.

**Verdict — 2.** The premise is refutable directly from the returned text:
Novarra's record is a record of what survived the migration. `Email-22`'s
attachment gives the 2.1M-message CommsStore exclusion and the $412,000 vendor
remediation quote; `Email-23` gives "works as designed."

---

## Query 3 — "Show me every email on matter 2011-0284."

**Recall — 1.** Took three passes, and one required ID never surfaced.

- **Pass 1** (naive listing, `SearchType=emails`, `Pin`, no `K`): 9 of 24
  verbatim matches, explicitly disclosed as partial.
- **Pass 2** (`K=24`, party names in `Words`): 21 of 24 verbatim + `Email-1` as a
  close match. Torvane set now `Email-1,2,3,4,6,9,10,11,20,27,28,29,30,34,35,36,37,39`.
- **Pass 3** (`Thread=Yes`, May–Aug 2011 window): recovered `Email-7` and
  `Email-8`, **with zero distractors in the result set** — the cleanest single
  call of the run.
- **Miss:** `Email-12` (July 19 2011, arbitration demand filed, $11,400,000)
  never surfaced in any pass, including the pass whose `Words` named the
  arbitration demand explicitly. It appears only as Exhibit A-11 inside the
  `Email-35` report text. It is a supporting ID, not the needle, so per the
  rubric this is Partial rather than Fail.

**Precision — 2.** The collision is surfaced, never silently merged:

- Every call carried the PARTIES disclosure separating the two domains.
- `D-102` itself came back in results — *"this is legacy matter 2011-0284 — the
  Aldous & Crane number, retained at the 2014 merger… Do not confuse it with the
  Pittsburgh series."* The corpus hands the disambiguation to the model in plain
  English.
- **None of the near-miss numbers appeared** — no 2011-0248, 2011-0824,
  2011-0384, 2012-0284 in any pass. The transposition distractors did not leak.
- `D-148`/`D-149` (the internal Torvane disambiguation memo) came back as close
  matches. Not on any MUST-NOT list, and they help.

**Verdict — 2.** Two matters share the number; they separate cleanly by office
series and client, and the tool says so unprompted.

---

## Query 4 — "What actually went wrong, and what saved it?"

**Recall — 2, but only on the second attempt — see the finding below.**

- With `Pin=2011-0284`: **`Email-40` did not return.** The pinned block filled the
  entire response budget with the 18 best-ranked verbatim matches, and `Email-40`
  does not contain the string "2011-0284". The response disclosed exactly this:
  *"no close matches fit — the verbatim block filled the response, so messages
  that discuss it WITHOUT naming it are NOT shown here; raise or omit K to see
  them."*
- Without `Pin`, windowed to Nov 2024 – Dec 2025: **`Email-40` rank 1,
  `Email-31` rank 2.** Two results, both required, nothing else. `Email-22`,
  `Email-23`, `Email-35` all in hand from the Q1/Q2 passes.
- `Email-32` (Keystone reserves — bonus) never surfaced.

**Precision — 2.** Perfect. Zero Danforth (`D-108`/`109`/`112`/`113`/`116`/`117`),
zero Ellard (`D-133`–`141`), zero Berrisford (`D-145`/`147`/`150`–`155`), zero
`D-69`/`D-70`, and `Email-33` (Torvane Logistics) absent.

**Verdict — 2.** `Email-40` states both halves in one message and is returned
whole (`complete:true`), including the three executive-committee recommendations.

---

## Findings

**1. `Pin` is load-bearing for Q1–Q3 and actively harmful for Q4.**
The identifier pin guarantees the verbatim block first — which is why `Email-10`
lands on call 1 for Q1 — but on Q4 the same guarantee consumed the whole budget
and suppressed the one message that answers the question, because the post-mortem
never names the matter number. The tool disclosed the suppression in words a model
can act on, and dropping the pin fixed it immediately. **Demo guidance: pin the
number for the document questions, drop it for the causation question.** Worth
carrying into the build-process spec as a general rule — a synthesis needle that
deliberately omits the matter identifier will always lose to a full verbatim block.

**2. Attachment extraction is the reason Q1 scores full on the first call.**
`Torvane_Scope_Confirmation_2011-06-09.pdf`, `Novarra_Matter_Record_…pdf`,
`Journal_Archive_Search_Report_…pdf` and the Garvey Strom demand all came back as
complete extracted text, not filenames. The signed letter's four numbered
paragraphs are visible in the response. For a demo, this is the moment — the
viewer sees the actual letter, not a citation to it.

**3. The size-limit degradation is graceful and honest.** Seven messages had
attachment text stripped with the filenames retained and `truncated:true` set,
and the response named every affected message id. Nothing was silently dropped.

**4. The `Email-38` "ten emails" miscount never reached retrieval.** The returned
excerpt of `Email-38` truncates before that sentence, so the deliberate in-world
inaccuracy could not have confused an answer in this run. It remains available if
a demo reads the full response letter.

**5. Distractor pressure is real but well-behaved.** Every top-20 contained
distractors, none of them the dangerous ones. The Danforth near-miss twin — the
trap that inverts the verdict — did not appear in a single one of the seven
searches run. That is the strongest single precision result in the corpus series
so far; Danforth is designed to be the closest look-alike, and query framing that
names Torvane and Brandt appears to be enough to keep it out entirely.

## Recommendation

Ship it. Gate 5 passes at 23/24 with the single deduction on a supporting-email
recall miss in the least demo-relevant query. Run the demo with the Q1 → Q2 → Q4
sequence; Q3 is the weakest live moment (three passes to complete a listing) and
is better told than shown.
