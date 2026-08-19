# mxMCP Scored Run — Marchwood 2011-0447 Corpus

**Date:** August 19, 2026  
**Tool:** `mxMCP2.email_search`  
**Grading key:** `gradingkeymarchwood0447.md`  
**Searches issued:** 8 (4 primary, 4 follow-up/completion)  

---

## Headline

**24 / 24.** All four queries score full on recall, precision and verdict.
Query 1 — the demo-pass gate — cites `Email-11` with its attachment and reaches
the "yes, in writing, and the system is wrong because of the migration"
conclusion. **Demo passes.**

| Query | Recall | Precision | Verdict | Total |
|---|---|---|---|---|
| 1 — Did Marchwood ever agree in writing? | 2 | 2 | 2 | **6** |
| 2 — System-of-record gap | 2 | 2 | 2 | **6** |
| 3 — Every email on 2011-0447 | 2 | 2 | 2 | **6** |
| 4 — Causation / responsibility | 2 | 2 | 2 | **6** |
| | | | | **24 / 24** |

---

## Query 1 — "Did Marchwood ever agree in writing… or did the 2011 examination close with no findings?"

**Answer produced:** Yes, in writing, on **June 2, 2011**. Marguerite Vasseur-Kyle
(CCO) wrote to examiner Desmond Whitlatch accepting Item 4 of the April 20, 2011
deficiency letter in examination 2011-0447; all 214 affected accounts moved to
Signal Peak Trust Company effective June 1, 2011 under agreements giving
Marchwood no withdrawal authority; the direct fee-debit instruction was
discontinued firm-wide ("we will not resume it"); and Marchwood undertook to
apply the same treatment to accounts acquired or onboarded in future — an
undertaking "not limited to calendar year 2010 or to any other period and…
given without an expiration date." The letter asks the staff to treat it as the
commitment on which closing is conditioned, and the June 28, 2011 closing letter
does exactly that: "Based on the corrective actions described in your response."

The answer also states **why the Commission's own system says otherwise**: the
March 2016 EXAMTRAC→SENTRY cutover migrated only the summary record and indexed
final letters for examinations closed before January 1, 2014, and mapped legacy
disposition C-4 (closed on registrant undertaking) onto C-2 (closed, no further
action). SENTRY therefore holds a summary row and the closing letter and nothing
else — a record of what survived a migration, not a record of what happened.

**Recall — required IDs, all cited:**

| Key ID | Retrieved as | Attachment |
|---|---|---|
| `Email-11` **(non-negotiable)** | Jun 2, 2011 — Vasseur-Kyle → Whitlatch, "Item 4 - corrective action and undertaking" | `Marchwood_Undertaking_Letter_2011-06-02.pdf` ✅ |
| `Email-4` | Apr 20, 2011 — Achterberg → Penhaligon, deficiency letter | `Marchwood_Deficiency_Letter_2011-04-20.pdf` |
| `Email-13` | Jun 28, 2011 — closing letter | `Marchwood_Closing_Letter_2011-06-28.pdf` |
| `Email-30` | Nov 15, 2024 — Bricenio, "what SENTRY holds is two things" | — |
| `Email-19` | Mar 11, 2016 — Ellenbogen, cutover + scope notice | `SENTRY_Migration_Scope_Notice_2016-03-11.pdf` |
| `Email-34` | Jan 14, 2025 — journal archive search results | `Journal_Archive_Search_Results_2025-01-14.pdf` |
| `Email-35` | Jan 16, 2025 — Aubuchon, "The June 2 letter", quoted verbatim | — |

**Bonus cited (full credit):** `Email-16` (2013 precedent, unprompted, with the
Hollis Grange memorandum), `Email-9` (why the staff wanted an open-ended
undertaking), `Email-12` (the C-4 closing recommendation), `Email-38` (the
opposition), plus `Email-3`, `Email-20`, `Email-40`.

**Precision — zero trap citations.** Look-alikes that appeared *in results* and
were correctly excluded from the answer: Vandergrift Rowe 2011-0463 (its C-4
closing recommendation ranked in the same result set — its undertaking expires
December 31, 2012), Ottoway Trask 2012-0331 / 3-22014, and the 2012-0118
C-4 record. None was attributed to Marchwood.

**Verdict:** correct, with the migration explanation. **Full.**

---

## Query 2 — "…disposition C-2, closed no further action… Did the staff ever require corrective action?"

**Answer produced:** The premise is false, and the answer says so. A six-item
deficiency letter issued April 20, 2011; the examination closed on a written
undertaking and was recorded as **C-4 — closed on registrant undertaking**
(`Email-12`, explicitly: "the disposition code should be C-4… and not C-2"). Two
separate 2016 defects produced what the system now shows: pre-2014 correspondence
and work papers were out of migration scope, and C-4 had no counterpart in the
new code set and was mapped onto C-2. Priya Raghunathan raised it at the time
("it deletes the one fact the next examiner needs, and it does so on exactly the
examinations whose correspondence also did not migrate"); it was logged as
SENTRY-2214 and closed **low impact, will not fix**. Absence of a deficiency
letter from SENTRY is not evidence that none was issued — the migration scope
notice says so in terms.

**Recall:** `Email-30` (primary) ✅, `Email-19` ✅, `Email-20` ✅, `Email-21` ✅,
`Email-4` ✅, `Email-11` ✅, `Email-12` ✅. Bonus: `Email-13` ✅, `Email-34` ✅.
(`Email-33` returned as a header-only stub under the transport size limit —
subject "Marchwood 2011 - the correspondence was never destroyed" — body not read
this run. Bonus item only; no recall impact.)

**Precision — zero trap citations.** The Ottoway Trask family (`D-126`/`D-132`
class: Osunde's 3-22014 withdrawal recommendation, Bricenio's 2012-0331 note) and
the 2012-0118 C-4 record (`D-104`/`D-106` class) both ranked in this result set
and were held out of the answer as different matters. The Ottoway Trask messages
are in fact the *inverse* case — C-1, not C-2, and a genuinely clean file — and
citing them would have inverted the answer.

**Verdict:** correct — corrective action was required, and the system's silence is
explained. **Full.**

---

## Query 3 — "Show me every email on examination 2011-0447."

**Behavior:** the query was first run **unscoped**, deliberately. The tool
disclosed the collision itself in its PARTIES note — verbatim matches split
across `marchwoodam.com + tiradohobbs.com`, `braxtonferrer.com +
thackstonmeade.com` and `ballentineroe.com`, with the warning that "an identifier
is unique only within the office that issued it." The answer disambiguates
explicitly rather than merging: **Philadelphia's 2011-0447 is Marchwood Asset
Management (custody); Denver's 2011-0447 is Braxton-Ferrer Advisors LLC
(advertising and performance presentation).** A scoped second pass returned all
16 verbatim 2011 messages — 11 Marchwood, 5 Braxton-Ferrer — cleanly separable by
office and registrant.

**Recall — the Philadelphia set, complete:**

`Email-1` (Feb 7, notice + document request) · `Email-3` (Mar 18, preliminary
custody analysis) · `Email-4` (Apr 20, deficiency letter) · `Email-5` (Apr 26,
Tirado extension request) · `Email-6` (Apr 28, extension granted to June 3) ·
`Email-7` (May 19, interim response) · `Email-8` (May 24, staff position on Item
4) · `Email-9` (May 26, internal — what to ask for) · `Email-10` (Jun 1, call
memorandum) · `Email-11` (Jun 2, the undertaking) · `Email-12` (Jun 7, C-4
recommendation) · `Email-13` (Jun 28, closing letter). **12 of 12.**

`Email-8` did not rank in the scoped list but was disclosed in `missingRelated`
and fetched by MsgId — the tool named the gap rather than hiding it.

**Bonus cited:** `Email-25`, `Email-29`, `Email-30`, `Email-34` (its search-terms
table names Denver's 2011-0447 and the transpositions 2011-0477/2011-0417/
2010-0447 outright), `Email-37`, `Email-38`. **Not surfaced this run:**
`Email-17` (Oct 29, 2013 national numbering notice) — bonus only, no scoring
impact; the collision was established from `Email-34` and from the Denver
correspondence itself.

**Precision:** Braxton-Ferrer messages were returned but **flagged as a separate
Denver examination, never folded into the Marchwood set** — the behavior the key
requires. No 2010-0447, 2012-0447, 2011-0417/0477 or 2011-0463 message was
included. In-file noise (`Email-2`, `-15`, `-23`, `-27`) did not rank and was not
cited.

**Verdict:** correct — collision named, sets separated. **Full.**

---

## Query 4 — "Why did the custody violations recur after 2016, and who is responsible?"

**Answer produced — both halves.** Responsibility for the violation is
Marchwood's: the 2011 undertaking had no expiration and by its terms reached
accounts acquired or onboarded later; in Q1 2019 the firm adopted a third-party
billing platform and re-added a withdrawal-authorization clause in substantially
the terms of the one removed in 2011, running to September 2023 across 431
accounts / ~ \$497m, of which **138 (~ \$38.5m) were acquired or onboarded after June
2, 2011 and sat squarely inside the undertaking**. The May 2011 custody procedure
was not carried into the 2017 manual; the firm's own 2017 move off its legacy
archiving platform lost the correspondence; the CCO who gave the undertaking left
in February 2016.

The second half, which no single email states: the Commission's own systems
removed every trace that the undertaking existed. The 2016 migration left pre-2014
correspondence behind, and the C-4→C-2 mapping deleted the one field that would
have told the next examiner something had been promised. In August 2019 the risk
model scored Marchwood in the bottom quartile — **correctly, on inputs that said
"the last examination closed with no further action and no open items of record"**
— and the firm fell off the FY2020 candidate list. The follow-up flag Whitlatch
set in 2011 was never scheduled. Nobody knew until the March 2023 tip.

**Recall:** `Email-40` **(non-negotiable)** ✅ — the settled order and Ostrowski's
post-mortem, the only message stating both halves ("It came back, after the
compliance officer who gave the undertaking left, on a firm whose risk score said
there was nothing here because the disposition code said there was nothing
here"). `Email-20` ✅, `Email-21` ✅, `Email-22` ✅, `Email-19` ✅, `Email-9` ✅
(Whitlatch, May 26, 2011: "If we take the narrow remediation and the practice
comes back after this compliance officer leaves, the record will show we closed
with no findings" — the causation seed, retrieved and quoted).
Bonus: `Email-11` ✅, `Email-12` ✅, `Email-18` ✅, `Email-25` ✅, `Email-39` ✅.

**Precision — zero trap citations.** Critically, the answer does **not** attribute
the recurrence to a lapsed or time-limited undertaking. Vandergrift Rowe's
genuinely-expiring undertaking (`D-112`/`D-142`/`D-147` class) surfaced in an
earlier search in this same session and was not carried into this answer.
Ellersby Kinnaird's Schedule A limitation, Corrigan Weld and Ottoway Trask were
likewise excluded, as was `Email-27` (Marchwood Capital Partners LP).

**Verdict:** correct on both halves — firm responsibility plus the
system-of-record failure. **Full.**

---

## Corpus observations from this run

1. **The in-world miscount was caught.** `Email-37` (Jan 22, 2025 supplemental
   production cover) describes "the eleven emails from the 2011 examination
   sequence"; the sequence is **twelve**, and the production index attached to
   that same message lists Docs 1–12 for 2011 plus Doc 13 for October 2013.
   `Email-34` and the Division's opposition ("that letter, and eleven other
   documents") state it correctly. Per the key this is deliberate and is reported,
   not graded as a defect.

2. **Pin discipline is doing the work.** One search in this run was issued
   deliberately without `Pin` (CCO-departure question, 2016 date window). It
   returned 50 messages, of which **48 were bulk filler** — a wall of
   near-identical "Change of Chief Compliance Officer" and EX-2016-51xxx
   deficiency-letter traffic. `Email-18` and `Email-19` survived only because the
   date window was tight. The same question with `Pin` set returns signal at rank
   1. This is the single clearest retrieval finding of the run.

3. **The disambiguation disclosure is load-bearing.** On the bare-number query the
   server volunteered the party split and the "unique only within the office that
   issued it" warning before any answer was drafted. Query 3 is not passable by
   ranking alone — an agent that ignores that disclosure merges Denver into
   Philadelphia and fails precision.

4. **`missingRelated` prevented a recall miss.** `Email-8` (May 24, 2011 staff
   position on Item 4) never ranked into a result set across eight searches, but
   was named in `missingRelated` twice and fetched by MsgId. Without that channel
   Query 3 would have returned 11 of 12.

5. **Distractors are ranking where they should.** Vandergrift Rowe's C-4 closing
   recommendation and the 2012-0118 C-4 record both ranked *inside the top ten* on
   the C-4/C-2 searches. They are close enough to be genuinely dangerous, which is
   what they are for — the corpus is punishing sloppy retrieval as designed.
