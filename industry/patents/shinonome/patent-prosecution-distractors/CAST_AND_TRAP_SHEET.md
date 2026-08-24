# Cast and trap sheet — `patent-prosecution-distractors` — NEVER INGEST

The authoring brief for the 155 hard negatives that sit alongside the
`shinonome-0392` signal file. Read all of it before writing a single message.

A distractor's only job is **to be wrong in a way that is expensive to detect.**
Every message here must be plausible enough that a careful reader has to do work
to rule it out, and wrong enough that citing it loses the argument.

---

## 0. What the signal says (do not contradict, do not corroborate)

Marsden Audio Laboratories, Inc. (San Mateo) owns patent family
**MAL-JP-2010-0392** (legacy `MAL-2010-0392`, **Yokohama series**), covering
decoder-side object clustering. In 2024 Shinonome Device Solutions K.K. asserted
co-ownership; the assertion collapsed in March 2025 on a June 3, 2011 Japanese
confirmation letter from 海田 隆志 of 東雲電機株式会社 and an October 21, 2013
letter in which he turned away a third party's licence request.

**These strings must NEVER appear anywhere in the distractor file:**

`MAL-JP-2010-0392` · `WO 2012/024531` · `PCT/US2011/048013` · `特許第5617402号`
· `61/375,208` · `US 8,977,546` · `EP 2 604 125` · `KR 10-1584772` ·
`ZL 2011 8 0040217.6` · `SDK-IP-2011-0288` · `Vega` · `オブジェクトクラスタリング`
· `object clustering` · `菱和電子` · `Ryowa` · `SDS-IPL-2024-0611` ·
`IG-SR-2025-0007` · `IPOPS-MIG-2016-004` · `Kagami` · `加賀美` · `Morisue` ·
`森末` · `一色` · `Nyeholt` · `Okonkwo-Lind` · `Utsugi` · `宇津木` · `芦谷`

**This string MUST appear, on the wrong family, in batch A:** `MAL-2010-0392`.

---

## 1. Shared Marsden address book

Any Marsden person who appears in a distractor **must** use exactly these
strings, byte for byte. Do not invent new Marsden staff outside this list.

```
Eleanor Bricknell <eleanor.bricknell@marsdenlabs.com>          Chief IP Counsel, San Mateo, to 2019
Beatrix Hollerith <beatrix.hollerith@marsdenlabs.com>          European Patent Attorney, Munich, 2007-
Roswell Vantassel <roswell.vantassel@marsdenlabs.com>          SVP Licensing, San Mateo, 2006-
Marisol Etxeberria <marisol.etxeberria@marsdenlabs.com>        VP & Chief IP Counsel, San Mateo, 2020-
Trevor Ashimolowo <trevor.ashimolowo@marsdenlabs.com>          Senior IP Counsel, San Mateo, 2018-
Bettina Crozier <bettina.crozier@marsdenlabs.com>              Director, IP Operations, San Mateo, 2017-
Fenella Drozdov <fenella.drozdov@marsdenlabs.com>              Director, Information Governance, 2015-
Osamu Sonoda <o.sonoda@marsdenlabs.com>                        知的財産部長, Marsden Japan, Yokohama, 2017-
Chihiro Kuroiwa <c.kuroiwa@marsdenlabs.com>                    特許エンジニア, Marsden Japan, 2019-
Se-hoon Park <s.park@marsdenlabs.com>                          IP Manager, Marsden Korea, Seoul, 2014-
Jianing Lu <j.lu@marsdenlabs.com>                              IP Counsel, Marsden Shanghai, 2016-
Marsden IP Docket <ip-docket@marsdenlabs.com>
Marsden IP Team <ip-team@marsdenlabs.com>
```

Additional Marsden staff you MAY use (distractor-only, but the same rule
applies — identical strings every time):

```
Halvard Ostenfeld <halvard.ostenfeld@marsdenlabs.com>          SVP Corporate Development, 2004-2021
Priyasha Nandakumar <priyasha.nandakumar@marsdenlabs.com>      IP Counsel, San Mateo, 2013-
Dermot Achinstein <dermot.achinstein@marsdenlabs.com>          Patent Agent, San Mateo, 2011-
Yolande Grimbeek <yolande.grimbeek@marsdenlabs.com>            IP Operations Analyst, San Mateo, 2016-
Wendell Aduba-Reiss <wendell.aduba-reiss@marsdenlabs.com>      Director, Standards, San Mateo, 2009-
Ingrid Solheim-Baptista <ingrid.solheim-baptista@marsdenlabs.com>  Patent Paralegal, San Mateo, 2008-2020
Kwabena Ofori-Lund <kwabena.ofori-lund@marsdenlabs.com>        Senior Patent Counsel, San Mateo, 2015-
Annika Vorderbrück <annika.vorderbrueck@marsdenlabs.com>       Patent Attorney, Marsden Europe, Munich, 2014-
Tomás Renaudin-Whyte <tomas.renaudin-whyte@marsdenlabs.com>    Licensing Manager, San Mateo, 2012-
```

Counterparties from the signal that you MAY reuse (identical strings):

```
海田 隆志 <t.kaida@shinonome-denki.co.jp>       知的財産部長, 東雲電機, to March 2017
新開 果林 <k.shinkai@shinonome-denki.co.jp>     知的財産部, 東雲電機, 2016-
蒲生 亮太 <gamo@nakanoshima-law.jp>             弁護士, 中之島総合法律事務所
皆川 悠子 <minagawa@yodo-naniwa-ip.jp>          弁理士, 淀川・浪速国際特許業務法人
Adrienne Whitcomb <awhitcomb@whitcombreyes.com> Whitcomb Reyes LLP
```

Everyone else is yours to invent, inside your batch only.

---

## 2. Format — reproduce exactly

```
**Email-1**··
To: Display Name <local@domain>··
From: Display Name <local@domain>··
Cc: Display Name <local@domain>··
Subject: ...··
Date: March 08, 2016, 14:05··
References:··
Body:··
First line of the body.

Second paragraph.
```

- `··` means **exactly two trailing spaces**. Every header field line ends with
  them. `Cc:` is optional; omit the line entirely if unused.
- `Date:` is exactly `Month DD, YYYY, HH:MM` — full English month name,
  zero-padded day, 24-hour clock, **even on Japanese, Korean, Chinese and
  German messages**. The header is machine format; only the body is localized.
- **No `Attachment:` lines anywhere in this file.**
- Number your messages `**Email-1**` upward **within your batch only**, with no
  gaps. `References:` may name only messages **earlier in your own batch**.
  I will renumber and rewrite references when I merge the four batches.
- A reply's minute must differ from its parent's minute. Vary times across
  06:00–20:00.
- **No weekend dates and no US federal holidays.** Check each date.
- One display name maps to exactly one address and vice versa, throughout.

---

## 3. Language

A non-English message is written **wholly** in that language: subject line,
body, signature block. No English gloss, no bilingual summary. That is the
point — an English-only index must not be able to see it.

Per-batch language quota is in the batch brief. Overall target across the file:
about 40 Japanese, 12 Korean, 12 Chinese, 12 German, the rest English.

English text is **American**: license, program, organize, analyze, color.

---

## 4. Domain vocabulary — get it right, a patent professional will read this

- National/regional phase: **30 months** for JP, CN, US, BR; **31 months** for
  EP, KR, IN. CN extendable to 32 with a surcharge.
- JP request for examination: **3 years from the filing date** (for a PCT case,
  the international filing date). Terms: 出願審査請求, 拒絶理由通知書, 意見書,
  手続補正書, 拒絶査定, 特許査定, 設定登録. Response for a foreign applicant:
  **3 months**, extendable by 3.
- JP annuities: years 1–3 paid as a lump sum within 30 days of the 特許査定,
  then annually from year 4. **No annuities on pending JP, KR or CN cases.** The
  EPO charges renewal fees on applications from the **third year**; Germany
  likewise on applications and patents.
- EPO: opposition **9 months from the mention of grant**; Rule 71(3)
  communication with a **four-month non-extendable** period to pay the grant fee
  and file claim translations into the other two official languages. London
  Agreement in force from 2008. **Unitary Patent and the UPC from 1 June 2023**;
  a unitary patent cannot be opted out.
- China: **SIPO before 2018, CNIPA after.** 专利复审委员会 (PRB) before
  **1 April 2019**, 复审和无效审理部 after. First office action response 4
  months, later ones 2 months. Foreign filing licence / 保密审查 required under
  Art. 19 for inventions made in China.
- Korea: **KIPO** throughout this corpus (it became MOIP only in October 2025).
  의견제출통지서, 의견서, 보정서. Response period **2 months** in this era.
  Request for examination 3 years from filing for applications filed on or after
  1 March 2017, 5 years before that.
- Japanese patent numbers: 特許第5,500,000号 ≈ May 2014; 特許第5,800,000号 ≈
  October 2015; 特許第6,000,000号 is not reached until late September 2016.
- Co-ownership law, if you touch it: Japan Art. 73 — work freely, **licence
  needs consent of all**; Art. 38 joint filing, breach is an invalidity ground
  under Art. 123(1)(ii) with **no time limit**; Art. 74 transfer claim only for
  applications filed **on or after 1 April 2012**. Korea Art. 99 mirrors Japan;
  Art. 44 is the joint-filing rule. China Art. 14 — a co-owner **may** grant a
  non-exclusive licence unilaterally, royalties shared. US 35 U.S.C. § 262 plus
  *Schering*, *Ethicon*, *STC.UNM*. Germany §§ 741 ff. BGB — licence needs
  consent of all.
- Systems in use at Marsden: legacy **PALLAS** (in-house, 1999, decommissioned
  June 2018), current **Veritan IPM** (cut over **February 19, 2016**). Program
  codes `JD-xxx-YY` (joint development), `IN-xxx-YY` (licensed in). Veritan's
  `Ownership Status` is a controlled field: `Sole`, `Joint`, `Licensed-In`.
- Never use "PatSnap" as a docketing system; it is search and analytics.

---

## 5. Batch A — `D-1` to `D-40` — the same number, the wrong family

**Language quota: 26 English, 8 Japanese, 4 German, 2 Chinese.**

### A1. The San Mateo `MAL-2010-0392` (14 messages, 2010–2019)

The single most important trap in the corpus. Until the January 2013 docket
harmonization, San Mateo, Yokohama and Munich each ran an independent
`MAL-YYYY-NNNN` series restarting at 0001 every January. **San Mateo's
`MAL-2010-0392` is a completely different family** and it keeps the bare number
after harmonization, because only the Yokohama series was re-prefixed.

| Fact | Value |
|---|---|
| Title | Adaptive microphone-array beamforming for conference endpoints |
| Docket | `MAL-2010-0392` — say **San Mateo series** where a message is careful, and **omit the series** in at least six of the fourteen |
| Inventors | Hyacinth Delacroix, Bjørn Umbertsen (both Marsden San Mateo) |
| US provisional | 61/311,904, filed March 9, 2010 |
| PCT | PCT/US2011/027655, international filing date March 8, 2011 |
| Publication | **WO 2011/112480 A1**, September 15, 2011 |
| US patent | US 8,824,693 B2, issued September 2, 2014 |
| EP | EP 2 545 719 B1, granted June 24, 2015; **opposed by Kesselring Audiotechnik GmbH**, opposition filed March 18, 2016, rejected by the Opposition Division February 7, 2018 |
| JP | 特許第5731049号, registered April 24, 2015 |
| Ownership | **Sole. Marsden alone. No joint development program. No program code.** |

Write the arc: disclosure and filing, national phase, a JP 拒絶理由通知 and
response, the EPO Rule 71(3), the opposition and its rejection, a licensing
enquiry, and — this one matters — **two messages in which someone confuses the
two `MAL-2010-0392` matters and has to be corrected** (one in 2012, one in
2021). The 2021 one should be a royalty report that attributed the wrong family.

### A2. Transposed docket numbers (10 messages, 2011–2023)

Short arcs, two or three messages each, on unrelated inventions.

- `MAL-2010-0329` — "Sample rate conversion with fractional delay compensation."
- `MAL-2010-0932` — a **Munich series** matter, "Loudspeaker excursion limiting."
  German. Note in one message that the Munich series also collided with San
  Mateo before harmonization.
- `MAL-2011-0392` — "Bitstream error concealment for object metadata."
- `MAL-2010-0392D` — a **divisional of the San Mateo family**, filed 2013. This
  one is the nastiest: it looks like a suffix on the signal's number.

### A3. Number near-misses (8 messages, 2012–2024)

Each must appear in a message that is otherwise about something plausible.

`WO 2012/024513` (a third party's publication cited in a search report) ·
`WO 2012/025431` (a Marsden Munich family) · `WO 2011/024531` (a competitor's
publication) · `特許第5617042号` (a Marsden JP patent on a different family) ·
`特許第5167402号` (a third party's patent cited as prior art). Two of these
messages in Japanese.

### A4. Right person, wrong matter — 海田 隆志 (8 messages, 2009–2016)

海田 隆志 <t.kaida@shinonome-denki.co.jp> writes about other things. Japanese.

- **`MAL-2009-0271` — THE QUALIFIED TWIN.** A confirmation letter from Kaida
  dated **February 22, 2011** on a *different* Marsden family (title: "Metadata
  carriage for dialogue enhancement"), worded almost identically to the signal's
  needle — **except that it is expressly limited 「日本国内において」, to Japan.**
  Outside Japan the co-ownership stands. Write the 2011 letter and one 2013
  message referring back to it. Never state or imply that this confirmation
  covers any other family.
- **`MAL-2012-0114`** — Kaida declines to give a confirmation at all, saying the
  invention *is* inside Annex A of the Shinonome agreement and the parties should
  file jointly. Two messages, 2012. This is the one that shows Kaida did not
  simply sign whatever he was asked to sign, which makes the signal's letter
  stronger and makes this message a tempting wrong citation.
- Three or four routine program-administration messages from Kaida: meeting
  logistics, a test-vector delivery, a change of contact.

---

## 6. Batch B — `D-41` to `D-80` — Annex A everywhere, and five companies called Shinonome

**Language quota: 22 English, 10 Japanese, 4 German, 2 Korean, 2 Chinese.**

### B1. Twenty other Annex A's (20 messages, 2009–2024)

Twenty messages, each carrying an `Annex A` or `別紙A`, none of them the
Shinonome joint development agreement's. Spread them across:

- The **Chenwei Microsystems** joint development agreement (`JD-CHW-12`,
  executed March 2012) — its Annex A is a list of six work packages, and its
  Article 5 says the *opposite*: everything arising in the program is jointly
  owned **whether or not** within Annex A. Chinese and English.
- The **Hanyoung Precision** joint development agreement (`JD-HYP-10`, executed
  January 2010) — same form of agreement as Shinonome's, same Annex A structure.
  (Batch C owns the confirmation letter; batch B owns the agreement traffic.)
- A **component supply agreement** with an Annex A of part numbers.
- A **mutual NDA** with an Annex A listing permitted recipients.
- A **standards licensing agreement** with an Annex A of essential claims.
- A **sponsored research agreement** with a university whose Annex A defines the
  research plan and whose Article 7 gives the university a share.
- An **annuity services agreement** with an Annex A of jurisdictions.

At least five of the twenty must be about **ownership** under their Annex A, so
that an identifier search on `Annex A` or `別紙A` returns ownership language on
the wrong agreement.

### B2. The Shinonome group name collisions (20 messages, 2012–2025)

Five distinct legal entities. Every message must make the entity identifiable
from its own subject line or first paragraph, but only if the reader looks.

| Entity | Domain | What it is |
|---|---|---|
| 東雲電機株式会社 / Shinonome Electric Co., Ltd. | `shinonome-denki.co.jp` | The signal's counterparty. Osaka. |
| 東雲デバイスソリューションズ株式会社 / Shinonome Device Solutions K.K. | `shinonome-ds.co.jp` | Carved out April 2022. |
| 東雲セミコンダクター株式会社 / Shinonome Semiconductor Co., Ltd. | `shinonome-semi.co.jp` | A separate group company, Kumamoto. **A Marsden licensee**, not a partner. |
| Shinonome America, Inc. | `shinonome-america.com` | US sales subsidiary, Irvine CA. Handles the group's US trademark portfolio. Nothing to do with patents. |
| 東雲精密工業株式会社 / Shinonome Seimitsu Kogyo Co., Ltd. | `shinonome-seimitsu.co.jp` | **No relation to the group.** Precision machining, Nagano. Different owners, same characters. |
| 東雲興業株式会社 / Shinonome Kogyo Co., Ltd. | `shinonome-kogyo.co.jp` | **No relation.** Construction. Appears once, in a facilities email about the Yokohama fit-out. |

Include:

- **The adjacent-date collision.** 東雲精密工業 asserts ownership of a *different*
  Marsden family, `MAL-2013-0771`, by letter dated **November 19, 2024** — one
  week after the real assertion. Different family, different agreement, unrelated
  company, and it is **correct**: Marsden concedes and adds them as co-applicant
  on a pending divisional. Three or four messages, Japanese.
- Licensing traffic with 東雲セミコンダクター that repeatedly says "Shinonome" with
  no qualifier in the subject line.
- A trademark matter with Shinonome America that has nothing to do with any of it.

---

## 7. Batch C — `D-81` to `D-118` — the twin that inverts the verdict, and the family that really is co-owned

**Language quota: 14 English, 10 Korean, 12 Japanese, 2 German.**

### C1. THE NEAR-MISS TWIN — Hanyoung Precision (16 messages, 2010–2020)

**한영정밀 주식회사 / Hanyoung Precision Co., Ltd.**, Ansan, `hanyoung-p.co.kr`.
Joint development program `JD-HYP-10`, agreement executed **January 14, 2010**,
on the same form as the Shinonome agreement, **term to March 31, 2014**.

The trap: on **May 18, 2011** — sixteen days before the signal's needle —
김도윤 (Do-yun Kim), 지식재산부장, sends Marsden Korea a confirmation letter on
family `MAL-2011-0304` ("Speaker protection using thermal modeling") in wording
almost identical to the Shinonome letter, **except for the final sentence**:

> 「본 확인은 공동개발계약의 유효기간 동안에 한한다.」
> (This confirmation is limited to the term of the joint development agreement.)

The agreement expired **March 31, 2014**. Write:

- the 2011 letter and its covering message (Korean),
- a 2013 message treating it as settled,
- **2019: it fails.** Hanyoung asserts co-ownership of `MAL-2011-0304`; Marsden
  relies on the 2011 letter; Hanyoung points to the final sentence; outside
  counsel advises that the confirmation lapsed on April 1, 2014. Korean and
  English.
- **the outcome: Marsden concedes** and signs a separate co-ownership and
  royalty-sharing agreement on **November 8, 2019**, registered in Veritan.
  Marsden pays **KRW 940,000,000**.
- a 2020 lessons-learned message that says, in terms, "check whether the
  confirmation is time-limited" — the right lesson, on the wrong document.

Anyone who cites the Hanyoung letter as a parallel to the Shinonome letter loses
the argument, because Hanyoung's expired and Marsden lost on it.

### C2. THE INVERTED PREMISE — `MAL-2011-0455`, genuinely co-owned (14 messages, 2011–2023)

A Marsden family that **really is** jointly owned with 東雲電機株式会社, properly
and without controversy.

| Fact | Value |
|---|---|
| Title | Encoder-side loudness measurement with cross-channel gating |
| Docket | `MAL-2011-0455`, program code `JD-SHN-09` |
| Why joint | Squarely inside Annex A work package **A-2**. Both companies' engineers on the disclosure. |
| Filing | Filed **jointly** in both names under Art. 38, PCT/JP2012/059118, WO 2012/144622 |
| JP | 特許第5498271号, registered March 14, 2014, two proprietors |
| Practice | Every licence under it has a signed consent from Shinonome, per Art. 73(3) and Art. 7 of the JDA. Consents in 2015, 2017, 2019, 2021, 2023. |

Write it as completely routine. Japanese and English. **This is the inverted
premise**: a reader who merges it with the signal concludes that co-ownership
with Shinonome was normal and that the 0392 family is probably the same. Every
message must be individually correct and boring.

Include one message where Shinonome **refuses** a consent request (2019, a
licensee in a market where Shinonome competes), because that is what makes
co-ownership expensive and is exactly what Marsden avoided on the 0392 family.

### C3. The qualified twin bites — `MAL-2009-0271` outside Japan (8 messages, 2016–2019)

Batch A writes Kaida's Japan-limited confirmation of February 22, 2011. This is
what happens next. In 2016 Marsden wants to license `MAL-2009-0271` to a German
licensee; the EP member is co-owned; German law needs the consent of all
co-owners; Shinonome's confirmation does not reach Germany because it says
「日本国内において」. Consent is sought, negotiated and granted in 2017 for a fee
of **EUR 310,000**. German and Japanese and English.

---

## 8. Batch D — `D-119` to `D-155` — the anti-precedent, and everything else that looks like the story

**Language quota: 17 English, 10 Chinese, 6 Japanese, 2 German, 2 Korean.**

### D1. THE ANTI-PRECEDENT — `MAL-2012-0688`, Chenwei Microsystems (16 messages, 2012–2023)

**辰威微电子有限公司 / Chenwei Microsystems Co., Ltd.**, Shanghai,
`chenwei-micro.com.cn`. Joint development program `JD-CHW-12`.

The same story shape as the signal, and it ends the other way.

- 2012–2013: family `MAL-2012-0688` ("Object metadata compression for
  low-bitrate transport") is developed during the program. Marsden believes it is
  outside the Chenwei agreement's Annex A and files alone. **Nobody asks for a
  confirmation letter.** One message should show someone deciding not to bother.
- 2016: the same PALLAS to Veritan migration; same derived `Joint` value.
- **October 2022:** Chenwei asserts co-ownership.
- **January 2023: the journal archive is searched.** Same team, same method,
  same nineteen-minute search. **It returns nothing.** There is no confirmation
  letter, because none was ever requested. What the archive does return is a
  2013 message from a Marsden engineer describing Chenwei's contribution to the
  very feature that was claimed — which makes it worse.
- Chenwei's agreement's Article 5 assigns everything arising in the program
  regardless of Annex A.
- **Outcome, June 2023: Marsden concedes.** Co-ownership recorded, a
  royalty-sharing agreement signed, Marsden pays **USD 1,240,000** and gives up
  the right to license in China without consent.

Chinese-heavy. This is the message set that proves the tool is reading evidence
rather than pattern-matching a story: same archive, same search, opposite
answer, because the evidence is not there.

### D2. Other archive searches (8 messages, 2019–2024)

Four short arcs in which the journal archive is searched on other matters:
one where it finds a document that **damages** Marsden's position, one where it
finds nothing and the matter settles anyway, one where the search is refused on
cost, one where it resolves an inventorship question. English and Japanese.

### D3. Migration fallout on other fields (7 messages, 2016–2023)

The 2016 migration derived other things wrongly too: renewal responsibility on
94 matters, jurisdiction group on 12, a licensee list. Never about ownership.
These make the migration story ordinary, so that the signal's version has to be
distinguished on its facts rather than recognized by shape.

### D4. General adverse and routine traffic (6 messages, 2013–2025)

An EPO opposition Marsden loses; a Chinese invalidation Marsden wins; a Korean
office action; a US inter partes review petition against a Marsden patent
(2018); a lapsed annuity and its restoration; an inventorship correction under
37 CFR 1.48. German, Chinese, Korean, English.

---

## 9. What will get a batch rejected

- An `Attachment:` line.
- A header line without exactly two trailing spaces.
- A forbidden string from §0.
- A Marsden person with an address that is not in §1, or two spellings of one
  person, or one address on two names.
- A date on a weekend or a US federal holiday.
- A non-English message with an English summary in it.
- A reply whose minute matches its parent's.
- Any message that could be cited **in support of** the signal's conclusion. A
  distractor that helps is not a distractor.
- Anachronism: CNIPA before 2018, UPC before June 2023, a 特許第6,xxx,xxx号 before
  October 2016, an annuity on a pending Japanese application.
