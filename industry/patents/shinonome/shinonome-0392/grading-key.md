# Demo Grading Key — Shinonome 0392 Global Patent Filing Corpus

Use this to score a live AI-chat demo objectively. The corpus is the
**40-email signal thread** (`shinonome-0392.md`) with its **17 attachments**,
plus the **155 hard-negative distractors**
(`patent-prosecution-distractors.md`), salted into **6,000 messages** of
generated bulk filler (`patent-prosecution-bulk-filler.md`). Total **6,195**
messages.

A correct answer is judged on three axes:

1. **Recall** — did it surface the specific signal emails and attachments it needed?
2. **Precision** — did it *avoid* the look-alikes? The collision axes here are the
   docket number `MAL-2010-0392` (two Marsden families hold it), `別紙A` /
   `Annex A` (twenty other agreements have one), the six companies whose name
   begins 東雲 / Shinonome, and three other partner confirmations that look like
   the needle and say something different.
3. **Verdict** — is the final natural-language answer correct, especially where
   the firm's own IP management system, and the only ownership document in it,
   both say the opposite?

**The thing this corpus exists to test.** The needle, the precedent and the
document that falsifies the system of record are all in **Japanese**. The
near-miss twin that inverts the verdict is in **Korean**. An English-only
retriever finds the two-line English forward (`Email-11`) and stops there, and a
demo that stops there gets a materially weaker answer than the one the archive
supports. Every query below is written the way a customer would type it — in
English. Score the answer, not the language it was asked in.

Unprefixed IDs (e.g. `Email-10`) refer to `shinonome-0392.md`.
IDs prefixed `D-` refer to `patent-prosecution-distractors.md`.

---

## Signal reference map

| ID | What it is | Lang | Role |
|---|---|---|---|
| Email-1 | Bricknell circulates the executed 2009 JDA, both texts, and warns that the program code "will be read later as if it meant something about ownership" | en | Supporting / the causation seed |
| Email-2 | 発明届出書 for the Vega decoder-clustering invention; no Shinonome material used | ja | The causation seed |
| Email-3 | Kagami's file note: the technology was shown at the April 20 review under Art. 9; Ashiya asks whether it is inside 別紙A | ja | The causation seed |
| Email-4 | Matter opened as `MAL-2010-0392`; PALLAS takes the program code from the disclosure form's "first disclosed at" field; warns that San Mateo already has a `MAL-2010-0392` | en | The causation seed |
| Email-5 | Nyeholt: provisional 61/375,208 filed; **get a sealed letter naming Annex A before the PCT**, because Art. 38 breach is an invalidity ground with no time limit | en | Supporting |
| Email-6 | The formal written request for confirmation, with the Art. 38 reasoning | ja | Supporting |
| Email-7 | Kaida: no substantive disagreement; the 知的財産委員会 will decide in December | ja | Supporting |
| Email-8 | EP renewal instructions on three unrelated families | en | In-file noise |
| Email-9 | Ashiya: the December committee resolved to read 別紙A strictly and not to claim outside it | ja | Supporting |
| **Email-10** | **June 3, 2011, 16:12 — Kaida to Kagami, attaching the sealed 確認書 SDK-IP-2011-0288 and setting out its operative sentence in the body** | **ja** | **THE needle** |
| Email-11 | Kagami's two-line English gist to San Mateo — the entire English-language record of the exchange | en | The trap the tool must overcome |
| Email-12 | Okonkwo-Lind records it as a PALLAS free-text note, cannot change the program code, and notes that nobody in San Mateo can read the letter | en | The causation seed |
| Email-13 | PCT/US2011/048013 filed in sole name, international filing date August 17, 2011 | en | Supporting |
| Email-14 | Munich office move, address for service at the EPO and the DPMA | en | In-file noise |
| Email-15 | National and regional phase entries reported; the docket number changes to `MAL-JP-2010-0392` and pre-2013 papers keep the old one | ja | Cross-year link |
| Email-16 | Supplemental IDS on two unrelated Munich-origin families | en | In-file noise |
| **Email-17** | **October 21, 2013 — Kaida tells Ryowa Electronics that Shinonome has no share and no authority to license, and cites the June 3, 2011 確認書 by date** | **ja** | **Precedent** |
| Email-18 | Kagami's one-line English file note about it | en | Cross-year link |
| Email-19 | SDS asserts co-ownership; ¥4,005,000,000; 無効審判 threatened | ja | Present-day thread start |
| Email-20 | Veritan says `Joint — Shinonome Electric (50%)`; the only ownership document on the matter is the English courtesy translation | en | The trap the tool must overcome |
| Email-21 | What the family is worth, and what a co-owner could do in each jurisdiction | en | Supporting |
| Email-22 | Whitcomb: Art. 74 unavailable on a pre-April-2012 filing; the money claim is at the prescription boundary; **invalidation has no time limit** | en | Supporting |
| Email-23 | Gamō concurs and explains why the demand is dated November 12 | ja | Supporting |
| Email-24 | Q4 annuity batch instructions | en | In-file noise |
| Email-25 | Nothing before 2014 anywhere; the 2016 migration derived `Ownership Status` from the program code and dropped the free-text note | en | The trap the tool must overcome |
| Email-26 | Yokohama file room cleared 2016; Yodogawa merged; everyone has left; the response deadline is extended to February 14 | ja | Supporting |
| Email-27 | Annual UPC opt-out review | en | In-file noise |
| Email-28 | Shinonome Electric's own systems lost it too; Kaida retired in 2017 | ja | Supporting |
| Email-29 | The journal archive was never in scope for any migration, because it is not a docketing system — and do not search in English | en | The product moment |
| Email-30 | 241,700 messages searched in nineteen minutes; the eleven-message Osaka sequence; the sealed 確認書 intact; the Japanese original of the JDA | en | **The product moment** |
| Email-31 | Gamō reads the 確認書 and quotes the operative sentence verbatim | ja | Supporting |
| Email-32 | The Annex A problem was a translation problem — 別紙A vs "arising therefrom", and the Article 8 sentence the English never carried | en | The product moment |
| Email-33 | The precedent recovered on the January 17 addendum pass | ja | **Precedent** |
| Email-34 | Park: keep the Hanyoung confirmation out of the package — it was limited to the JDA term | ko | Supporting / precision warning |
| Email-35 | EP register and German co-ownership under Art. 74 EPC and §§ 741 ff. BGB | de | Supporting |
| Email-36 | PRC Patent Law Art. 14 — China is where an adverse finding costs most | zh | Supporting |
| Email-37 | The response package goes to SDS | ja | Formal rebuttal |
| Email-38 | **SDS withdraws the assertion and the ¥4,005,000,000 demand in full** | ja | **Outcome** |
| Email-39 | 合意書 executed; confirmation, quitclaim, 不起訴の合意, 清算条項; no payment; USD 487,000 of cost | en | Outcome |
| Email-40 | What actually went wrong: a controlled field derived from a program code, and a courtesy translation standing in for a governing text | en | **Causation** |

**Full 2009–2013 trail:** `Email-1` – `Email-7`, `Email-9` – `Email-13`,
`Email-15`, `Email-17`, `Email-18`.

**Full 2024–2025 trail:** `Email-19` – `Email-23`, `Email-25`, `Email-26`,
`Email-28` – `Email-40`.

**In-file noise that is NOT part of either trail:** `Email-8` (EP renewals on
other families), `Email-14` (Munich office move), `Email-16` (IDS on two other
families), `Email-24` (Q4 annuity batch), `Email-27` (UPC opt-out review).

**Deliberate in-world inaccuracy — do NOT grade as a corpus defect:** Email-37
and the response letter it carries describe the 2011 exchange as
「2011年の大阪往復書簡10通」 — **ten** messages. The sequence is **eleven**, and
Email-30 and the journal search report both state it correctly. Real archives
contain human counting errors. An evaluator that notices the discrepancy and
reports it is behaving correctly and should be credited, not penalised.

**Not an error, and the plot:** the English courtesy translation of the 2009 JDA
is wrong in four places, and Annex A is not translated at all. That is the
second of the two things that made the customer's own record say the wrong
thing. Never grade it as a corpus defect.

---

## Query 1 — Primary ("prove the value")

> *"Shinonome Device Solutions are claiming they co-own our decoder-side object
> clustering family and want half the royalties back to 2019. Did anyone at
> Shinonome ever confirm in writing that this invention was outside the joint
> development — and does our own record support them or not?"*

**Correct verdict:** Yes, and in terms. On **June 3, 2011** 海田 隆志 (Takashi
Kaida), General Manager of the intellectual property department of 東雲電機株式会社
(Shinonome Electric Co., Ltd.), wrote **in Japanese** to Ryoko Kagami of Marsden
Japan attaching a sealed 確認書, document number SDK-IP-2011-0288, four pages,
which states that the invention 「2009年11月16日付共同開発契約 別紙A に定める対象範囲
に含まれず、貴社の単独所有である」 — that it does not fall within the scope defined
in Annex A to the joint development agreement of November 16, 2009 and is
Marsden's sole property — that Shinonome asserts **no share whatsoever** in the
invention or in the right to obtain patents on it in Japan or abroad, that it
**will not license third parties**, and that the confirmation 「期間の定めなく効力を
有する」, has effect without limitation of period and is unaffected by the
expiry or termination of the joint development agreement. Marsden asked for it
deliberately, before filing the PCT in its sole name, because Article 38 of the
Japanese Patent Act makes joint filing mandatory where the right to obtain the
patent is co-owned and a breach is an invalidity ground under Article 123(1)(ii)
with no time limit.

**And no, Marsden's own record does not support them — it contradicts the
truth, twice.** Veritan shows `Ownership Status: Joint — Shinonome Electric Co.,
Ltd. (50%)`, a value **derived at the February 19, 2016 migration from the
matter's `JD-SHN-09` program code**, which is a cost-allocation classification;
the free-text `OWNERSHIP BASIS` note that recorded the 2011 confirmation had no
target field and was dropped. And the only ownership document on the matter is
an **English courtesy translation** of the 2009 agreement whose Article 5.1
reads "all improvements arising therefrom shall be jointly owned", having lost
the Japanese text's limitation to 「別紙Aに定める対象範囲」; Annex A itself was never
translated, and Annex A excludes decoder-side and playback-adaptive processing
by name.

A complete answer also gives the precedent: on **October 21, 2013** Kaida told a
third party, 菱和電子株式会社 (Ryowa Electronics), that Shinonome had no share in
the technology and no authority to license it, cited the 2011 確認書 by date
without being asked whether such a letter existed, and sent them to Marsden —
turning away a licence fee he could have taken. The assertion was withdrawn in
full on **March 6, 2025** and settled on **April 18, 2025** with no payment in
either direction.

**MUST cite (recall):**

- `Email-10` — the needle, with its attachment `Shinonome_Kakuninsho_2011-06-03_JA.pdf` (**non-negotiable**)
- `Email-17` — the precedent (**non-negotiable for full recall**)
- `Email-5` — why the letter was asked for
- `Email-6` — the request that produced it
- `Email-20` — the system of record says the opposite
- `Email-25` — where that value came from
- `Email-30` — the archive search that produced the 2011 sequence
- `Email-32` — the translation
- `Email-33` — the precedent recovered
- `Email-38` — the withdrawal
- The present-day trail: `Email-19` – `Email-23`
- Bonus (full credit): `Email-11` and `Email-12` (the thin English record and the
  note that nobody in San Mateo could read the letter), `Email-1`, `Email-9`,
  `Email-31`, `Email-37`, `Email-39`

**MUST NOT cite (precision fails):**

- The other `MAL-2010-0392` — San Mateo's adaptive microphone-array beamforming
  family, the closest look-alike in the corpus: `D-4`, `D-11`, `D-20`, `D-28`,
  `D-31`, `D-40`, `D-48`, `D-60`, `D-62`, `D-64`, `D-66`, `D-72`, `D-93`,
  `D-117`, `D-126`, `D-143`
- The near-miss twin — Hanyoung Precision's confirmation of May 18, 2011, which
  looks identical and was limited to the term of the agreement: `D-2`, `D-3`,
  `D-7`, `D-8`, `D-9`, `D-15`, `D-16`, `D-17`, `D-52`, `D-55`, `D-58`, `D-105`,
  `D-106`, `D-110`, `D-111`, `D-114`, `D-116`, `D-119`
- The qualified twin — Kaida's own confirmation on `MAL-2009-0271`, limited
  「日本国内において」 to Japan: `D-10`, `D-12`, `D-50`, `D-75`, `D-76`, `D-78`,
  `D-80`, `D-82`, `D-85`, `D-88`, `D-103`
- Right person, wrong matter — Kaida **refusing** a confirmation on
  `MAL-2012-0114` because that invention really was inside Annex A: `D-27`,
  `D-30`
- The inverted premise — `MAL-2011-0455`, genuinely co-owned with Shinonome
  Electric and properly filed jointly: `D-14`, `D-21`, `D-26`, `D-42`, `D-53`,
  `D-57`, `D-69`, `D-71`, `D-90`, `D-102`, `D-113`, `D-128`, `D-144`
- The anti-precedent — Chenwei Microsystems, where the same archive search found
  nothing and Marsden conceded: `D-24`, `D-25`, `D-35`, `D-38`, `D-41`, `D-44`,
  `D-49`, `D-70`, `D-74`, `D-94`, `D-100`, `D-137`, `D-138`, `D-139`, `D-140`,
  `D-141`, `D-145`
- Name collisions across the six companies called Shinonome: `D-29`, `D-61`,
  `D-63`, `D-79`, `D-96`, `D-121`, `D-122`, `D-130`, `D-134`, `D-135`, `D-136`,
  `D-142`, `D-146`
- The adjacent-date collision — 東雲精密工業's unrelated and **correct** assertion
  of November 19, 2024 on `MAL-2013-0771`: `D-39`, `D-150`, `D-151`, `D-152`,
  `D-153`, `D-155`
- In-file noise framed as part of the matter: `Email-8`, `Email-14`, `Email-16`,
  `Email-24`, `Email-27`

**Scoring:** cites `Email-10` **and** reaches the conclusion that Shinonome
confirmed sole ownership in writing without limitation of period, **and** says
that Marsden's own system of record is wrong = pass. Misses `Email-10`, or
answers that no confirmation was ever given, or answers that the co-ownership
claim is good because Veritan says Joint = fail. Any trap citation = precision
deduction. Relying on `Email-11` alone, without reaching `Email-10` or its
attachment, scores **partial** on recall and **partial** on verdict — the
English forward does not carry the no-licensing undertaking, the no-expiry
wording, or the reference to Annex A.

---

## Query 2 — The system-of-record gap

> *"Our IP management system has MAL-JP-2010-0392 down as fifty per cent
> co-owned with Shinonome Electric, and the joint development agreement on the
> matter says all improvements from the program are jointly owned. So we do
> co-own it, don't we?"*

**Correct verdict:** No. Both of those are wrong, for two different reasons, and
they are the only two ownership sources in the system. The `Ownership Status`
field is a controlled field that Veritan will not let be empty; PALLAS held no
ownership data, so the February 19, 2016 migration **derived** the value from
the matter's program code under rule 4.3 of the scope note — every matter
carrying a `JD-` code became `Joint` at 50%, all sixty-one of them, and nobody
has reviewed any of them since. The program code was itself set in May 2010 from
a "first disclosed at" box on an invention disclosure form. Article 8 of the
agreement says in terms that the cost-allocation classification is not a
statement of ownership — but the English translation omitted that sentence. And
the agreement on the matter is not the agreement: Article 18 makes the **Japanese
text** the governing text, its Article 5.1 covers only 「別紙Aに定める対象範囲に
おいて生じた発明」, and Annex A — untranslated, and not in Veritan at all — limits
the field to four encoder-side work packages and excludes decoder and
playback-adaptive processing by name.

**MUST cite:** `Email-20` (primary), `Email-25`, `Email-32`, `Email-1`,
`Email-4`, `Email-12`, `Email-10`.
**Bonus:** `Email-29`, `Email-30`, `Email-40`.

**MUST NOT cite:**

- `D-70`, `D-71`, `D-73`, `D-83`, `D-89`, `D-94`, `D-95`, `D-104`, `D-131` —
  other things the same migration derived wrongly, none of them ownership on
  this matter, and `D-70` in particular records that nobody reviewed the
  ownership values
- `D-14`, `D-21`, `D-57`, `D-69`, `D-71`, `D-90`, `D-102`, `D-113`, `D-128`,
  `D-144` — `MAL-2011-0455`, where `Joint` in Veritan is **correct**
- `D-24`, `D-25`, `D-100`, `D-137`, `D-138`, `D-139`, `D-145` — Chenwei, where
  the derived `Joint` value turned out to be right and Marsden paid
- Concluding "yes, you co-own it", or concluding "the migration is unreliable so
  nothing in Veritan can be trusted" — the correct answer is specific to this
  matter and rests on the 2011 confirmation, not on distrust of the system

**Scoring:** contradicts the false premise **and** explains both the derived
field and the translation = pass. Contradicts it on the confirmation alone,
without the mechanism = partial. Confirms the premise = fail.

---

## Query 3 — The disambiguation trap

> *"Show me every email on MAL-2010-0392."*

The corpus contains **two Marsden patent families docketed `MAL-2010-0392`** by
design. Until the January 2013 harmonization, San Mateo, Yokohama and Munich
each ran an independent `MAL-YYYY-NNNN` series restarting at 0001 every January.
The Yokohama one is the decoder-side object clustering family at issue here and
was re-prefixed to `MAL-JP-2010-0392` in 2013; **all of its pre-2013
correspondence, including the needle, uses the bare number**. The San Mateo one
is an unrelated adaptive microphone-array beamforming family and keeps the bare
number to this day. A divisional of the San Mateo case is docketed
`MAL-2010-0392D`. The corpus contains an in-world warning about this collision
(`Email-4`) and two in-world instances of somebody getting it wrong (`D-28`,
`D-126`).

**Correct behaviour:** either scope to the Yokohama family from conversation
context, or state explicitly that two families share the number and separate
them — **not** silently merge them, and not silently return only one of them.
The disambiguators available are the series name, the WO publication number, and
the title.

**MUST cite — the Yokohama family, and only the Yokohama family:** `Email-4` –
`Email-7`, `Email-9` – `Email-13`, `Email-15`, `Email-19`, `Email-30`,
`Email-38`, plus the messages that use the post-2013 form of the number,
`Email-20` – `Email-22`, `Email-25`, `Email-39`, `Email-40`.

**MUST NOT cite — the San Mateo family and its divisional, unless expressly
identified as a different family:** `D-4`, `D-11`, `D-20`, `D-28`, `D-31`,
`D-40`, `D-48`, `D-60`, `D-62`, `D-64`, `D-66`, `D-72`, `D-93`, `D-117`,
`D-126`, `D-143`.

**MUST NOT cite — transpositions and number near-misses, which are not this
number at all:** `D-18`, `D-56`, `D-112` (`MAL-2010-0329`); `D-23`, `D-46`,
`D-91` (`MAL-2010-0932`); `D-36`, `D-77` (`MAL-2011-0392`); `D-34`, `D-43`
(`WO 2012/024513`); `D-51`, `D-120` (`WO 2012/025431`); `D-86`
(`WO 2011/024531`); `D-97` (`特許第5617042号`); `D-107` (`特許第5167402号`).

**Scoring:** discloses that two families share the number = pass on precision.
Returns a merged set with no disclosure = fail. Returns only the San Mateo
family = fail on all three axes.

---

## Query 4 — Causation / responsibility

> *"Nobody lost a document here — the letter was in the archive the whole time.
> So why did this nearly cost us twenty-six million dollars, and what would have
> prevented it?"*

**Correct verdict:** Two failures that pointed the same way, which is why
neither was caught by the other. First, a **controlled field was populated by
derivation from a key that was never about ownership**: Veritan required an
`Ownership Status` value, PALLAS had none to give it, so the 2016 migration took
the `JD-SHN-09` program code — set in May 2010 from a "first disclosed at" box
on a disclosure form — and turned a cost-allocation classification into an
ownership assertion that then fed the royalty schedule and fourteen licence
agreements for nine years, while the free-text note recording the real answer
had no target field and was dropped. Second, **the governing text of the
agreement is Japanese and everyone at headquarters read an English courtesy
translation** that dropped the Annex A limitation from Article 5.1, dropped the
sentence in Article 8 saying the program code is not an ownership statement,
dropped the sentence in Article 5.2 saying that disclosure at a review meeting
does not affect sole ownership, and did not translate Annex A at all.

Nothing was lost and nobody was negligent in 2010 or 2011: Nyeholt asked for
exactly the right document and said why, Kagami spent eight months getting it,
Kaida wrote it in terms that were dispositive in 2011 and in 2025,
Okonkwo-Lind recorded it and flagged both future failure modes in the same
message, and Bricknell had warned in November 2009 that the program code would
one day be read as if it meant something about ownership.

What would have prevented it: not deriving a controlled field from another
field; keeping the governing-language text on the matter rather than only a
translation; and searching the mail journal archive at the point the matter
became disputed rather than after the document systems had been exhausted — the
search took nineteen minutes and it worked because it searched in Japanese.
Marsden spent from November 12 to January 6 searching the one system that could
not contain the answer.

**MUST cite:** `Email-40` (primary — it is the only message that states both
halves), `Email-4`, `Email-12`, `Email-25`, `Email-32`, `Email-1`.
**Bonus:** `Email-29`, `Email-30`, `Email-5`.

**MUST NOT cite:**

- `D-119` and `D-145` — the lessons-learned notes from the Hanyoung and Chenwei
  matters, which draw *different* lessons from *different* facts
- `D-73`, `D-83`, `D-89`, `D-95`, `D-104`, `D-131` — other fields the same
  migration derived wrongly, none of which caused this
- `D-70`, `D-74`, `D-94`, `D-138` — Chenwei, where the cause was that nobody ever
  asked for a confirmation letter, which is the opposite of what happened here
- Attributing the failure to a lost document, to records destruction, to the
  PALLAS decommissioning, to the tape cull, or to any individual's negligence.
  Every one of those is in the corpus and none of them is the cause. The
  documents were never lost; they were in the archive throughout.

**Scoring:** states **both** halves — the derived controlled field and the
governing-text translation — = pass on verdict. States one = partial. Attributes
it to a lost document or to individual negligence = fail.

---

## Quick scoring rubric (per query)

| Axis | Full (2) | Partial (1) | Fail (0) |
|---|---|---|---|
| **Recall** | All required IDs plus the key attachment | Misses a supporting email but has the core needle; or reaches `Email-11` but not `Email-10` | Misses the core needle for that query |
| **Precision** | Zero trap citations | One minor look-alike, or a trap cited and correctly distinguished | Cites the other `MAL-2010-0392`, the Hanyoung or `MAL-2009-0271` confirmation as a parallel, `MAL-2011-0455` as evidence that co-ownership was normal, or the Chenwei outcome as this outcome |
| **Verdict** | Correct, and explains why the system of record disagrees | Correct but shallow — the conclusion without the mechanism | Wrong (e.g. "no written confirmation exists", "the family is co-owned", "the document was lost in the migration") |

4 queries × 3 axes × 2 points = **24 points**.

**Demo passes** when Query 1 scores full on recall, precision and verdict.

---

## Notes for whoever runs the evaluation

- **`grading-key.md`, `DESIGN-BRIEF.md`, `BUILD-NOTES.md` and
  `CAST_AND_TRAP_SHEET.md` must never be ingested into the corpus.** The indexer
  must take only `shinonome-0392.md` from the signal folder. A `*.md` glob puts
  the answer key in the searchable archive and every subsequent evaluation is
  worthless. This has been a real failure mode on a previous build.
- **Ask Query 1 in English.** That is the whole point. If the tool is asked in
  Japanese it will find `Email-10` at rank 5 on lexical matching alone and the
  demo proves nothing about cross-language retrieval.
- **Test the primary query both with and without the docket number.** The live
  `email_search` build hard-restricts results to messages containing a document
  identifier verbatim when one appears in the query, silently and in both
  directions: it drops trail emails that never name the number, and it does not
  disambiguate by family, so the San Mateo `MAL-2010-0392` messages survive with
  equal weight. On this corpus `MAL-2010-0392` appears verbatim in 13 signal
  messages, 14 distractors and **zero** filler messages.
- **The hostile follow-up to rehearse** is "we had a confirmation like this from
  another partner and it expired — why is this one different?" The answer is the
  final sentence of each letter: Hanyoung's says 「본 확인은 공동개발계약의 유효기간
  동안에 한한다」 and lapsed on April 1, 2014; Shinonome's says 「本確認は期間の定めなく
  効力を有する」 and expressly survives the agreement. `Email-34` makes the
  distinction and is in Korean.
