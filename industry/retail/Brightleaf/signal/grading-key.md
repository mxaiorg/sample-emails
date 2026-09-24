# Demo Grading Key — Brightleaf Millbrook Field-Service Corpus — HARD (no roadmap)

The corpus is the **40-email signal thread** (`brightleaf-820-hard.md`) plus the
**154 hard-negative distractors** (`fieldservice-distractors.md`), salted into
6,000 messages of bulk filler (`fieldservice-bulk-filler.md`).

**What makes this the hard variant.** The standard build contains counsel's own
2026 write-up of the answer: the paralegal's search results, a chronology
attachment quoting the needle, an apportionment model dated from it, and
settlement correspondence describing it. A tool could find the needle by
reading that write-up and then verifying it. Here all of that is gone. In this
version counsel searched the archive by identifier, found nothing before the May
12 2021 service order, and concluded that the pleaded date holds (`Email-35`,
`Email-37`). The case is still open. The needle can only be reached through the
2020–21 record itself.

**Fair clues that remain, on purpose:** the complaint's ¶17 claims spoilage
"from March 2020" (`Email-30`); Vandehey's June 2020 reply mentions "aisle 12,
which Dorsey had asked about in March" (`Email-11`); her February 2021 reply
counts the asks as "March 2020, June 2020, November 2020 and now" (`Email-20`);
Brill's field note cites "the aisle 12 product complaints raised by the store in
March" (`Email-14` attachment); and `Email-34` names the store manager.

A correct answer is judged on four axes:

1. **Earliest awareness** — did it find the message that shows when a person
   first knew?
2. **Chronology** — is the sequence complete, in order, and attributed to the
   right people on the right dates?
3. **Precision** — did it avoid the look-alikes: earlier temperature complaints
   at the same store about *different* equipment, other customers' Rack B-3s,
   the Brightleaf name collisions, and other matters' chronologies?
4. **Verdict** — is the answer right, **including where it contradicts both
   the firm's service system and the firm's own counsel**?

Unprefixed IDs (e.g. `Email-5`) refer to `brightleaf-820-hard.md`. Emails 1–29
are identical to the standard build. IDs prefixed `D-` refer to
`fieldservice-distractors.md`.

---

## Signal reference map

| ID | What it is | Role |
|---|---|---|
| Email-2 | January 2020 temperature log, sent Feb 14. Shows B-3 excursions from Jan 8. Nobody read it. | Supporting — data, not awareness |
| Email-3 / Email-4 | The freezer door decal thread the needle is buried in | Supporting |
| **Email-5** | **Mar 11 2020, Kalloway to Vandehey: "the ice cream in aisle 12 is soft again. Second time this month." Fourth paragraph of an email about decal adhesive.** | **THE needle** |
| Email-6 | Mar 12 2020: "put in a service order through the portal" | Supporting — ask 1 of 4 |
| Email-7 | Brill: "nine times out of ten it is the door" | Supporting |
| Email-9 | Apr 21 2020 preventive maintenance visit: walked aisle 12, wrote nothing up | Supporting |
| Email-10 | Jun 18 2020, Ontiveros: frozen shrink high three weeks running | Supporting |
| **Email-11** | **Jun 19 2020, Vandehey: "including aisle 12 which Dorsey had asked about in March"** | **Cross-year link — the fair clue to March** |
| Email-13 | July 2020 log: 96 hours out of spec | Supporting |
| **Email-14** | **Sep 22 2020, Brill: discharge running 30° over; field note attached** | **The causation seed** |
| Email-15 | Quarterman parks it | Causation |
| Email-16 | Nov 4 2020, Kalloway: "we dumped two pallets" | Supporting |
| Email-17 | "this is the third time we have asked" | Supporting — ask 3 |
| Email-19 | Feb 11 2021, Bascombe: 4.1% vs a 1.2% average; "rule out equipment" | Supporting |
| **Email-20** | **Feb 12 2021: "the fourth time… March 2020, June 2020, November 2020 and now"** | **Cross-year link** |
| Email-21 | May 12 2021 service request — WO-114872 | The pleaded date |
| Email-23 – Email-25 | Diagnosis and quote; deferred to the capital cycle; the $18,400 option | Causation |
| Email-26 / Email-27 | Aug 18 2021 total failure | Outcome |
| Email-28 / Email-29 | $1.92M loss report; invoice 44718 | Supporting |
| Email-30 | The complaint: $4.1M; ¶14 pleads May 12 2021; ¶17 claims spoilage from March 2020 | Present-day thread start |
| **Email-32** | **Service-system export: `First Reported: 05/12/2021`; the 2023 migration dropped pre-2022 notes** | **The trap the tool must overcome** |
| Email-33 | Counsel's first assessment; the service agreement is attached | Supporting |
| Email-34 | Both witnesses have left; Quarterman remembers "2021" | Supporting |
| **Email-35** | **Counsel's identifier search: "earliest… is Achterberg's service request of May 12 2021"** | **The trap the tool must overcome — the firm's own wrong conclusion** |
| Email-36 | The Brill/Quarterman exchange surfaced to counsel | Causation |
| **Email-37** | **Wardlow: "their pleaded date holds"** | **The trap the tool must overcome** |

**Full 2020–21 trail:** Email-2 – Email-7, Email-9 – Email-11, Email-13 – Email-17,
Email-19 – Email-29.
**Full present-day trail:** Email-30 – Email-37.

**In-file noise that is NOT part of either trail:** Email-1 (maintenance
schedule), Email-8 (site access protocol), Email-12 (van leases), Email-18
(refrigerant reporting), Email-38 (expense system), Email-39 (archive retention
notice), Email-40 (holiday coverage).

---

## Deliberate in-world inaccuracies — do NOT grade as corpus defects

1. **Counsel's conclusion (`Email-35`, `Email-37`) is wrong, on purpose.** They
   searched by identifier, and the needle contains none. An evaluator that
   points out that counsel's method could not have found the needle is doing
   exactly what this variant tests.
2. **Quarterman remembers 2021 (`Email-34`, `D-143`).** His own September 2020
   email (`Email-15`) contradicts that.
3. **Brightleaf pleads May 12 2021 in good faith.** Nothing in the corpus
   suggests the pleading is dishonest.
4. **Kalloway's "second time this month" undercounts.** The logs show
   excursions from January 8.

**Benign if cited — do not deduct:** `D-54` (WO-109331 closed, the same visit as
`Email-14`) and `D-148` (Sowerby contrasting Quarterman's memory with his email).

---

## Query 1 — Primary ("prove the value")

> *"When did anyone at Brightleaf first show they knew there was a temperature
> problem at the Millbrook store?"*

**Correct verdict:** **March 11 2020.** Store manager Dorsey Kalloway wrote to
account manager Priscilla Vandehey, in the fourth paragraph of an email about
freezer door decal adhesive: *"the ice cream in aisle 12 is soft again. Second
time this month."* That is fourteen months and one day before the May 12 2021
date Brightleaf pleads, and before the date that Ledgerwood's own service system
**and its own counsel** both accept. The answer must say why both missed it.
The system dates first notice from ticket creation and lost pre-2022 notes in
the 2023 migration. Counsel searched by identifier, and the needle names no
equipment, ticket or contract. A full answer gives the ordered chronology and
treats the January 8 2020 log as data rather than awareness.

**MUST cite:**

- `Email-5` — the needle **(non-negotiable)**
- `Email-6`, `Email-10`, `Email-16`, `Email-19`, `Email-21` — the rungs
- **Bonus (full credit):** `Email-11` or `Email-20` (the contemporaneous clues
  that point to March), `Email-2` correctly labelled as data, `Email-3`/`Email-4`
  as the thread context, `Email-35` identified as the method that failed

**MUST NOT cite:**

- **Earlier temperature complaints at Millbrook about different equipment:**
  `D-10`/`D-11` (deli case, July 2019 — the highest precision risk in the
  corpus), `D-18` (beverage cooler), `D-27` (ice machine)
- **A later complaint:** `D-81` (a case reading warm after the rack was replaced)
- **Other Brightleaf stores:** `D-46`, `D-47`, `D-59`, `D-66`, `D-95`
- **Name collisions:** `D-8`, `D-31`, `D-34`, `D-51` (Brightleaf Farms);
  `D-71`, `D-72`, `D-87` (Brightleaf Plaza); `D-45`, `D-77`, `D-101`, `D-112`
  (other chains' Store 14)
- **The near-miss twin:** `D-28`, `D-29`, `D-32`, `D-36`, `D-40`, `D-147`
- **Recollection cited as evidence:** `D-143`, `D-144`, `D-145`
- **Other matters' chronologies:** `D-94`, `D-96`, `D-105`, `D-107`, `D-114`,
  `D-118`, `D-120`, `D-129`, `D-136`, `D-137`, `D-141`, `D-150`
- In-file noise: `Email-1`, `Email-8`, `Email-12`, `Email-18`, `Email-38`,
  `Email-39`, `Email-40`

**Scoring:** Pass if it cites `Email-5` and states March 11 2020. Fail if it
answers May 12 2021, takes counsel's conclusion in `Email-35`/`Email-37` as
correct, or gives `D-10`/`D-18`/`D-27` as the date. Surfacing those three and
explaining they concern different equipment earns bonus credit. **Traps cited
only as named exclusions are not deducted on any query.**

---

## Query 2 — The system-of-record gap

> *"Our service system says Brightleaf first notified us about the Millbrook
> freezer on May 12, 2021. Is that right?"*

**Correct verdict:** No. `First Reported` is populated from the order creation
date, and the 2023 migration dropped pre-2022 technician notes. First notice in
writing was March 11 2020, and Ledgerwood asked for a service order four times
before one was opened. The answer should also say that counsel's own search
reached the same wrong date because it searched for identifiers.

**MUST cite:** `Email-32`, `Email-5`, `Email-21`, and at least one ask
(`Email-6`, `Email-11`, `Email-17` or `Email-20`).
**Bonus:** `Email-35` (why counsel got it wrong), `Email-30` (¶17 claims
spoilage from March 2020 while ¶14 pleads May 2021), `Email-34`.
**MUST NOT:** `D-143`, `D-144`, `D-145`, `D-125`, `D-126`, `D-128`, `D-88`,
`D-106`.

**Note:** on this wording the needle ranks 17th in the BM25 pre-check (Gate 4),
because the word "freezer" matches the needle thread's subject. The match is
real — it is not a signpost — but it makes Q2 easier than Q1.

---

## Query 3 — The disambiguation trap

> *"Show me everything on Rack B-3 at Brightleaf Millbrook."*

Fifteen customers have a Rack B-3. The correct behavior is to scope to
Brightleaf Millbrook, or to say that several customers have one and separate
them.

**MUST cite (the correct set):** `Email-14`, `Email-15`, `Email-21` – `Email-29`.
**Bonus:** `Email-2`, `Email-13` (their attachments name the rack; the email
bodies don't), `Email-30`, `Email-32`, `Email-35`, `Email-36`.
**MUST NOT:** `D-6`, `D-12`, `D-19`, `D-24`, `D-39`, `D-50`, `D-67`, `D-75`,
`D-82`, `D-89`, `D-99`, `D-108`, `D-116`, `D-132` (other customers' Rack B-3);
`D-4`, `D-15`, `D-26`, `D-48`, `D-58`, `D-70`, `D-84`, `D-92`, `D-97`, `D-110`,
`D-123` (other CR-820s); `D-2`, `D-68`, `D-103`, `D-146` (SA-2019-4421).

The needle names no identifier, so this query cannot return it and should not.

---

## Query 4 — Causation / apportionment

> *"Who is responsible for the Millbrook Rack B-3 failure, and how should the
> seventeen months of spoilage be apportioned between Brightleaf and us?"*

**Correct verdict:** Both parties share responsibility, and the split follows
who knew what, when. The direct cause is the discharge valve Ledgerwood's own
technician found on September 22 2020 and his manager parked. Brightleaf knew
from March 11 2020, six months earlier. It was asked four times to open an order
and didn't. It then pushed the May 2021 quote into a capital cycle and ignored
the $18,400 repair that was within its own approval limit. That gives three
windows: **Brightleaf alone** (Mar 11 – Sep 22 2020), **both** (Sep 22 2020 –
May 12 2021) and **Ledgerwood formally** (May 12 – Aug 17 2021).

The archive has no agreed figures in this variant. A full-credit answer states
the windows and may apply them to the ¶17 total of $1,340,000, but must say that
any per-window amount is its own estimate. An answer that starts Brightleaf's
awareness at May 12 2021, and so puts all seventeen months on Ledgerwood, fails.

**MUST cite:** `Email-14`, `Email-15`, `Email-5`, `Email-23`, `Email-24`,
`Email-25`.
**Bonus:** the asks (`Email-6`, `Email-11`, `Email-17`, `Email-20`), `Email-9`,
`Email-26`/`Email-27`, `Email-33` (agreement §4.2 and §5.3).
**MUST NOT:** `D-42`, `D-43`, `D-79`, `D-80` (the product-loss exclusion);
`D-60`, `D-61`, `D-62`, `D-90` (the case where the contractor knew first);
`D-124`, `D-125`, `D-126`, `D-128`, `D-134` (the case where the pleaded date
held); `D-93`, `D-16`, `D-23`, `D-55` (Brill's findings at other sites); `D-91`,
`D-133`, `D-142` (other product-loss claims).

---

## Quick scoring rubric (per query)

| Axis | Full (2) | Partial (1) | Fail (0) |
|---|---|---|---|
| **Earliest awareness** | Right date, actor and source message | Right message, vague on date or actor | Misses `Email-5`, accepts May 12 2021, or gives a different-equipment complaint as the date |
| **Chronology** | All required rungs, in order, correctly attributed — **in the answer to this query** | Rungs present but out of order or misattributed | Fewer than five rungs, or the pleaded date placed first |
| **Precision** | No trap cited as part of the answer (named exclusions are fine) | One minor look-alike | Cites a different-equipment complaint, a name collision, another customer's Rack B-3 or another matter's chronology as part of the answer |
| **Verdict** | Correct, and explains why both the system and counsel got it wrong | Correct but shallow | Wrong |

4 queries × 4 axes × 2 points = **32 points per pass, 160 per five-pass run.**

**Demo passes** when Query 1 scores full on all four axes. A tool that passes
Query 1 here has found the needle without being told where to look.
