# Build notes — `shinonome-0392`

Sixth corpus in the series, after `harborpoint-marina` (insurance),
`riverwalk-garage` (engineering/AEC), `northfield-grain` (commercial lending),
`corbin-tower-632588` (interiors/architecture) and `marchwood-0447` (US
securities regulation).

**Vertical: global corporate patent filing and prosecution**, seen from inside a
US technology licensor's in-house IP department with regional staff in Japan,
Germany, Korea and China. Built to showcase **cross-language retrieval** in
mxMCP: the archive whose value the demo proves is the company's own mail journal
archive, the system that gets the answer wrong is its IP management system, and
**the answer is in Japanese.**

The customer this pattern is aimed at is a technology licensor that runs a
global patent-filing operation through mxHERO rules — per-country routing to
different groups of outside counsel, program-coded joint-development traffic,
annuity and deadline mail. No real customer is named or implied anywhere in the
corpus. The registrants, staff, firms, docket numbers, patents and the dispute
are all invented. The legal framework is real and was verified against primary
sources during the build (§7).

---

## 1. Why this vertical needs a different needle

Every previous corpus turned on a document that a public register could not
settle. That constraint is sharper in patents than anywhere else, because
**almost everything about a patent is public**. Filing dates, grants, lapses,
proprietors on the register, oppositions — a competent adversary looks all of it
up in twenty minutes, and a demo built on any of it collapses.

So the dispute here is about the one thing that is *never* public: **whether an
invention fell inside the defined field of a joint development agreement**, and
therefore whether the right to obtain the patent was co-owned. That question is
answered only by what the two companies said to each other at the time.

It also has real teeth. Japan Patent Act **Article 38** requires an application
to be filed by all co-owners jointly; breach is a ground of refusal under Art.
49 and a ground of invalidity under **Art. 123(1)(ii)**, and there is **no time
limit on requesting an invalidation trial** (Art. 123(3); no Patent Act analogue
to the five-year bar in Trademark Act Art. 47). The exposure never ages out.
That is what makes a fourteen-year-old letter the only thing that ends the
matter, and it is the whole reason the archive is worth what it is worth.

---

## 2. Phase 0 — the design, as six sentences

1. **The needle.** June 3, 2011 — 海田 隆志 (Takashi Kaida), 知的財産部長 of
   東雲電機株式会社 (Shinonome Electric Co., Ltd.), Osaka, writes **in Japanese** to
   加賀美 涼子 of マースデン・ジャパン株式会社, attaching a sealed 確認書 (SDK-IP-2011-0288)
   confirming that the invention 「2009年11月16日付共同開発契約 別紙A に定める対象範囲に
   含まれず、貴社の単独所有である」, that Shinonome claims **no share** in the right to
   obtain patents on it anywhere, that it **will not license third parties**, and
   that the confirmation 「期間の定めなく効力を有する」 and survives the agreement.
   Marsden asked for it deliberately, before filing the PCT in its sole name,
   because of Art. 38.
2. **Both systems lose it.** The **February 19, 2016 PALLAS → Veritan IPM
   migration** carried correspondence only from January 1, 2014, and — because
   Veritan's `Ownership Status` is a controlled field that cannot be empty and
   PALLAS held no ownership data — **derived** the value from the matter's
   program code. `MAL-2010-0392` carried `JD-SHN-09` because a docket clerk in
   May 2010 took it off the "first disclosed at" box on an invention disclosure
   form. All 61 `JD-` matters migrated as `Joint`. The free-text `OWNERSHIP
   BASIS` note recording the 2011 confirmation had no target field and was
   dropped. On the other side, Shinonome Electric changed platform in 2018 on a
   seven-year retention, and the April 2022 carve-out to Shinonome Device
   Solutions transferred contracts, not correspondence.
3. **Everyone has left.** Kaida retired March 2017; Kagami left in 2016; Nyeholt
   2015; Okonkwo-Lind 2015; Bricknell 2019; Ashiya 2019. 淀川国際特許事務所 merged
   in 2018 and destroyed its pre-2015 paper in 2022; 中臣 retired in 2019.
4. **The claim.** November 12, 2024 — Shinonome Device Solutions asserts
   co-ownership, demands a half share across the family and **¥4,005,000,000**
   (≈ **USD 26,700,000** at ¥150), and threatens 無効審判 on Art. 123(1)(ii). The
   forward licensing position at risk is **USD 58,700,000** to expiry on
   August 17, 2031.
5. **The archive produces it — plus the precedent.** January 14, 2025 — the mail
   journal archive, journaling the corporate tenant since 2008 and never
   migrated because it is not a system of record, returns **241,700** messages
   for 2009–2014 and, in nineteen minutes, the **eleven-message Osaka sequence**,
   the sealed 確認書 intact, and the **Japanese original** of the 2009 agreement
   including 別紙A. A second pass on January 17 with the direction filter off
   returns the precedent: **October 21, 2013**, Kaida telling 菱和電子株式会社 that
   Shinonome has no share and no authority to license, citing the 2011 確認書 by
   date without being asked whether it existed, and giving up a licence fee.
6. **The claim collapses.** March 6, 2025 — withdrawn in full. April 18, 2025 —
   a 合意書 with a 権利帰属確認条項, a quitclaim held in escrow (registration of a
   transfer is constitutive in Japan under Art. 98(1)(i)), a 不起訴の合意 covering
   無効審判 on entitlement grounds, and a 清算条項. No payment in either direction.
   Marsden's total cost: **USD 487,000**.

**Why the demand is dated November 12, 2024.** The Japanese patent was
registered on December 12, 2014. Pleaded as a single claim accruing at
registration it falls under the pre-2020 Civil Code and the old ten-year
objective prescription (改正民法附則10条4項, 旧民法167条1項). SDS filed four weeks
before the boundary. Whitcomb's memorandum points out that if they repleaded it
as an accounting for receipts in 2019–2024 the prescription point would
disappear — which is exactly why they did not.

---

## 3. What is new in this build: the multilingual layer

This is the first corpus in the series where **the language of a message is part
of the trap.**

| File | ja | ko | zh | de | en |
|---|---|---|---|---|---|
| Signal (40) | 16 | 1 | 1 | 1 | 21 |
| Distractors (155) | ~45 | ~14 | ~26 | ~14 | ~56 |
| Filler (6,000) | 1,305 | 474 | 630 | 751 | 2,840 |

A non-English message is written **wholly** in that language — subject line,
body and signature block. There is no English gloss anywhere. That is what makes
the retrieval test real: an English-only index cannot see the message at all.

Three design decisions make the language load-bearing rather than decorative:

1. **The needle is in Japanese and its English shadow is deliberately thin.**
   `Email-11` is Kagami's two-line forward to San Mateo: *"Shinonome have
   confirmed in writing that the invention is outside the Annex A field and is
   ours alone."* It does not carry the no-licensing undertaking, the no-expiry
   wording, or the fact that the letter names Annex A. `Email-12` says, in 2011,
   that the letter is in Japanese with no translation and that anyone in San
   Mateo who needs to know what it says will have to have Yokohama read it to
   them. A tool that finds `Email-11` and stops gets a weaker answer that is not
   obviously weaker — which is the failure mode worth demonstrating.
2. **The document that misled the customer is a translation.** The only
   ownership document in the IP management system is the English courtesy
   translation of the 2009 agreement. It renders 「別紙Aに定める対象範囲において
   生じた発明」 as "all improvements arising therefrom", drops the sentence in
   Article 8 saying the program code is not an ownership statement, drops the
   sentence in Article 5.2 saying that disclosure at a review meeting does not
   affect sole ownership, and does not translate Annex A at all. Article 18
   makes the Japanese text governing. **The system field and the system's own
   document are wrong for two independent reasons and both point the same way**,
   which is why neither was ever caught by the other.
3. **The trap that inverts the verdict is in Korean.** Hanyoung Precision's
   confirmation of May 18, 2011 is near-identical to the needle — same form of
   agreement, same signatory level, sixteen days apart — except for its last
   sentence, 「본 확인은 공동개발계약의 유효기간 동안에 한한다」, limiting it to the term
   of the agreement, which expired April 1, 2014. Marsden relied on it in 2019,
   lost, conceded co-ownership and paid **KRW 940,000,000**. A tool that reads
   Japanese but not Korean, or that reasons from shape rather than from text,
   cites it as a parallel and loses the argument. `Email-34` is the in-corpus
   warning and it too is in Korean.

**Practical note for the build pipeline.** `tools/md_to_pdf.sh` needs a
CJK-capable font before the attachments will render. With pandoc and xelatex,
add `-V CJKmainfont="Noto Serif CJK JP" -V mainfont="Noto Serif"` (or the
equivalent for the fonts installed) — the default Latin font silently drops
every CJK glyph and produces blank pages for eight of the seventeen attachments.

---

## 4. Files

```
stories/
├── shinonome-0392/
│   ├── shinonome-0392.md                 40 emails, 18 attachment refs   <- INGEST ONLY THIS
│   ├── grading-key.md                    4 queries, 24 points            <- NEVER INGEST
│   ├── BUILD-NOTES.md                    this file                       <- NEVER INGEST
│   ├── DESIGN-BRIEF.md                   the authoring brief             <- NEVER INGEST
│   └── attachments/                      17 markdown documents (ja / en / mixed)
├── patent-prosecution-distractors/
│   ├── patent-prosecution-distractors.md 155 hard negatives
│   ├── CAST_AND_TRAP_SHEET.md            the authoring brief             <- NEVER INGEST
│   └── part-A..D.md                      the four authored batches, merged and superseded  <- NEVER INGEST
└── patent-prosecution-bulk-filler/
    ├── patent-prosecution-bulk-filler.md 6,000 generated messages
    ├── generate.py                       seeded, self-contained
    └── _config_block.py                  the CONFIG block alone, for the next port
tools/
├── validate_story.py                     unchanged
├── audit_corpus.py                       ERA_TERMS extended; nth_weekday bug fixed
├── rank_check.py                         CJK tokenizer and length normalization added
└── check_grading_key.py                  unchanged
```

**Corpus total: 6,195 messages.**

The indexer must take **only** `shinonome-0392.md` from the signal folder. A
`*.md` glob puts the answer key in the searchable archive.

---

## 5. Reproducing the filler

```
python3 stories/patent-prosecution-bulk-filler/generate.py \
    --count 6000 --seed 390211 \
    --out stories/patent-prosecution-bulk-filler/patent-prosecution-bulk-filler.md
```

Seed **390211**, count **6000**, sha256 prefix **07011fd67731575a**. Verified
byte-for-byte reproducible across three runs.

The vertical lives entirely in the CONFIG block. **Five machinery changes** were
made below the line and are commented in place:

1. `PROJECTS` → `MATTERS`. The unit of work is a docketed patent family, and its
   application, publication and patent numbers are **derived arithmetically from
   the docket, once** (`derive_numbers()`), so the same matter carries the same
   numbers in every message in every language. Filler docket numbers all use a
   4-digit block ≥ 3000, so no filler docket can collide with — or contain as a
   substring — any signal or distractor docket.
2. **Language.** Every template declares the language it is written in. The
   correspondent must have that language, and the Marsden author must be at the
   site that speaks it (everyone writes English; only Yokohama writes Japanese,
   only Munich German, only Seoul Korean, only Shanghai Chinese). Opener, closer
   and reply pools are keyed by `(language, register)`.
3. **Role gating.** `TEMPLATE_ROLES` names the roles that may send each template.
   Without it the generator casts a facilities coordinator as the author of an
   EPO opposition note.
4. **Counterparty-kind gating.** An annuity provider does not send an office
   action report and a licensee does not receive filing instructions.
5. **In-language date rendering.** A Japanese message writes 2016年3月14日, a
   Korean one 2016년 3월 14일, a German one 14. März 2016. The `Date:` header
   stays in the machine format in every language.

`audit_corpus.py` `ERA_TERMS` gained thirty patent terms: Unitary Patent and UPC
from 2023, CNIPA from 2018 with SIPO closing in 2018, 专利复审委员会 closing and
复审和无效审理部 opening in 2019, MOIP from 2025, the AIA and inter partes review
from 2011–2012, 特許異議申立 from 2015, the London Agreement from 2008, ePCT, WIPO
DAS, Global Dossier, PCT Direct, 知財高裁 from 2005, and the two in-world systems.
`PALLAS` is deliberately open-ended at the top of its window — a 2025 message
legitimately refers back to a system retired in 2018.

**A real bug was fixed in the shipped toolkit.** `nth_weekday(year, month, wd,
-1)` walked forward from day 28 and then stepped back, which returns the wrong
date whenever day 28 already sits past the last occurrence — it computed
Memorial Day 2010 as May 24 instead of May 31. Both `audit_corpus.py` and the
generator carried the bug, so the holiday sets were consistently wrong together
and no previous build would have noticed. Fixed in both.

---

## 6. Gate results

### Gate 1 — structural validation

```
shinonome-0392.md:                       40 emails, 18 attachment references   PASS
patent-prosecution-distractors.md:      155 emails,  0 attachment references   PASS
patent-prosecution-bulk-filler.md:    6,000 emails,  0 attachment references   PASS
grading-key.md (check_grading_key.py)                                          PASS, no warnings
  Query 1: 21 must-cite, 101 must-not-cite
  Query 2:  7 must-cite,  25 must-not-cite
  Query 3: 17 must-cite,  31 must-not-cite
  Query 4:  6 must-cite,  12 must-not-cite
  4 queries x 3 axes x 2 points = 24 points; key references 40/40 signal emails
```

### Gate 2 — adversarial realism audit

`PASS` on all three files together. Notable lines:

```
ok    signal:era-gating          0 anachronistic term uses
ok    signal:holidays            0 emails sent on a US federal holiday
ok    signal:body-diversity      100.0% distinct
ok    distractors:holidays       0 emails sent on a US federal holiday
ok    filler:body-diversity      88.1% distinct (target >=75%)
ok    filler:coverage            6000 emails, 2009-01-07 to 2025-12-31, 17 years
ok    cross:cast-leak            0 addresses appear in both the filler and a signal file
ok    cross:token-leak           0 signal tokens found in the filler
ok    cross:spelling             signal / distractors / filler all american
```

Three advisory `info` lines, all expected: weekday skew 27.5% on the signal and
43.9% on the distractors, both hand-authored narrative below the 200-message
threshold at which the distributional checks bind; 21.2% on the filler, which is
the target.

The filler's subject diversity is 46%, which is low and is a property of a
template generator with 72 templates over 6,000 messages. Body diversity, which
is the check that binds, is 88.1%.

### Gate 3 — content consistency

Two adversarial passes were run, one over the signal plus all seventeen
attachments and one cross-checking the four independently authored distractor
batches against each other and against the signal. Together they returned
**97 findings**. All substantive ones are fixed. The ones worth recording,
because they are the class of defect that falsifies a demo:

| # | Defect | Fix |
|---|---|---|
| 1 | **The translation trap did not work on its own text.** As first drafted, the English translation's Article 1 defined "the Joint Development" *by reference to Annex A* and Article 4 repeated the limitation — so "improvements arising therefrom" still meant "within the Annex A scope", and the English said exactly what the Japanese said. The whole second wrong source evaporated. | Article 1 rewritten to define the Joint Development as R&D "in the field of next-generation object-based audio coding"; Article 4 reduced to a bare work-package pointer. "Therefrom" now has nothing to attach to but the whole field. |
| 2 | Worse: the same English translation contained, **in English**, three separate answers to the claimant's three grounds — that disclosure at a review meeting does not affect sole ownership (Art. 5.2), that the cost-allocation code is not an ownership statement (Art. 8), and an instruction to go and read Annex A in the Japanese. Eight weeks of paralysis was incredible against a document already in the system. | All three deleted from the English. The Japanese original keeps them, which is what makes `Email-32` a discovery instead of a re-reading. |
| 3 | **The Hanyoung JDA's expiry date had bled into the Shinonome one.** `Email-31` — the message in which counsel explains why 「期間の定めなく」 matters — dated the Shinonome agreement's expiry to 2014-03-31, which is Hanyoung's date and which the recovered Japanese original contradicts. | Shinonome's term ends 2013-12-31; Hanyoung's stays 2014-03-31. The two must never share a date. |
| 4 | `Email-25` said all 61 `JD-` matters read `Joint`; `Email-40` then reported five of the same 61 as **wrongly `Sole`**, which the migration rule makes impossible. | `Email-40` now audits two populations — the 61 coded matters and 212 matters with an agreement and no code. |
| 5 | **A distractor programme falsified the signal's central systems fact.** Two 2016 distractors described a formal post-cutover verification of the derived `Ownership Status` values, escalated by name — against `Email-25`'s "nobody has ever looked at whether that is true of any individual one of them", from the same speaker. | Recast as a cost reconciliation that finds a mismatch incidentally and records in terms that no ownership review was ever run. |
| 6 | **The anti-precedent was defused by its own author.** A 2018 distractor had the same attorney read the Chenwei Article 5 correctly and write it up four years before the 2022 message in which he "reads it for the first time". | Reversed: he reads it in 2018 and reaches the *wrong* conclusion, and nobody corrects him. It is now a second incriminating document rather than an alibi. |
| 7 | **The precedent was overclaimed as "unprompted".** Kaida's October 2013 letter opens by acknowledging Ryowa's licence enquiry of October 15, which is quoted in his own first line. Three messages and the response letter described the letter itself as unprompted — answerable from the exhibit in one line. | Narrowed everywhere to the true and stronger point: nobody asked him whether the 2011 confirmation existed, and he cited it by date anyway. |
| 8 | The Hanyoung agreement's Annex A existed in two irreconcilable versions across two batches (five packages `A-1…A-5` versus four packages `H-1…H-4`, different subject matter). | Unified to `H-1…H-4`. |
| 9 | `MAL-2009-0271` was sole-filed in one batch and jointly filed from the outset in another, which made the Japan-limited confirmation meaningless. | Filed by Marsden alone; Shinonome's EP share asserted and conceded in 2015. |
| 10 | The Shinonome agreement's ownership clause was cited as **Article 4.2** in two distractors against Article 5.1 everywhere else, including the signal. | Article 5.1 throughout. |
| 11 | **Pre-AIA applicant formalities.** A PCT filed at RO/US in August 2011 named the corporation as sole applicant for all designated States; a 2010 US provisional named the corporation as applicant. | Inventors named as applicants for the US on the PCT; the provisional relabelled to assignee of record. |
| 12 | **Chain of title was never executed.** The inventors are Marsden Japan employees, so under pre-2015 Art. 35 the right vested in the *inventors* and passed to **Marsden Japan** by 予約承継 — but every filing is in the name of the US parent, and the 確認書 was addressed to Marsden Japan. No assignment appeared anywhere. | 確認書 preamble defines 貴社 as the group; the assignment chain 森末/一色 → Marsden Japan K.K. → Marsden Audio Laboratories, Inc. is recorded in the PCT docket note; Marsden Japan added as a fourth party to the settlement agreement. |
| 13 | The response letter asserted 消滅時効 without dealing with the **催告** effect of the November 12 letter (旧民法153条: six months' provisional interruption), which is the one point opposing counsel answers. | Addressed expressly in the response letter. |
| 14 | The prescription argument was applied to the wrong claim: an accounting for royalties *received* in 2019–2024 accrues on receipt, nowhere near the ten-year boundary. | The demand is repleaded as a single claim accruing at registration, and Whitcomb notes that repleading it the other way would destroy Marsden's own prescription point. |
| 15 | The WO publication number was quoted in an August 2011 email, six months before publication allocated it. | Removed; the docket note now says the number will come with Form PCT/IB/308. |
| 16 | A Japanese divisional was filed three days **after** the parent's 設定登録, which closes the 44条 window. | Order swapped. |
| 17 | The journal-archive volumes across four distractors were mutually impossible (from 480 to 9,700 journaled messages per custodian per year). | Anchored to ~44,000 messages a year company-wide, consistent with the signal's 241,700 for 2009–2014. |
| 18 | 保密审查 cited to PRC Patent Law **Art. 19** in 2014–2016 and co-ownership to **Art. 14** in 2021 — both are the post-2020 numbering, in force 1 June 2021. | Art. 20 and Art. 15 before that date; the 2022 messages correctly use the current numbering. |
| 19 | Nine career-window violations across the merged distractor file (Etxeberria in 2019, Crozier in 2016, Achinstein in 2010, Nandakumar in 2011, and 淀川・浪速国際特許業務法人 seventeen times before the 2018 merger that created it). | All reassigned; a pre-2018 associate at 淀川国際特許事務所 invented for the earlier traffic. |
| 20 | All 56 empty `References:` lines in the merged distractor file carried three trailing spaces, not two — an artifact of the merge script. | Fixed. |

Also corrected: a disclosure form attached to a March 2010 email carrying IP-department entries dated up to 77 days in the future; a January 14 report containing a January 17 addendum that leaked the precedent a week early (split into two documents, the addendum now carried by `Email-33`); tape images destroyed under a seven-year rule five years after creation; "nine months" for an eight-month wait; "thirteen-year-old" and "fourteen-year-old" in the same author's email and memorandum on the same day; a PCT fee table that did not add up; a settlement agreement to which Marsden Japan was not a party; three messages citing the covering email's paragraph numbering while purporting to cite the letter; 特許第5617042号 registered on a date its own number rules out; a Rule 71(3) period computed to a date matching no rule; a Korean-language message using Japanese corner quotes; German `du` and `Sie` between the same pair; and a Chief IP Counsel tasking a colleague with producing the document she had just attached.

Two things were **not** changed and are documented as intentional: the
「2011年の大阪往復書簡10通」 miscount (§8), and the fact that the English courtesy
translation is wrong in four places.

### Gate 4 — retrieval reality check (`rank_check.py`, BM25 over all 6,195)

`rank_check.py` needed two changes before it could measure anything here. A
Latin-only tokenizer sees a Japanese message as the empty document, so CJK and
Hangul runs are now emitted as **character bigrams**; and because one bigram per
character makes a Japanese body look two to three times longer than an English
one, **document length counts a CJK bigram as half a term**. Without the second
change BM25 penalises every Japanese document on every query. The stopword list
also gained the query-shell words (`show`, `every`, `did`, `ever`, `why`, …),
without which a natural-language demo query is ranked mostly on the word
"email".

| Query | Needle | Rank | First filler | Top-20 |
|---|---|---|---|---|
| Q1 in **English** — "did anyone at Shinonome ever put in writing that this invention was outside the joint development?" | `Email-11` (the English shadow) | **5** | 44 | 12 distractor / 8 signal — **PASS** |
| the same query, scored against the real needle | `Email-10` (Japanese) | **527** | 44 | — **FAIL, and this is the finding** |
| Q1 in **Japanese** | `Email-10` | **5** | 39 | 12 signal / 8 distractor — **PASS** |
| Q2 — "our IP system shows it as jointly owned … where did that value come from?" | `Email-25` | **10** | 20 | 11 distractor / 8 signal / 1 filler — **PASS on the needle, one filler at rank 20** |
| Q3 — the bare identifier `MAL-2010-0392` | `Email-10` | **16** | 196 | 14 distractor / 6 signal — **PASS** |
| Q4 — "what went wrong, the derived ownership field or the courtesy translation?" | `Email-40` | **3** | 26 | 13 distractor / 7 signal — **PASS** |

**The 527 is the headline number of this corpus, not a defect.** On the primary
query, asked in English, plain lexical retrieval puts the document that decides
the matter at rank 527 of 6,195 and puts its two-line English summary at rank 5.
That is precisely the gap the demo is for. Everything downstream of the needle —
the no-licensing undertaking, the no-expiry wording, the fact that the letter
names Annex A, and the entire October 2013 precedent — lives only in the
Japanese, and an English-only reader gets a materially weaker answer without any
signal that it is weaker.

Per §13 of the process specification the primary query was tested **both with and
without the docket number**. `MAL-2010-0392` appears verbatim in 13 signal
messages, 14 distractors and **zero** filler messages, so the live tool's
verbatim-identifier filter eliminates the filler entirely and leaves the two
families that share the number competing on equal weight — which is exactly the
point of Query 3.

Query 4's needle is `Email-40`, not the migration emails: `Email-40` is the only
message that states both halves of the causation answer.

### Gate 5 — blind evaluation

Not run. Requires the corpus built to `.eml` and ingested. See §9.

---

## 7. Verified legal facts this corpus depends on

Checked against primary sources during the build. Do not "correct" these.

- **JP Art. 38 / 49(ii) / 123(1)(ii) / 123(3)** — joint filing mandatory; breach is
  a refusal ground and an invalidity ground; **no time limit** on an invalidation
  trial, and one may be requested after the patent lapses.
- **JP Art. 74** (transfer claim) — introduced by 平成23年法律第63号, in force
  1 April 2012, and **附則第2条第9項 limits it to applications filed on or after
  that date**. Under Art. 184-3(1) a PCT application is deemed filed in Japan on
  its **international filing date** — here August 17, 2011 — so the transfer
  claim is closed to the claimant and invalidation is the only real lever. This
  is the single most load-bearing fact in the corpus.
- **JP Art. 73** — (2) each co-owner may work the invention without consent;
  (3) **no co-owner may grant any licence without the consent of all**.
- **JP Art. 33(3) / 34(1) / 34(4) / 98(1)(i)** — share assignment needs consent; a
  pre-filing succession is not effective against third parties unless the
  successor files; a post-filing transfer needs notification; **registration of a
  transfer is constitutive**, not merely a matter of third-party effect.
- **JP Art. 35, pre-2015** — for an invention made in 2010 the right arises in the
  **inventor** and passes to the employer by 予約承継. Original employer vesting
  applies only from 1 April 2016.
- **35 U.S.C. § 262** and *Schering v. Roussel-UCLAF* (Fed. Cir. 1997) — a joint
  owner may make, use and sell without accounting, and may license unilaterally;
  the licensing right is Federal Circuit gloss, not statutory text.
  ***Ethicon v. U.S. Surgical*** (Fed. Cir. 1998) and ***STC.UNM v. Intel***
  (Fed. Cir. 2014) — all co-owners must join as plaintiffs and a co-owner's
  refusal is a substantive right that defeats Rule 19(a) involuntary joinder.
- **PRC Patent Law Art. 14** (2020 amendment, in force 1 June 2021; formerly
  Art. 15) — a co-owner may exploit alone **or grant a non-exclusive licence**,
  with royalties shared. China is the only jurisdiction here where the statute
  itself permits unilateral licensing.
- **KR Art. 99(2)–(4)** — modelled on JP Art. 73; **Art. 44** is the joint-filing
  rule.
- **Art. 74 EPC** sends ownership to national law; Germany applies §§ 741 ff. BGB.
  Self-use is free (BGH *Gummielastische Masse II*); the prevailing view is that
  a licence needs the consent of all co-owners.
- **改正民法附則10条4項** — a claim arising before 1 April 2020 stays under the old
  ten-year objective prescription of 旧民法167条1項; 旧民法153条 gives a 催告 six
  months' provisional interruptive effect.
- **Procedure** — national/regional phase 30 months for JP, CN, US, BR and **31
  for EP, KR, IN**; JP request for examination 3 years from the filing date;
  JP office-action response 3 months for a foreign applicant, 60 days for a
  domestic one; JP patent fees years 1–3 within 30 days of the 特許査定, then
  annually from year 4; **no annuities on pending JP, KR or CN applications**;
  EPO renewal fees from the third year, moving to the national offices after the
  year of grant; EPO opposition 9 months from the mention of grant; Rule 71(3)
  four months non-extendable; London Agreement from 2008; Unitary Patent and UPC
  from 1 June 2023; JP post-grant opposition from 1 April 2015; SIPO → CNIPA in
  2018 and 专利复审委员会 → 复审和无效审理部 on 1 April 2019; KIPO throughout (it
  became MOIP only in October 2025, after this story ends); Korean office-action
  response 2 months in this era. Japanese patent numbers: 特許第5,500,000号 ≈ May
  2014, 特許第5,800,000号 ≈ October 2015, 特許第6,000,000号 not until late
  September 2016 — 特許第5617402号 is correct for a December 2014 registration.

---

## 8. Deliberate in-world inaccuracy

`Email-37` and the response letter it carries describe the 2011 exchange as
「2011年の大阪往復書簡10通」 — **ten** messages. The sequence is **eleven**.
`Email-30` and the journal search report both state it correctly. Documented in
the grading key as intentional. An evaluator that notices the discrepancy and
reports it is behaving correctly and should be credited.

Gate 3 confirmed this is the only miscount in the corpus.

---

## 9. What is left to do

```bash
# 1. attachments -> PDF  (needs a CJK font; see §3)
tools/md_to_pdf.sh stories/shinonome-0392/attachments

# 2. build .eml  (only <slug>.md from the signal folder)
go run . -create -md stories/shinonome-0392/shinonome-0392.md -out stories/shinonome-0392/emls
go run . -create -md stories/patent-prosecution-distractors/patent-prosecution-distractors.md -out stories/patent-prosecution-distractors/emls
go run . -create -md stories/patent-prosecution-bulk-filler/patent-prosecution-bulk-filler.md   -out stories/patent-prosecution-bulk-filler/emls

# 3. send
go run . -send stories/shinonome-0392/emls
go run . -send stories/patent-prosecution-distractors/emls
go run . -send stories/patent-prosecution-bulk-filler/emls
```

Then confirm the indexer took **only** `shinonome-0392.md` from the signal
folder — not `grading-key.md`, not `BUILD-NOTES.md`, not `DESIGN-BRIEF.md` — and
run five blind-evaluator passes, recording each as
`test-results-<date>-run<N>.md`.

**Check one thing before the first run:** that the index and the embedding model
actually handle Japanese, Korean and Chinese. If they do not, Query 1 will
return `Email-11` and nothing else, and the corpus will look like it has a hole
in it when what it has is the finding.

**Demo-ready** = Query 1 scores full on recall, precision and verdict.

---

## 10. Demo script, in five moves

1. **"Show me every email on MAL-2010-0392."** Two Marsden families come back.
   The tool has to say so. This is the query the customer will try first because
   it is the one their own docketing system answers wrongest — and the in-world
   warning about the collision was written in May 2010 by the clerk who created
   it (`Email-4`).
2. **"Our IP system says this family is fifty per cent co-owned with Shinonome,
   and the agreement on the matter agrees. So we co-own it?"** No — and here is
   where the field came from and why the agreement on the matter is not the
   agreement. A controlled field derived from a cost code, and a courtesy
   translation of a Japanese governing text.
3. **"Did anyone at Shinonome ever say otherwise, in writing?"** Yes. June 3,
   2011. **Then show the English record first** — the two-line forward — and then
   the Japanese letter it summarises. The gap between them is the product.
4. **"Did they ever act on it?"** October 21, 2013. Unasked, to a third party,
   with no dispute pending, giving up a licence fee, citing the 2011 letter by
   date. That is the beat that ends the argument.
5. **"We had a letter like this from a Korean partner and it expired. Why is
   this one different?"** The last sentence of each letter. Hanyoung's is limited
   to the term of the agreement and lapsed in 2014; Shinonome's says
   「本確認は期間の定めなく効力を有する」 and expressly survives it. One is in Korean,
   one is in Japanese, and the distinction is the whole case.

The number to say out loud at the end is **¥4,005,000,000 — about
$26,700,000 — withdrawn in full**, and the sentence to say with it is Marisol
Etxeberria's in `Email-40`: the search that found it took nineteen minutes, and
it worked because it searched in Japanese.
