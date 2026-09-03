# Demo Grading Key — Kelling 2011-0284 Legal Practice Corpus

Use this to score a live AI-chat demo objectively. The corpus is the
**40-email signal thread** (`kelling-0284.md`) plus the **155 hard-negative
distractors** (`legal-practice-distractors.md`), salted into **6,000
bulk-filler messages** (`legal-practice-bulk-filler.md`).

A correct answer is judged on three axes:

1. **Recall** — did it surface the specific signal emails and attachments it needed?
2. **Precision** — did it *avoid* the look-alike traps (a second matter numbered
   2011-0284 from the Aldous & Crane merger, a near-identical but time-limited
   scope carve-out at Danforth Elastomers, the same general counsel writing the
   same kind of letter for a different employer, four unrelated companies named
   Torvane, two unrelated Kellings, and an anti-precedent claim where the same
   archive search honestly found nothing)?
3. **Verdict** — is the final natural-language answer correct, especially where
   the firm's own document management system would mislead?

Unprefixed IDs (e.g. `Email-10`) refer to `kelling-0284.md`.
IDs prefixed `D-` refer to `legal-practice-distractors.md`.

**This file must never be ingested into the corpus.** The indexer takes only
`kelling-0284.md` from the signal folder.

---

## Signal reference map

| ID | What it is | Role |
|---|---|---|
| Email-1 | Mar 24, 2011 — Tenniel engages the firm on the Kelling Station Unit 2 failures; names Brandt Thermal among parties to check | Supporting |
| Email-2 | Mar 30, 2011 — conflicts clearance; matter 2011-0284 assigned; Brandt named as potential adverse party | Supporting |
| Email-3 | Apr 4, 2011 — engagement letter, "claims arising out of the Kelling Station Unit 2 expansion project" — the broad wording the 2024 demand quotes | The trap's source document |
| Email-4 | Apr 7, 2011 — countersigned | Supporting |
| Email-5 | May 10, 2011 — CLE compliance reminder | In-file noise |
| Email-6 | May 17, 2011 — Wisner identifies the Brandt warranty claim and the limitations clock, memo attached | The causation seed |
| Email-7 | May 19, 2011 — Pellum recommends preserving the claim, in writing, and asks for instructions | The causation seed |
| Email-8 | May 26, 2011 — Tenniel: Brandt is the sole-source supplier; decision going to the CEO | Supporting |
| Email-9 | Jun 8, 2011 — Pellum's call memo: Torvane elects not to pursue; written confirmation requested | Supporting |
| Email-10 | **Jun 9, 2011 — Tenniel confirms in writing, with signed letter attached: the engagement is limited to the Ridgeline claims; the Brandt claim "is expressly outside the scope of your engagement"; the firm is asked to take no step to preserve it; the confirmation "is not limited to any period and stands unless I withdraw it in writing."** Attachment `Torvane_Scope_Confirmation_2011-06-09.pdf` | **THE needle** |
| Email-11 | Jun 10, 2011 — tickler closed "per client written instruction"; Casebridge Scope Note updated — the field the 2016 migration will drop | Causation |
| Email-12 | Jul 19, 2011 — arbitration demand filed against Ridgeline, $11,400,000 | Supporting |
| Email-13 | Sep 8, 2011 — office move notice | In-file noise |
| Email-14 | May 22, 2012 — hearing dates; mediation overture | Supporting |
| Email-15 | Oct 10, 2013 — Caulfield Roth FY2013 audit inquiry | Supporting |
| Email-16 | Oct 15, 2013 — draft audit response includes a precautionary Brandt paragraph, flagged for the client | Supporting |
| Email-17 | **Oct 17, 2013 — Tenniel strikes the Brandt paragraph: "as I confirmed to Arthur in writing on June 9, 2011, the Brandt Thermal warranty matter is expressly outside Prescott Vane's engagement" — the client applying the carve-out unprompted, citing it by date** | **Precedent** |
| Email-18 | Oct 18, 2013 — final audit response, Ridgeline arbitration only | Precedent support |
| Email-19 | Nov 12, 2013 — holiday card list | In-file noise |
| Email-20 | Feb 13, 2014 — Ridgeline settles at $4,850,000; matter closed | Cross-year link |
| Email-21 | Mar 12, 2015 — Tenniel leaving Torvane | Cross-year link |
| Email-22 | Feb 26, 2016 — Novarra cutover: pre-2014 CommsStore correspondence out of scope; journal archive is the retention copy | The trap the tool must overcome |
| Email-23 | Mar 15, 2016 — NOV-2119: Matter Scope derived from the engagement-letter class; Casebridge Scope Notes not carried; "works as designed" | Causation |
| Email-24 | Jun 15, 2018 — Pellum retires | Cross-year link |
| Email-25 | Aug 13, 2019 — parking garage notice | In-file noise |
| Email-26 | Oct 5, 2021 — Torvane acquired by Copeland Ridge Partners; relationship dormant | Cross-year link |
| Email-27 | Nov 14, 2024 — Garvey Strom demand: $3,675,000, quoting the engagement letter's broad scope. Attachments: demand letter + 2013 RTO performance study | Present-day thread start |
| Email-28 | Nov 14, 2024 — litigation hold, carrier notice, Brannock assigned | Supporting |
| Email-29 | Nov 15, 2024 — "I need the complete record of Matter 2011-0284" | Supporting |
| Email-30 | Nov 18, 2024 — Novarra holds fourteen documents and **no correspondence, no amendment, no limitation**; the Matter Scope field repeats the engagement letter. Attachment `Novarra_Matter_Record_2011-0284_2024-11-18.pdf` | The trap the tool must overcome |
| Email-31 | Nov 21, 2024 — on this record the demand's premise holds; Pellum remembers a carve-out but has nothing; everyone else is gone | Supporting |
| Email-32 | Dec 9, 2024 — Keystone reserves set; early resolution urged | Supporting (the stakes) |
| Email-33 | Dec 10, 2024 — Torvane Logistics warehouse lease (unrelated company, unrelated matter) | In-file noise |
| Email-34 | Dec 16, 2024 — Grady: the mail journal archive, journaling since October 2007, never migrated; targeted search proposed | The product moment (setup) |
| Email-35 | Jan 9, 2025 — search results: the eleven-message 2011 sequence, attachments intact, signed confirmation recovered. Attachment `Journal_Archive_Search_Report_2025-01-09.pdf` | The product moment |
| Email-36 | Jan 9, 2025 — the June 9, 2011 email quoted verbatim; Rule 1.2(c) analysis | Supporting |
| Email-37 | Jan 13, 2025 — second pass surfaces the October 17, 2013 audit-response email | Precedent (recovery) |
| Email-38 | Jan 21, 2025 — response letter served with the production. Attachment `PV_Response_Letter_2025-01-21.pdf` | Formal rebuttal |
| Email-39 | Feb 24, 2025 — claim withdrawn in its entirety. Attachment `Torvane_Withdrawal_Letter_2025-02-24.pdf` | Outcome |
| Email-40 | Mar 10, 2025 — post-mortem: indemnity $0, defense $92,400; both halves of the causation story; the archive as the only witness | Outcome |

**Full 2011 matter trail:** Email-1 – Email-4, Email-6 – Email-12.
**Full 2013 precedent trail:** Email-15 – Email-18.
**Full migration and causation trail:** Email-21 – Email-24, Email-26.
**Full present-day trail:** Email-27 – Email-32, Email-34 – Email-40.

**In-file noise that is NOT part of any trail:** Email-5 (CLE reminder),
Email-13 (office move), Email-19 (holiday cards), Email-25 (parking garage),
Email-33 (Torvane Logistics LLC — a different company on a different matter).

**Deliberate in-world inaccuracy — do NOT grade as a corpus defect:**
Email-38 describes the production as "the ten emails from the 2011 matter
sequence." The sequence is **eleven**. Email-35, the search report, and the
response letter itself all state eleven correctly. Real productions contain
human miscounts. An evaluator that notices the discrepancy and reports it is
behaving correctly and should be credited, not penalized.

---

## Query 1 — Primary ("prove the value")

> *"Did Torvane ever confirm in writing that the Brandt warranty claim was
> outside the scope of Prescott Vane's engagement on the Kelling Station
> matter, or did the firm really let a client's claim expire on its watch?"*

**Correct verdict:** Yes, in writing, on **June 9, 2011**. Torvane's General
Counsel Rosalind Tenniel wrote to Arthur Pellum, copying the company's VP of
Engineering, attaching a signed letter on Torvane letterhead, confirming that
the engagement under Matter 2011-0284 was limited to the claims against
Ridgeline Constructors; that Torvane had considered the Brandt Thermal warranty
claim and elected not to assert it; that the claim was "expressly outside the
scope of your engagement," with the firm asked to take no step to evaluate,
preserve, or pursue it; that the company had been advised, orally and in
writing, of the limitations consequences and accepted them; and that the
confirmation was "not limited to any period and stands unless I withdraw it in
writing." It was never withdrawn. The firm had in fact identified the claim
(May 17, 2011), analyzed the limitations period, and recommended preserving it
by tolling agreement (May 19, 2011) — the client, after advice, instructed
otherwise. In October 2013 the same General Counsel enforced the limitation
herself, striking the Brandt matter from the firm's draft audit response and
citing the June 9, 2011 confirmation by date.

The answer must also state **why the firm's own document system says
otherwise**: the February 2016 Casebridge–Novarra migration excluded matter
correspondence filed before January 1, 2014, and Novarra's Matter Scope field
was populated from the engagement letter alone (NOV-2119), so the DMS shows an
unlimited engagement and holds no trace of the limitation. The confirmation
survived only in the mail journal archive, which was never migrated.

**MUST cite (recall):**

- `Email-10` — the confirmation, with `Torvane_Scope_Confirmation_2011-06-09.pdf` (non-negotiable)
- `Email-6` or `Email-7` — the firm identified the claim and recommended preserving it
- `Email-30` — what Novarra actually holds
- `Email-22` — why it holds only that
- `Email-35` — the journal archive recovery
- `Email-17` — the client's own 2013 application of the carve-out
- **Bonus (full credit):** `Email-9` (the call memo), `Email-11` (tickler
  closed per written instruction), `Email-36` (the verbatim quotation),
  `Email-37` (the precedent's recovery), `Email-38`–`Email-39` (rebuttal and
  withdrawal), `Email-3` (the broad wording the demand quotes)

**MUST NOT cite (precision fails):**

- **The near-miss twin** — Danforth Elastomers' scope confirmation of
  **May 25, 2011**, near-identical words from the same partner's client, but
  expressly limited "for the term of the standstill agreement ... which
  expires December 31, 2012": `D-1`, `D-5`, `D-6`, `D-7`, `D-41`, `D-42`,
  `D-44`, `D-108`, `D-109`, `D-112`, `D-113`, `D-116`, `D-117`. `D-6` is the
  closest look-alike in the corpus, and citing it as the Torvane confirmation
  inverts the verdict — that carve-out lapsed and cost the firm $610,000.
- **The other 2011-0284** — the legacy Aldous & Crane real-estate matter
  (Glassport Realty Partners, Harrisburg): `D-2`, `D-3`, `D-4`, `D-18`,
  `D-22`, `D-102`, `D-103`, `D-104`, `D-105`, `D-114`
- **Right person, wrong employer** — Rosalind Tenniel writing the same kind of
  scope-confirmation letter as GC of Halbrook Fasteners from 2016: `D-79`,
  `D-80`, `D-82`, `D-83`, `D-90`, `D-99`, `D-100`, `D-101` (`D-82` even
  repeats her "not limited to any period" formula)
- **The qualified twin** — Maunsell Paper's Schedule 1 exclusion list: `D-27`,
  `D-28`, `D-29`, `D-60`, `D-61`, `D-71`
- **The inverted premise** — Vollmer Foundry, where the engagement covered
  everything and the firm tolled every claim: `D-8`, `D-9`, `D-15`, `D-34`,
  `D-47`, `D-54`, `D-55`
- **The anti-precedent** — Ellard Marine, where the same archive search
  honestly found no confirmation and the firm paid $1,150,000: `D-133`,
  `D-134`, `D-135`, `D-136`, `D-137`, `D-138`, `D-139`, `D-140`, `D-141`
- **Name collisions** — Torvane Marine Group, Torvane Capital Partners,
  Torvane Logistics, Kelling Ridge Apartments, Kelling County IDA, Brandt
  Paving: `D-94`, `D-95`, `D-96`, `D-115`, `D-144`, `D-146`, `D-122`,
  `D-124`, `D-125`, `D-127`, `D-128`, `D-129`, `D-142`, `D-143`, `D-106`,
  `D-107`, `D-110`, `D-111`, `D-120`, `D-64`, `D-65`, `D-72`, `D-73`,
  `D-74`, `D-118`, `D-119`, `D-121`
- In-file noise framed as part of the claim: `Email-5`, `Email-13`,
  `Email-19`, `Email-25`, `Email-33`

**Scoring:** Cites `Email-10` **and** reaches the "yes, confirmed in writing,
without time limit, and the DMS is wrong because of the migration" conclusion =
pass. Misses `Email-10`, or answers "the engagement covered the Brandt claim"
or "no written limitation exists" = fail. Any trap citation is a precision
deduction; citing `D-6` as the operative confirmation is a precision **and** a
verdict failure.

---

## Query 2 — The system-of-record gap

> *"Novarra shows matter 2011-0284 with the engagement letter, fourteen
> documents, and a Matter Scope of 'claims arising out of the Kelling Station
> Unit 2 expansion project' — no amendment, no limitation, no correspondence.
> Is that the whole record of what the firm was engaged to do?"*

**Correct verdict:** The premise is false and the tool must say so. Novarra's
record is a record of **what survived the February 2016 migration**, not of
what happened. Matter correspondence filed before January 1, 2014 (the
CommsStore module) was out of the migration's scope, and the Matter Scope field
was populated from the engagement-letter document class alone — NOV-2119
confirmed that post-engagement scope changes recorded only in correspondence
or in Casebridge's free-text Scope Note field were not carried, and was closed
"works as designed." The actual record — the June 9, 2011 written confirmation
and signed letter, the surrounding advice, and the Casebridge scope note
described in Email-11 — exists in full in the mail journal archive, which was
never migrated and is the firm's retention copy for email.

**MUST cite:** `Email-30` (primary), `Email-22`, `Email-23`, `Email-10`,
`Email-35`. **Bonus:** `Email-11` (the scope note the field dropped),
`Email-29`, `Email-34`, `Email-40`.

**MUST NOT cite:** `D-87`, `D-88`, `D-89`, `D-91`, `D-92`, `D-93` (the 2017
Casebridge cold-restore recoveries — that path died when the backups were
destroyed on September 29, 2017, so presenting it as the answer here is
wrong); `D-130`, `D-131`, `D-132` (the 2022 certification thread, which
post-dates and does not concern this matter); `D-57`, `D-58`, `D-59` (the
2014 records-policy revision); `D-102`–`D-105` (the other 2011-0284's
migration discussion). Concluding "the engagement was unlimited" or "the
record is complete" is a verdict failure regardless of citations.

---

## Query 3 — The disambiguation trap

> *"Show me every email on matter 2011-0284."*

The corpus contains **two matters numbered 2011-0284 by design**. The
Pittsburgh series number belongs to Torvane Industrial Group / Kelling Station
Unit 2. The legacy Aldous & Crane (Harrisburg) number belongs to the Glassport
Realty Partners shopping-center refinance — legacy matters kept their numbers
at the January 2014 merger, and `D-102` says so explicitly. Near-miss numbers
are also in active use: 2011-0248 (Weatherell Foods), 2011-0824 (Loxley Tool &
Die), 2011-0384 (Marlbank Optics), 2012-0284 (Dorrance Properties), and the
firm's own docketing memos (`D-25`, `D-26`) discuss transposition errors among
them.

**Correct behavior:** either scope to the Torvane matter from conversation
context, or explicitly note that two matters share the number and disambiguate
by office series and client — **never silently merge them**.

**MUST cite (the Torvane 2011-0284 set):** `Email-1` – `Email-4`,
`Email-6` – `Email-12`.
**Bonus:** the later messages that carry the number — `Email-14` – `Email-18`,
`Email-20`, `Email-27` – `Email-30`, `Email-34` – `Email-37`.

**MUST NOT cite:**

- The Glassport / Aldous & Crane 2011-0284: `D-2`, `D-3`, `D-4`, `D-18`,
  `D-22`, `D-102`, `D-103`, `D-104`, `D-105`, `D-114`
- The near-miss numbers: `D-10`, `D-11`, `D-12`, `D-33`, `D-43` (2011-0248);
  `D-19`, `D-20`, `D-21`, `D-38`, `D-62` (2011-0824); `D-16`, `D-17`,
  `D-23`, `D-24` (2011-0384); `D-30`, `D-31`, `D-32`, `D-35` (2012-0284)
- In-file noise: `Email-5`, `Email-13`, `Email-19`, `Email-25`, `Email-33`

**Scoring:** Returning a merged set that includes any Glassport message
without flagging the collision = precision fail. Returning only the Glassport
set = recall **and** verdict fail.

---

## Query 4 — Causation / responsibility

> *"The firm came within weeks of negotiating a settlement on a $3,675,000
> malpractice claim that turned out to have no merit. What actually went
> wrong, and what saved it?"*

**Correct verdict:** Nothing went wrong in 2011 — the opposite: the firm
identified the claim, put the limitations risk in writing, recommended
preserving it, and obtained a written, signed, open-ended scope limitation
when the client chose otherwise. What went wrong is everything after, and no
single email before the post-mortem states it whole. The 2016 migration
dropped pre-2014 matter correspondence and populated Novarra's Matter Scope
from the engagement letter alone, so the firm's own system asserted, with
confidence, an unlimited engagement (Email-22, Email-23, Email-30). By 2024
every person who knew better was gone — Pellum retired, Tenniel gone from
Torvane, Wisner in-house, Hagerman deceased (Email-31) — and Torvane's side
had lost the same correspondence to its own platform changes and the 2021
acquisition (Email-39). What saved it was the mail journal archive — never
migrated precisely because it is an archive rather than a system of record —
which produced the 2011 sequence and the 2013 audit correspondence,
hash-verified, in a fourteen-minute search (Email-34, Email-35, Email-37).
Email-40 states both halves and the resulting process changes.

**MUST cite:** `Email-40` (non-negotiable — the only message that states both
halves), `Email-22`, `Email-23`, `Email-31`, `Email-35`. **Bonus:**
`Email-30`, `Email-32` (the stakes), `Email-34`, `Email-37`, `Email-39`,
`Email-11`.

**MUST NOT cite (precision fails):**

- `D-108`, `D-109`, `D-112`, `D-113`, `D-116`, `D-117` — the Danforth claim,
  where a **time-limited** carve-out lapsed and the firm paid $610,000.
  Attributing "the carve-out expired" or "the tickler was closed on an
  unconfirmed assurance" to the Torvane matter is the inverted answer and a
  verdict failure as well as a precision failure.
- `D-133` – `D-141` — Ellard Marine, where the archive search found nothing
  and the firm paid; concluding the archive "usually" proves such claims, or
  citing Ellard as this matter's outcome, is wrong.
- `D-145`, `D-147`, `D-150` – `D-155` — Berrisford Metals, the *other*
  November 2024 demand, resolved on entirely different grounds.
- `D-69`, `D-70` — the 2015 docketing near-miss on an unrelated appeal.
- `Email-33` — a different Torvane on a different matter.

Attributing the near-miss to negligence in 2011, to a lapsed or time-limited
carve-out, or to the archive being incomplete, is a verdict failure.

---

## Quick scoring rubric (per query)

| Axis | Full (2) | Partial (1) | Fail (0) |
|---|---|---|---|
| **Recall** | All required IDs plus the key attachment | Misses a supporting email but has the query's core needle | Misses the query's non-negotiable ID |
| **Precision** | Zero trap citations | One minor look-alike | Cites the Glassport 2011-0284, the Danforth confirmation, a Tenniel/Halbrook letter, a Torvane or Kelling name collision, or the Ellard search as if it were this matter |
| **Verdict** | Correct, and explains the system-of-record gap | Correct but shallow | Wrong (e.g. "the engagement covered the Brandt claim", "no written limitation exists", "the carve-out had expired") |

4 queries × 3 axes × 2 points = **24 points**.

**Demo passes** when Query 1 scores full on recall, precision and verdict.
