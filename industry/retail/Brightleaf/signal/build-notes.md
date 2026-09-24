# Phase 0 — `brightleaf-820` (the timeline archetype)

**Status:** design locked, **BUILT and DEMO-READY**, Sept 18 2026. Phases 1–6 complete.
All gates PASS. Gate 5 blind evaluation: **159/160**.

**Why this corpus exists:** the deliverable is **an ordered chronology with actors**, not a
document and not a ledger. The retrieval problem inverts: you need the *earliest weak
signal*, not the strongest match. Every prior corpus rewards a tool that ranks relevance;
this one punishes it, because the most relevant messages in the archive are all from the
wrong end of the story.

Accessibility is a design constraint, not a nice-to-have. A viewer needs no industry
knowledge: a grocery freezer stopped keeping ice cream frozen, somebody mentioned it in
passing fourteen months before anyone filed a ticket, and that one sentence moves
$2.86 million.

---

## 1. Setting

| | |
|---|---|
| Vertical | commercial refrigeration field service → regional grocery |
| Host firm (archive owner) | **Ledgerwood Refrigeration Services, Inc.**, `ledgerwoodref.com` — the **service contractor**, and the **defendant** |
| Counterparty | **Brightleaf Markets**, `brightleafmarkets.com` — 38-store regional grocery chain, customer since 2016 |
| Site | Brightleaf **Millbrook** store, **Store 14**. Also Brightleaf's regional frozen transfer hub for eleven stores — which is what makes a single-store loss an eight-figure-adjacent number |
| Equipment | **Rack B-3**, a **CR-820** compressor rack, installed 2013 |
| Contract | Service agreement **SA-2019-4412**, executed Jan 2019 |
| Work order | **WO-114872**, opened May 12 2021 — the date everyone believes is day one |
| Event | Brightleaf sues Feb 2026 for **$4,100,000**; mediation and settlement Aug–Sep 2026 |

**The archive is the defendant's own.** Every era-1 message has a Ledgerwood party on it.
That is a deliberate and load-bearing constraint: the product claim becomes *you can
reconstruct the other side's awareness from your own mail archive alone*, without a
single document from their custody. No discovery, no collection, no per-GB hosting.

---

## 2. The six beats, rewritten for this archetype

1. **A loss with a big number and a long tail.** $4.1M, seventeen months of intermittent
   failures, ending in a total compressor failure that took out the frozen hub overnight.
2. **The failure is real and partly ours.** This is not a story where the defendant walks.
   Ledgerwood's own technician found the failing discharge valve in September 2020 and his
   supervisor parked it. That email is in the same archive, and the chronology surfaces it.
3. **But the customer knew first, and in writing.** The earliest instance of awareness is
   not a complaint, a ticket, or a claim. It is one line at the bottom of an email about
   freezer door decals.
4. **They were told what to do, four times, and didn't.** Ledgerwood asked for a service
   order in March 2020, June 2020, November 2020 and February 2021. None was opened until
   May 2021.
5. **The system of record disagrees, and it is not lying.** Ledgerwood's field service
   platform reports `First Reported: 05/12/2021`, because that is when the ticket was
   created. A ticket system cannot know about the fourteen months of email that preceded
   it. Brightleaf pleads the same date in good faith.
6. **The chronology bounds the loss.** Not dismissal — apportionment across three windows
   defined by who knew what, when. $4,100,000 becomes $1,240,000.

### Why the verdict is apportionment and not victory

An earlier framing had the claim time-barred. It was cut. A viewer who watches the archive
rescue the party that actually broke the freezer roots against the product, and "AI helps
the guilty escape on a technicality" is the wrong thing to leave in the room. Making the
early email do **causation** work instead of **clock** work fixes it: nobody escapes, the
number just becomes correct, and the host firm learns something uncomfortable about itself
in the process.

---

## 3. The awareness ladder — the corpus's spine

Ten rungs. The chronology deliverable is this table with dates, actors and sources.

| # | Date | Actor | The signal | Strength | Carried in |
|---|---|---|---|---|---|
| L0 | Jan 8 2020 | *(machine)* | Millbrook temp log shows B-3 excursions | **data, not awareness** | attachment, unread |
| **L1** | **Mar 11 2020** | **Dorsey Kalloway**, Millbrook store manager | *"the ice cream in aisle 12 is soft again"* — last line of a decals thread | **THE needle** | body |
| L2 | Mar 12 2020 | Priscilla Vandehey, Ledgerwood AM | "put in a service order and we'll get someone out" | ask #1, unheeded | body |
| L3 | Jun 18 2020 | Marguerite Ontiveros, Brightleaf district manager | "frozen shrink high three weeks running, Dorsey thinks it's the cases" | awareness climbs the chain | body |
| L4 | **Sep 22 2020** | **Ynez Brill**, Ledgerwood technician | discharge valve on B-3 "running 30 degrees over… it needs to be scheduled" | **the causation seed — our own bad fact** | **attachment** |
| L5 | Sep 22 2020 | Roland Quarterman, Ledgerwood service manager | "we'll pick it up when they open something on B-3" | the escalation that died | body |
| L6 | Nov 04 2020 | Kalloway | "we dumped two pallets of frozen last week… can you just send somebody" | unambiguous, still no order | body |
| L7 | Feb 11 2021 | Truett Bascombe, Brightleaf loss prevention | *"before I write this up as theft I want to rule out equipment"* | **dollarized, and they say it themselves** | **attachment** |
| L8 | **May 12 2021** | Wendell Achterberg, Brightleaf facilities | the service request — **WO-114872** | the pleaded date | body |
| L9 | Aug 18 2021 | — | total failure of Rack B-3 | the loss | attachment |

### The three distinguished rungs

- **L1 is the needle, and it is unreachable by identifier.** The message contains no
  equipment name, no rack, no ticket, no contract number, and not the word
  "refrigeration." It is on a merchandising thread. Any tool that searches the way the
  problem is *described in 2026* will never find it. This is the whole demo.
- **L4 is the bad fact.** It proves the corpus is not a defense brief. It also carries
  its detail in an **attachment** — miss the attachment, miss the causation.
- **L7 is the precedent analogue.** There is no "they honored it once" in a timeline
  story. Its replacement is Brightleaf's own loss-prevention analyst, in Brightleaf's own
  words, treating Millbrook frozen as an equipment problem three months before the date
  Brightleaf later pleaded as first notice, and eleven months after its own store
  manager first raised it. Same rhetorical job: *they already said it
  themselves.*

### Signature quote (the needle, Email-5)

> "Also — the ice cream in aisle 12 is soft again. Second time this month. Frank says the
> case looks fine and the readout looks normal. Probably nothing but I told him I'd
> mention it to someone."

### The distinction the key must protect: data vs. awareness

L0 exists and matters, but it is **not** the answer. The monthly temperature logs were
transmitted on schedule and nobody opened them. An evaluator that surfaces the January 8,
2020 excursions and correctly labels them *machine data that no person acted on* earns
bonus credit. One that reports "first awareness: January 8 2020" without that
qualification is **wrong**, because the question is who knew, not what was recorded.

---

## 4. Locked number table

Every figure appears in at least two artifacts. **Compute once.** This table is the source.

| | |
|---|---|
| **Brightleaf claim, as pleaded** | **$4,100,000** |
| — interval spoilage, Mar 11 2020 – Aug 17 2021 (17.2 months) | $1,340,000 |
| — catastrophic loss, Aug 18 2021 (store frozen + hub inventory for 11 stores) | $1,920,000 |
| — business interruption and emergency transfer | $490,000 |
| — consequential (customer credits, brand) | $350,000 |

Interval spoilage split by awareness window — the three windows are the deliverable:

| Window | Span | Months | Spoilage | Who was on notice | Ledgerwood share |
|---|---|---|---|---|---|
| W1 | Mar 11 2020 – Sep 22 2020 | 6.4 | $498,000 | Brightleaf only | **0% = $0** |
| W2 | Sep 22 2020 – May 12 2021 | 7.7 | $600,000 | both | **50% = $300,000** |
| W3 | May 12 2021 – Aug 18 2021 | 3.1 | $242,000 | Ledgerwood, formally | **100% = $242,000** |
| | | **17.2** | **$1,340,000** | | **$542,000** |

| | |
|---|---|
| Catastrophic loss at comparative 35% (proximate cause is our unrepaired valve; their 14-month delay is failure to mitigate) | $672,000 |
| Business interruption at 35% | $171,500 |
| Consequential — withdrawn as unsupported | $0 |
| **Ledgerwood gross exposure** | **$1,385,500** |
| Offset — Invoice **44718**, Rack B-3 replacement, unpaid since Sept 2021 | −$147,500 |
| **Model output** | **$1,238,000** |
| **Settlement as executed** (rounded up for a mutual release and withdrawal of the consequential claim) | **$1,240,000** |
| **Reduction from the pleaded claim** | **$2,860,000** |

Supporting arithmetic that must not drift:

- $498,000 + $600,000 + $242,000 = $1,340,000 exactly.
- $1,340,000 + $1,920,000 + $490,000 + $350,000 = $4,100,000 exactly.
- $0 + $300,000 + $242,000 + $672,000 + $171,500 = $1,385,500 exactly.
- The $2,000 between the model output and the executed settlement is **deliberate** and
  stated as such in the term sheet. It is not a rounding drift.
- **The e-discovery counterfactual:** Brightleaf's counsel proposed a full ESI collection
  and hosted review. Wardlow's estimate was **$310,000** over ninety days. The archive
  search took an afternoon. This figure is the corpus's direct pitch against per-GB
  pricing and appears in Email-32 and Email-44.

---

## 5. Deliberate in-world inaccuracies

1. **Quarterman recalls "we first heard about it in 2021."** He is wrong; he replied to
   Brill's own valve finding in September 2020. Human memory, not a corpus defect. An
   evaluator that flags the contradiction between his recollection and his own email is
   exhibiting correct behavior.
2. **Brightleaf's complaint pleads first notice as May 12 2021 in good faith.** Their
   ticket record and ours agree, and both are incomplete in the same way. The pleading is
   not alleged to be dishonest anywhere in the corpus, and an evaluator that calls it
   fraud has over-read.
3. **The store manager writes "second time this month" on March 11 while the logs show
   excursions beginning February 8.** His count is low. Real people undercount.

---

## 6. Trap identifiers and two new distractor classes

Primary: **Rack B-3** — every supermarket in the region has one; ~12 other Ledgerwood
customers appear with theirs. Secondary: model **CR-820**, installed at ~11 other sites;
transposition pair **SA-2019-4412** / **SA-2019-4421**. Name collisions: Brightleaf
Markets / Brightleaf Farms (a produce supplier) / Brightleaf Plaza (a landlord customer) /
"Brightleaf" as a street name — plus **Store 14** at four other chains.

Beyond the trap classes in the process spec, the timeline archetype needs two that do not
exist yet:

- **The false early signal** (×6). Passing mentions of warm, soft or thawing product that
  are *not* this failure: a different Brightleaf store, or Millbrook but a different system
  — the deli case, the beverage cooler, the ice machine, a propped door. These are the
  precision heart of a timeline query. Everything that looks like early awareness and is
  not awareness of *this* failure.
- **The retroactive reconstruction** (×3). Someone in 2026 writing "as I recall we first
  heard about this back in 2019." Recollection that contradicts the contemporaneous record.
  A chronology must be built from documents, not memory, and a tool that dates an event
  from someone's later recollection has failed the archetype.

### The forwarded-2020-email trap

At least one era-2 message carries a **2020 email quoted inside a 2026 forward**. A
chronology built from message headers dates it 2026 and is wrong; the content is what
dates the event. This is the single most archetype-specific trap in the corpus and the
grading key must score it.

---

## 7. Grading changes

Axes become **earliest awareness / chronology / precision / verdict** — 4 queries × 4 axes
× 2 = **32 points**. Earliest awareness needs its own axis because it is the one item whose
loss invalidates everything downstream: a chronology that is complete, correctly ordered,
correctly attributed and starts on the wrong date is not a partial credit, it is the wrong
answer. Chronology scores ordering and actor attribution separately from finding L1.

This matches `ordway-4470` at 32 points but not on the same axes. Scores are comparable
within an archetype, never across.

Four queries:

1. **Primary** — "When did anyone at Brightleaf first show they knew there was a
   temperature problem at the Millbrook store?"
2. **System-of-record gap** — "Our service system says first notice was May 12, 2021. Is
   that right?"
3. **Disambiguation** — "Show me everything on Rack B-3." (twelve other customers)
4. **Causation / apportionment** — "Who is responsible for the August 2021 loss, and for
   how much of the seventeen months before it?"

---

## 8. Tool-behavior constraints designed around

- **Verbatim identifier filter.** The needle contains no identifier at all — not the rack,
  not the work order, not the agreement. Any query carrying `Rack B-3` or `WO-114872`
  therefore **cannot** return it. This is designed in, not worked around: the primary query
  must be tested with no identifier, and the demo script must not let a presenter type one.
- **Connective tissue present in every ladder email by design:** `Millbrook` and
  `Brightleaf`. Nothing else is universal. Test the primary query three ways — with
  "Millbrook", with "Brightleaf", with both.
- **Hop 1 depends on Email-34**, the paralegal instruction email, which hands a retrieval
  tool the vocabulary a store manager would actually use (*warm, soft, thawing, melting,
  not holding, dumping product, shrink*). It is realistic — it is exactly what a litigator
  says — and it is the corpus's answer to the lexical gap between how a problem is
  mentioned and how it is later asked about.
- **Ladder-email bodies held to 4–7 lines** so a nine-rung chronology answer does not
  overflow a `complete` call.

---

## 9. Gate changes

- Gate 4 runs in **two-hop mode** (see `gate4-two-hop.md`): the ladder is a set, so a
  single-needle rank is meaningless. Roadmap messages are Email-34, Email-35 and Email-37.
  Per-item sweep over all nine rungs.
- **Expected and must not be "fixed":** L1 will rank badly on the shared primary query.
  That is the phenomenon, not a defect — a message that ranked top-20 on "when did they
  first know there was a temperature problem" would have to describe itself as first
  notice of a temperature problem, and real ones never do.
- **New gate for this archetype:** every rung must be datable from its own content without
  reference to its header, because one of them is forwarded inside a later message.

---

## 10. Build layout

```
stories/brightleaf-820/brightleaf-820.md      54 emails      DONE
stories/brightleaf-820/attachments/           15 documents   DONE
stories/brightleaf-820/grading-key.md         32 points      DONE
stories/brightleaf-820/item-queries.txt       10 rungs       DONE - never ingest
stories/fieldservice-distractors/             154            DONE
stories/fieldservice-bulk-filler/             6,000          DONE, seed 440817
```

## 11. Gate results as built — 6,208 messages

| Gate | Result |
|---|---|
| 1 `validate_story.py` | PASS on all three files, signal with attachment cross-check |
| 1 `check_grading_key.py` | PASS, no warnings, key maps **54/54** signal emails |
| 2 `audit_corpus.py` | PASS. Cast leak 0, token leak 0, spelling american/american/american. Filler body diversity 80.1% |
| 3 content consistency | Two adversarial passes. **34 findings in the first, 8 more introduced by the fixes** — all closed |
| 4 `rank_check.py` two-hop | PASS on all four queries |
| 5 blind evaluation, live tool | **159/160** across five passes — see `test-results-2026-09-18-run1.md` |
| reproducibility | Filler reproduces byte for byte at `--seed 440817 --count 6000` |

**Gate 4 detail.** Hop 2: **10/10 rungs at rank 1** on their own vocabulary — every
rung is perfectly retrievable once you know to ask for it. Hop 1, roadmap into the
top-20: Q1 Email-36 at **12**, Q2 Email-36 at **2**, Q4 Email-40 at **10**.
**Zero filler in the top-20 on any query;** first filler at 49 / 27 / 53 / 67.
Q3 (disambiguation) runs single-needle: Email-21 at rank 2, top-20 is 12
distractors to 8 signal, which is the shape a disambiguation trap should have.

**The archetype's signature result:** on the primary query the needle Email-5 ranks
**around 500 of 6,208**, and that is correct, not a defect. A message that ranked
top-20 on "when did they first know there was a temperature problem" would have to
describe itself as first notice of a temperature problem, and real ones never do.
The whole corpus exists to demonstrate that gap.

## 12. Findings for the toolkit backlog

1. **The filler vocabulary budget is a hard constraint here, not a guideline.** The
   first filler build put the demo's working vocabulary (warm, soft, not holding,
   product temperature excursion, service order, temperature log, product loss) in
   **1,182 of 6,000** messages against the spec's ~250 target. Filler then competed
   for top-k on every generically-phrased query. Retuned to **475**, which passes.
   In the timeline archetype the demo query is *made of* common vertical
   vocabulary, so §8's "vocabulary proximity" rule and §9.4's "no filler in the
   top-20" rule pull against each other harder than in any previous corpus.
2. **`audit_corpus.py`'s subject-month window is wrong for this archetype.** A
   chronology email legitimately names a month years in the past
   ("earliest awareness March 2022" sent in January 2025). Two distractors trip it.
   Both are correct as written; the warn is expected and must not be "fixed".
3. **`validate_story.py` cannot see a wrong reference parent.** It checks that a
   reference resolves and points backward, not that it points at the message being
   answered. Twenty present-day emails were misthreaded and two threaded replies
   into in-file noise — Gate 1 passed all of it. Worth a check that matches an
   `RE:` subject to its parent's subject.
4. **Gate 4's "roadmap must reach the top-20" is meaningless on a disambiguation
   query,** where correct behavior is scoping rather than enumerating. Run Query 3
   single-needle.
5. **Gate 3 is the highest-yield gate in the toolkit and needs two passes.** The
   first found 34 defects, including a beat-destroying "fifteen months" that was
   three, a field note credited to the manager who buried it, and a system-of-record
   trap undermined by an archive appliance that was still readable on the day of the
   export. The fixes then introduced 8 more. Budget for the second pass.

Signal shape as built: **54 emails** — 29 accretion-era (Feb 2020 – Sep 2021),
25 present-day (Feb – Sep 2026), 7 in-file noise, 15 attachments (17 references).
The formal chronology attachment carries **ten** entries (L0–L9); Email-36, the
first-pass search result, compresses that to eight.

Cast — Ledgerwood: Vandehey (Account Manager), Brill (Service Technician, left 2023),
Quarterman (Service Manager, Northern District), Okonjo (Dispatch), Sowerby (Director of
Field Operations), Threlkeld (General Counsel, from 2024), Lisle (CFO), Pinkney (IT
Director). Brightleaf: Kalloway (Millbrook store manager, left 2022), Ontiveros (District
Manager), Achterberg (Director of Facilities), Bascombe (Loss Prevention), Draeger (VP
Store Operations). Outside counsel: Prentiss Wardlow LLP (Garrison Wardlow, Odile Menjivar)
for Ledgerwood; Thayer & Rounsaville LLP (Imogen Rounsaville) for Brightleaf. Adjuster:
Renshaw Claims Group (Vernon Renshaw).


## 13. Gate 5 — blind evaluation against the live tool, Sept 18 2026

Five blind-evaluator passes, each given only the four queries and `email_search`.
**159 of 160.** The single lost point was a chronology point on Query 1 in pass 1,
which found the needle and excluded every trap but answered with the earliest
instance alone instead of the ordered ladder.

**All five passes found `Email-5`** out of 6,208 messages, reached the right
verdict on the pleaded date, surfaced the adverse Brill/Quarterman exchange
rather than burying it, disambiguated Rack B-3 instead of merging it, and
reproduced the apportionment arithmetic intact.

**The sharpest trap did not fire.** `D-10`/`D-11` — the July 2019 deli case,
eight months *earlier* than the needle, same store, same two people, same
vocabulary, different rack — outranks the needle on the primary query, where the
needle does not surface at all. Every pass retrieved it and every pass correctly
excluded it as different equipment. Two went further and flagged that the
question is ambiguous on its face, answering the frozen-line reading while
stating the alternative. That is better behaviour than §7 anticipated, and the
key should credit it explicitly.

**Two corpus defects were found here that two adversarial Gate 3 passes missed.**
Both were ordering errors inside sentences whose every individual fact was true:
`Email-39` said the field note was parked after three refused asks when only two
had happened at that date, and `Email-36` called the needle "the last line of a
thread" when it is the last paragraph of an email with two messages after it.
Both fixed. **The lesson for the toolkit: blind evaluation is not only the demo
test, it is the cheapest remaining defect-finder after Gate 3, because an
evaluator reconstructing a timeline checks orderings that a consistency reviewer
checking facts does not.**

**Live-tool findings.**

- `email_search` does not substring-match email addresses. An entity whose name
  appears only in a domain is invisible to a name query — which is why the
  filler's ~30 counterparty organisations cannot be found by name. Harmless here,
  but a future filler build should put org names into some template bodies.
- The `Pin` constraint is confirmed empirically rather than predicted: pinning
  `Rack B-3` returns 31 verbatim matches and the needle is not among them.
- The pinned response's own PARTIES warning ("an identifier is unique only within
  the office that issued it") materially helped one pass scope correctly. The
  tool now supplies part of the behaviour Query 3 tests.
- Multi-term `SearchType: stat` false zeros are real and cost time during
  verification. Count with single clean terms only.