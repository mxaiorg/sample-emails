# Demo Grading Key — Harbor Point Marina Insurance Corpus

Use this to score a live AI-chat demo objectively. The corpus is the **40-email
signal thread** (`harborpoint-marina.md`) plus the **155 hard-negative distractors**
(`insurance-distractors.md`), optionally salted into bulk filler.

A correct answer is judged on three axes:

1. **Recall** — did it surface the specific signal emails / attachments it needed?
2. **Precision** — did it *avoid* the look-alike traps (wrong entity, wrong policy, wrong claim)?
3. **Verdict** — is the final natural-language answer correct, especially where the live policy system would mislead?

Email IDs below (e.g. `Email-6`) refer to the signal file `harborpoint-marina.md`.

---

## Signal reference map

| ID | What it is | Role |
|---|---|---|
| Email-6 | Karen Whitfield's **2011 confirmation of Endorsement #3** — dock & boathouse, $340,000 RC, eff. June 15 2011 (attaches `Endorsement_3_Dock_Boathouse.pdf`) | **THE needle** |
| Email-5 | Broker forwards the 2011 replacement-cost appraisal ($340K) requesting the endorsement | Supporting |
| Email-10 → Email-14 | **2011 claim CLM-2011-3320** — dock storm damage paid $15,900 net under Endorsement #3 (Email-13 = confirmation letter) | Precedent |
| Email-15 | 2024 FNOL — nor'easter total loss, opens the claim | 2024 thread start |
| Email-16 | Rachel Kim opens **claim CLM-2024-10592** | 2024 claim |
| Email-17 / Email-18 | Live system shows **no dock coverage** (dropped in 2016 migration) | The trap the tool must overcome |
| Email-20 | David Alcott reaches back across 13 years, cites the 2011 endorsement + prior claim (references Email-6 & Email-13) | Cross-year link |
| Email-23 | Meridian **confirms 2024 coverage** under Endorsement #3 | 2024 verdict |
| Email-30 | **Coverage Determination Letter 2024** (attaches `Coverage_Determination_Letter_2024.pdf`) | Formal outcome |
| Email-38 | Claim closed, paid to the $340K limit | Closure |

**Full trail of claim CLM-2024-10592:** Email-15 through Email-33, plus Email-35, Email-36, Email-38, Email-39. (The contractor sub-thread Email-24/25/33/35 is part of this claim.)

**In-file noise that is NOT part of the claim:** Email-8 (2011 billing), Email-9 (internal memo), Email-34 (**auto-glass claim CLM-2024-8841**), Email-37 (umbrella quote), Email-40 (renewal notice).

---

## Query 1 — Primary ("prove the value")

> *"Is the dock and boathouse at Harbor Point Marina actually covered under policy MPP-2011-44873? Show me the coverage confirmation and every email tied to the claim."*

**Correct verdict:** **Yes — covered.** The dock and boathouse are scheduled under **Endorsement #3** at **$340,000 replacement cost** (bound 2011, eff. June 15 2011), even though the *current* policy system doesn't show it because the endorsement was lost in the 2016 migration. Coverage was re-verified and the 2024 loss was paid to the limit.

**MUST cite (recall):**

- `Email-6` — the 2011 coverage confirmation + `Endorsement_3_Dock_Boathouse.pdf` (non-negotiable)
- `Email-23` and/or `Email-30` — 2024 coverage confirmed / determination letter
- The claim trail: `Email-15`–`Email-33`, `Email-35`, `Email-36`, `Email-38`, `Email-39`
- **Bonus (full credit):** `Email-13` + the 2011 precedent claim CLM-2011-3320

**MUST NOT cite (precision fails):**

- Any **Harbor Point Yacht Club** or **Harbor Point Condominium Association** email (distractor corpus) — same name, wrong entity
- Any **other** "Endorsement #3" confirmation (there are 13 on other policies) or any other marina's coverage letter
- Any other policy number (only `MPP-2011-44873` is correct)
- **Auto-glass claim CLM-2024-8841** (Email-34), umbrella quote (Email-37), or renewal (Email-40) framed as part of *this* claim

**Scoring:** Cites Email-6 **and** reaches the "yes, covered" verdict = pass. Misses Email-6, or says "not covered / not in system" = fail. Any trap citation = precision deduction.

---

## Query 2 — The migration-gap tell

> *"Our policy system doesn't show any dock coverage on MPP-2011-44873 — was it ever added?"*

**Correct verdict:** Yes. **Endorsement #3** was bound in 2011 (`Email-6`) with a $340K replacement-cost appraisal (`Email-5`); it never lapsed and was already honored once (2011 claim). It's missing from the live system only because of the 2016 platform migration (`Email-18`, `Email-20`).

**MUST cite:** `Email-6` (primary), `Email-5`, `Email-20`. **Bonus:** `Email-18`.
**MUST NOT:** cite any other Endorsement #3 / other policy; conclude "no coverage."

---

## Query 3 — Prior-claim history

> *"Has there ever been a prior claim on the Harbor Point dock structures?"*

**Correct verdict:** Yes — one prior claim, **CLM-2011-3320** (Dec 2011), a winter-storm dock loss paid **$15,900 net** under Endorsement #3.

**MUST cite:** `Email-10`–`Email-14` (esp. `Email-13`).
**MUST NOT:** present the **2024** claim as the "prior" claim; cite any other marina's storm claim from the distractor set; cite the auto-glass claim.

---

## Query 4 — Claims-file completeness

> *"Assemble the complete email trail for claim CLM-2024-10592."*

**Correct set (recall):** `Email-15`–`Email-33`, `Email-35`, `Email-36`, `Email-38`, `Email-39`.

**MUST NOT include (precision):** `Email-34` (auto-glass CLM-2024-8841), `Email-37` (umbrella), `Email-40` (renewal), `Email-8`, `Email-9`, or **any distractor-corpus claim**. This query specifically tests whether the tool distinguishes *this* claim from same-policyholder noise and same-vocabulary decoys.

---

## Quick scoring rubric (per query)

| Axis | Full (2) | Partial (1) | Fail (0) |
|---|---|---|---|
| **Recall** | All required IDs + key attachment | Misses a supporting email but has the core needle | Misses `Email-6` / the core needle |
| **Precision** | Zero trap citations | 1 minor look-alike | Cites a Harbor Point collision, wrong policy, or wrong claim |
| **Verdict** | Correct + explains the migration gap | Correct but shallow | Wrong (e.g., "not covered") |

**Demo passes** when Query 1 scores full on all three axes — i.e. it finds the one 2011 email out of thousands, ignores ~150 look-alikes, and returns the answer the live policy system alone would get wrong.
