# Design brief — `shinonome-0392` — NEVER INGEST

Sixth corpus in the series. Vertical: **global corporate patent filing / prosecution**,
seen from inside a US technology licensor's in-house IP department, with regional
IP staff in Japan, Germany, Korea and China.

**The new capability this corpus exists to prove: cross-language retrieval.**
The needle, the precedent, and the document that falsifies the customer's own
system of record are all in **Japanese**. The near-miss twin that inverts the
verdict is in **Korean**. Supporting analysis is in **German** and **Chinese**.
An English-only reader — which is what the customer's docketing system and its
US HQ both are — gets the wrong answer with high confidence.

Everything is fictitious. The legal framework is real and was verified against
primary sources during the build (§8).

---

## 1. The six beats

1. **The needle.** June 3, 2011 — 海田 隆志 (Takashi Kaida), 知的財産部長 of
   東雲電機株式会社 (Shinonome Electric Co., Ltd.), Osaka, writes **in Japanese** to
   加賀美 涼子 (Ryoko Kagami), IP Manager of マースデン・ジャパン株式会社, attaching a
   sealed 確認書 that states:

   > 本件発明は、2009年11月16日付共同開発契約 別紙A に定める対象範囲に含まれず、
   > 貴社の単独所有であることを確認いたします。当社は本件発明及びこれに基づく国内外の
   > 特許を受ける権利について何らの持分も主張せず、第三者に対する実施許諾も行いません。
   > 本確認は期間の定めなく効力を有します。

   ("We confirm that the present invention does not fall within the scope defined
   in Annex A to the Joint Development Agreement of November 16, 2009, and is the
   sole property of your company. We assert no share whatsoever in the invention
   or in the right to obtain patents on it in Japan or abroad, and we will not
   grant licences to third parties. This confirmation is effective without
   limitation of period.")

   Marsden asked for it **because Japan Patent Act Art. 38 makes joint filing
   mandatory where the right to obtain the patent is co-owned, and a breach is an
   invalidity ground under Art. 123(1)(ii)**. The confirmation was obtained
   deliberately, before the PCT was filed in Marsden's sole name.

2. **Both systems lose it.** The **February 2016 PALLAS → Veritan IPM migration**
   carried, per matter: bibliographic data, register data bought from a data
   provider, granted documents, and correspondence dated **on or after
   January 1, 2014**. Two things followed:
   - Veritan's `Ownership Status` is a *controlled* field (`Sole | Joint |
     Licensed-In`) and PALLAS had no equivalent. The migration **derived** it from
     the matter's program code. Matter `MAL-2010-0392` (Yokohama series) had been
     opened under program code `JD-SHN-09` — the joint-development program with
     Shinonome — because the invention-disclosure form's "first disclosed at"
     field named the JD-SHN-09 quarterly review. It therefore migrated as
     **`Joint — Shinonome Electric Co., Ltd. (50%)`**.
   - PALLAS's free-text `OWNERSHIP BASIS` note — *"Sole — Shinonome confirmation
     2011-06-03 (JA), corr. file"* — had **no target field** and was dropped.

   PALLAS was decommissioned in 2018 and its tape images culled in 2023 under the
   seven-year rule (the images were written at the February 2016 cutover; seven
   years from creation falls in February 2023). Marsden Japan's Yokohama file room was cleared in the 2016
   office consolidation. On the other side, Shinonome Electric changed mail
   platform in 2018 with a seven-year retention, and the April 2022 carve-out of
   the device business to **Shinonome Device Solutions K.K. (SDS)** transferred
   only the executed agreements listed in the carve-out schedule — no
   correspondence.

   **So Marsden's own system of record says the claimant is right**, and the only
   ownership document on the matter is the **English courtesy translation** of the
   2009 JDA, whose Article 5.1 reads "all improvements arising therefrom shall be
   jointly owned by the Parties." The Japanese original — which is the governing
   text under Article 18 — reads 「別紙Aに定める対象範囲において生じた発明」
   ("inventions arising within the scope defined in Annex A"). The translator
   collapsed the defined field into "therefrom." **Two independent wrong sources,
   both corrected by the original-language record.**

   **The translation has to be bad all the way through, or the trap does not
   close.** In the English text: Article 1 defines "the Joint Development" as
   joint R&D "in the field of next-generation object-based audio coding" with no
   reference to Annex A, so "therefrom" has nothing to attach to but the whole
   field; Article 4 describes work packages and defines no scope; Article 5.2
   loses the Japanese sentence saying that disclosure at a review meeting does
   not affect sole ownership; Article 8 loses the Japanese sentence saying the
   cost-allocation classification is not a statement of ownership; and the annex
   note says only that Annexes A and B are not included, with no instruction to
   go and read them. If any one of those four survives into the English, a
   reader at headquarters answers SDS in November 2024 out of the document
   already in Veritan and there is no story.

3. **Everyone has left.** Kaida retired March 2017. Kagami left Marsden in 2016.
   Nyeholt left 2015; Bricknell retired 2019; Okonkwo-Lind left 2015. The Japanese
   associate firm 淀川国際特許事務所 merged in 2018 and destroyed its pre-2015 paper
   files in 2022; 弁理士 中臣 圭介 retired in 2019.

4. **The claim.** **November 12, 2024** — 宇津木 遼 (Ryō Utsugi), General Manager,
   IP Licensing, Shinonome Device Solutions K.K., asserts that the invention arose
   within the Annex A field, that the right to obtain the patent was therefore
   co-owned, that Marsden's sole-name PCT filing breached Art. 38, and demands
   (a) a confirmatory transfer of a 50% share across the family and (b) an
   accounting of **¥4,005,000,000** (≈ **USD 26,700,000** at the ¥150/USD rate
   Marsden uses for reserves) for 2019–2024. If refused, SDS will file 無効審判
   against 特許第5617402号 on Art. 123(1)(ii).

   **Why the demand lands on November 12, 2024:** the Japanese patent was
   registered on **December 12, 2014**. A money claim arising at grant sits under
   the pre-2020 Civil Code (改正民法附則10条4項) and therefore under the old
   ten-year objective prescription of 民法167条1項. SDS filed four weeks before
   the boundary.

5. **The archive produces it — plus the precedent.** **January 14, 2025** — the
   mail journal archive, which has journaled every mailbox on the corporate tenant
   since 2008 (Yokohama included) and which was never migrated because it is not a
   docketing system, returns 241,700 messages for 2009–2014 across the Yokohama,
   San Mateo, Munich, Seoul and Shanghai mailboxes, including the **eleven-message Osaka sequence**, the sealed
   確認書 PDF intact, and the **Japanese original** of the 2009 JDA with 別紙A.
   Then a second pass — run **January 17, 2025** with the direction filter off,
   reported as a separate addendum and carried by Email-33 on **January 21, 2025**
   — produces the precedent: the **October 21, 2013** message in which Kaida
   turned away a licence request from 菱和電子株式会社 (Ryowa Electronics) under
   the very family, cc'ing Marsden Japan, writing that Shinonome had no share and
   no authority to license and that Ryowa should approach Marsden. Two years after
   the confirmation, with no dispute pending, to a third party, and at the cost of
   a licence fee Shinonome could have taken.

   **Do not write it as "unprompted."** Kaida is answering Ryowa's licence
   enquiry of October 15, 2013, and that enquiry is quoted in his own first line.
   What is unprompted is his citing the 2011 確認書 by date: nobody asked him
   whether such a letter existed. Emails 18 and 33 and the response letter must
   all say the narrow thing, because the wide thing is answerable from the exhibit
   itself.

6. **The claim collapses.** **March 6, 2025** — SDS withdraws the assertion and the
   ¥4,005,000,000 accounting demand in full and undertakes not to file 無効審判.
   **April 18, 2025** — Shinonome Electric (甲), SDS (乙), Marsden Audio
   Laboratories, Inc. (丙) **and マースデン・ジャパン株式会社 (丁)** execute a 合意書
   containing a 権利帰属確認条項, a quitclaim of any share that may be found to
   exist, a 不起訴の合意 covering 無効審判 on entitlement grounds, and a 清算条項.
   Marsden Japan is a party because it is the addressee of the assertion, the
   employer of the inventors, the addressee of the 確認書 and a client of the
   回答書 — a 清算条項 that does not name it releases nothing as to it.
   No payment either way. Marsden's total cost: **USD 487,000**.

---

## 2. Identifiers, and how they collide

| Identifier | Correct referent | The collision |
|---|---|---|
| `MAL-2010-0392` | The codec family (Yokohama series) | **Two Marsden families hold it.** Until the January 2013 docket harmonization, San Mateo, Yokohama and Munich each ran an independent `MAL-YYYY-NNNN` series restarting at 0001 every year. San Mateo's `MAL-2010-0392` is an unrelated **adaptive microphone-array beamforming** family. After harmonization the Yokohama case is `MAL-JP-2010-0392`; the San Mateo case keeps the bare number. **All pre-2013 correspondence — including the needle's thread — uses the bare number.** |
| `別紙A` / `Annex A` | The field definition in the 2009 Shinonome JDA | ~30 distractor messages carry an Annex A on some other agreement, several of them ownership provisions. |
| `WO 2012/024531` | The PCT publication | Near-misses in daily use: `WO 2012/024513`, `WO 2012/025431`, `WO 2011/024531`. |
| `特許第5617402号` | The granted JP patent | Near-misses: `特許第5617042号`, `特許第5167402号`. |
| Docket transpositions | — | `MAL-2010-0329`, `MAL-2010-0932`, `MAL-2011-0392`, `MAL-2010-0392D` (a divisional). |
| **東雲 / Shinonome** | Shinonome Electric Co., Ltd. (Osaka) | 東雲デバイスソリューションズ株式会社 (SDS), 東雲セミコンダクター株式会社, Shinonome America, Inc., 東雲精密工業株式会社, and an entirely unrelated 東雲興業株式会社 (construction). |
| `JD-SHN-09` | The program code | `JD-SHN-12`, `JD-HYP-10` (Hanyoung), `JD-CHW-12` (Chenwei). |

**Never search `MAL-2010-0392` alone.** **Never scope by 東雲 alone.**
**Never scope by 海田 alone** — he signs confirmations on three other families,
two of which say something different.

---

## 3. Cast — signal file

Career windows are load-bearing: no message from anyone outside their window.

### Marsden Audio Laboratories, Inc. — `marsdenlabs.com` (one global tenant)

| Person | Role | Site | Window |
|---|---|---|---|
| Eleanor Bricknell | Chief IP Counsel | San Mateo | 1998–2019 (retired) |
| Curtis Nyeholt | Senior Patent Counsel | San Mateo | 2004–2015 |
| Adaeze Okonkwo-Lind | IP Operations Manager (docketing) | San Mateo | 2006–2015 |
| 加賀美 涼子 / Ryoko Kagami | 知的財産マネージャー | Yokohama | 2005–2016 |
| 森末 健吾 / Kengo Morisue | Senior Engineer, audio lab | Yokohama | 2003–2018 |
| Beatrix Hollerith | European Patent Attorney | Munich | 2007– |
| Roswell Vantassel | SVP, Licensing | San Mateo | 2006– |
| Marisol Etxeberria | VP & Chief IP Counsel | San Mateo | 2020– |
| Trevor Ashimolowo | Senior IP Counsel, prosecution | San Mateo | 2018– |
| Bettina Crozier | Director, IP Operations | San Mateo | 2017– |
| Fenella Drozdov | Director, Information Governance | San Mateo | 2015– |
| 園田 修 / Osamu Sonoda | 知的財産部長, マースデン・ジャパン | Yokohama | 2017– |
| 黒岩 千尋 / Chihiro Kuroiwa | 特許エンジニア | Yokohama | 2019– |
| 박세훈 / Se-hoon Park | IP Manager, Marsden Korea | Seoul | 2014– |
| 陆嘉宁 / Jianing Lu | IP Counsel, Marsden Shanghai | Shanghai | 2016– |

### 東雲電機株式会社 / Shinonome Electric Co., Ltd. — `shinonome-denki.co.jp`

| Person | Role | Window |
|---|---|---|
| 海田 隆志 / Takashi Kaida | 知的財産部長 | 1994–2017 (retired March 2017) |
| 芦谷 美奈 / Mina Ashiya | 知的財産部 主任 | 2007–2019 |
| 新開 果林 / Karin Shinkai | 知的財産部 | 2015– (answers the 2024 enquiry; knows nothing of 2011) |

### 東雲デバイスソリューションズ株式会社 / SDS — `shinonome-ds.co.jp` (from April 2022)

| Person | Role | Window |
|---|---|---|
| 宇津木 遼 / Ryō Utsugi | 知的財産ライセンス部長 | 2023– |

### Outside advisers

| Person | Firm | Window |
|---|---|---|
| 弁理士 中臣 圭介 / Keisuke Nakatomi | 淀川国際特許事務所, Osaka (merged 2018) | 1996–2019 |
| 弁理士 皆川 悠子 / Yūko Minagawa | 淀川・浪速国際特許業務法人 | 2012– |
| Adrienne Whitcomb | Whitcomb Reyes LLP, Palo Alto | 2009– |
| 弁護士 蒲生 亮太 / Ryōta Gamō | 中之島総合法律事務所, Osaka | 2008– |
| 桜井 大輔 / Daisuke Sakurai | 菱和電子株式会社 (Ryowa Electronics) | 2009–2016 |

---

## 4. The technology and the numbers — computed once

| Fact | Value |
|---|---|
| Product family | Marsden **Vantage** immersive audio format |
| The invention | Decoder-side object clustering under a channel budget, adapted to the rendering environment |
| Internal project | **Vega** (Marsden-internal roadmap, Yokohama audio lab) |
| Inventors | 森末 健吾, 一色 綾乃 (Ayano Isshiki) |
| Invention completed | February 26, 2010 |
| Invention disclosure | March 8, 2010 |
| Shinonome JDA | executed November 16, 2009; **term January 1, 2010 – December 31, 2013** (Art. 16). *Not* 2014-03-31 — that is the Hanyoung JDA (§6, the near-miss twin), and the two must never share a date. |
| Matter opened | May 24, 2010 — `MAL-2010-0392`, program code `JD-SHN-09` |
| US provisional | 61/375,208 — filed **August 19, 2010** (priority date) |
| PCT | PCT/US2011/048013 — **international filing date August 17, 2011**, RO/US, EPO as ISA |
| PCT publication | **WO 2012/024531 A1**, February 23, 2012 |
| JP national phase | 特願2013-525118, entered February 12, 2013 (30 months from priority = Feb 19, 2013) |
| JP examination requested | June 18, 2013 (3-year deadline from IFD = August 17, 2014) |
| JP grant | **特許第5617402号**, 設定登録 **December 12, 2014** |
| EP | EP 2 604 125 B1, granted March 11, 2015; validated DE, FR, GB, IT, NL, SE |
| KR | KR 10-1584772, registered January 6, 2016 |
| CN | ZL 2011 8 0040217.6, granted September 23, 2015 |
| US | US 8,977,546 B2, issued March 10, 2015 |
| Family expiry | **August 17, 2031** (20 years from the international filing date) |
| Royalties attributable to the family, 2019–2024 | **USD 53,400,000** across 14 licensees |
| Average per year | **USD 8,900,000** |
| SDS demand (50% of the above) | **¥4,005,000,000 ≈ USD 26,700,000** at ¥150/USD |
| Forward exposure 2025 → expiry (6.6 yrs × 8.9M) | **≈ USD 58,700,000** |
| Marsden's total cost of the matter | **USD 487,000** |
| Archive messages searched, 2009–2014 | **241,700** |
| The Osaka sequence | **eleven** messages, September 30, 2010 – June 3, 2011 |
| Migration ownership audit | **61** matters carry a `JD-` code and all 61 migrated as `Joint`; a further **212** carry an agreement but no program code and migrated as `Sole`. **19 wrong: 14 of the 61 wrongly `Joint`, 5 of the 212 wrongly `Sole`.** The five wrongly-`Sole` cannot come from inside the 61 — rule 4.3 makes every `JD-` matter `Joint`. |
| Non-English governing agreements | **340** *matters*, audited by Ashimolowo (Email-40). Not 340 agreements: the scope note migrated 214 agreements, of which 118 are English translations of a foreign-language original. |

**Systems.** Legacy docketing: **PALLAS** (in-house, built 1999, decommissioned
2018, tapes culled 2023). Current: **Veritan IPM** (Veritan Group, cloud,
cut over **February 19, 2016**). The mail journal archive has journaled the
corporate tenant since 2008 and was never migrated.

---

## 5. Email plan — 40 messages, two eras

`LANG` is the language the body is written in. `att` = attachment count.

### Era 1 — 2009-11 → 2013-10 (18 messages)

| # | Date | Lang | What | Role | att |
|---|---|---|---|---|---|
| 1 | 2009-11-19 | EN | JDA executed; Japanese governing; Annex A defines the field; program code JD-SHN-09 | Supporting | 2 |
| 2 | 2010-03-08 | JA | 発明届出書 for the Vega decoder-clustering invention | The causation seed | 1 |
| 3 | 2010-04-21 | JA | Presented at the JD-SHN-09 quarterly review as background; Ashiya asks whether it is inside 別紙A | The causation seed | 0 |
| 4 | 2010-05-24 | EN | Matter opened `MAL-2010-0392`; program code taken from "first disclosed at"; warns of the San Mateo twin | The causation seed | 0 |
| 5 | 2010-08-19 | EN | US provisional filed; Art. 38 warning — settle ownership before the PCT | Supporting | 1 |
| 6 | 2010-09-30 | JA | Formal written request for confirmation | Supporting | 1 |
| 7 | 2010-11-10 | JA | Kaida: 知財委員会 will decide in December; preliminary view is out of scope | Supporting | 0 |
| 8 | 2011-01-27 | EN | **In-file noise** — EP renewal instructions, other families | In-file noise | 0 |
| 9 | 2011-03-15 | JA | Quarterly review minutes; 別紙A to be applied strictly | Supporting | 0 |
| **10** | **2011-06-03** | **JA** | **THE NEEDLE** — the 確認書 | **THE needle** | 1 |
| 11 | 2011-06-07 | EN | Kagami's two-line English gist to HQ — omits the no-licensing and no-expiry terms; forwards the JA PDF unread | The trap the tool must overcome | 1 |
| 12 | 2011-06-08 | EN | Okonkwo-Lind records it as a PALLAS free-text note; program code cannot be changed | The causation seed | 0 |
| 13 | 2011-08-17 | EN | PCT filed in sole name, IFD August 17, 2011 | Supporting | 1 |
| 14 | 2012-02-24 | EN | **In-file noise** — Munich office relocation, DPMA/EPO address change | In-file noise | 0 |
| 15 | 2013-02-14 | JA | National/regional phase entries reported by Nakatomi | Supporting | 0 |
| 16 | 2013-06-25 | EN | **In-file noise** — IDS cross-citation on another family | In-file noise | 0 |
| **17** | **2013-10-21** | **JA** | **THE PRECEDENT** — Kaida turns away Ryowa's licence request | **Precedent** | 0 |
| 18 | 2013-10-24 | EN | Kagami's one-line English file note about it | Cross-year link | 0 |

### Era 2 — 2024-11 → 2025-05 (22 messages)

| # | Date | Lang | What | Role | att |
|---|---|---|---|---|---|
| 19 | 2024-11-12 | JA | SDS asserts co-ownership; ¥4,005,000,000; 無効審判 threatened | Present-day thread start | 1 |
| 20 | 2024-11-13 | EN | Veritan says `Joint — Shinonome Electric (50%)`; the only ownership document is the English JDA translation | The trap the tool must overcome | 1 |
| 21 | 2024-11-15 | EN | Royalty exposure; the US co-owner consequences under §262 / *Ethicon* / *STC.UNM* | Supporting | 1 |
| 22 | 2024-11-18 | EN | Whitcomb: Art. 74 unavailable (pre-April-2012 IFD); prescription is at the boundary; **無効審判 has no time limit** | Supporting | 1 |
| 23 | 2024-11-21 | JA | Gamō concurs; the demand's timing is not a coincidence | Supporting | 0 |
| 24 | 2024-11-26 | EN | **In-file noise** — Q4 annuity batch instruction, other families | In-file noise | 0 |
| 25 | 2024-12-03 | EN | Veritan holds nothing before 2014-01-01; the 2016 migration scope note | The trap the tool must overcome | 1 |
| 26 | 2024-12-09 | JA | Yokohama file room cleared 2016; Yodogawa merged 2018, files destroyed 2022 | Supporting | 0 |
| 27 | 2024-12-12 | EN | **In-file noise** — UPC opt-out review of the 2015–2019 classical validations | In-file noise | 0 |
| 28 | 2024-12-17 | JA | Shinonome Electric's own systems lost it too; Kaida retired 2017 | Supporting | 0 |
| 29 | 2025-01-06 | EN | The journal archive was never migrated because it is not a docketing system | The product moment (setup) | 0 |
| **30** | **2025-01-14** | **EN** | **THE PRODUCT MOMENT** — 241,700 messages searched; the eleven-message Osaka sequence; the sealed 確認書; the Japanese original of the JDA | **The product moment** | 1 |
| 31 | 2025-01-15 | JA | Gamō reads the 確認書 and quotes the decisive sentence verbatim | Supporting | 0 |
| **32** | **2025-01-16** | **EN** | **The translation discrepancy** — 別紙A vs "arising therefrom"; Japanese governs | The product moment | 1 |
| **33** | **2025-01-21** | **JA** | **The precedent recovered** — carries the January 17 archive addendum | **Precedent** | 1 |
| 34 | 2025-01-28 | KO | Park: the Hanyoung confirmation looks identical but was limited to the JDA term — keep it out of the package | Supporting / precision warning | 0 |
| 35 | 2025-02-04 | DE | Hollerith: EP register shows Marsden sole throughout; German co-ownership under Art. 74 EPC / §§741 ff. BGB | Supporting | 0 |
| 36 | 2025-02-06 | ZH | Lu: PRC Patent Law Art. 14 — a co-owner may license non-exclusively unilaterally; China is where an adverse finding hurts most | Supporting | 0 |
| 37 | 2025-02-10 | JA | The response package goes to SDS — **contains the deliberate miscount ("ten")** | Formal rebuttal | 1 |
| **38** | **2025-03-06** | **JA** | **SDS withdraws in full** | **Outcome** | 0 |
| 39 | 2025-04-18 | EN | 合意書 executed — confirmation, quitclaim, 不起訴の合意, 清算条項; no payment | Outcome | 1 |
| **40** | **2025-05-14** | **EN** | **Causation** — a controlled field derived from a program code, and an English courtesy translation standing in for a Japanese governing text | **Causation** | 0 |

**In-file noise that is not part of either trail:** 8, 14, 16, 24, 27.

**Deliberate in-world inaccuracy:** Email-37's covering note says
「2011年の大阪往復書簡10通」 — *ten* messages in the 2011 Osaka sequence. It is
**eleven**. Email-30 and the archive search results attachment both state it
correctly. Documented in the grading key as intentional.

**NOT an error, and the plot:** the English courtesy translation of JDA Art. 5.1.
Never grade it as a corpus defect.

---

## 6. Distractor trap classes → concrete construction

| Trap class | Concrete build |
|---|---|
| Same number, wrong matter | San Mateo's `MAL-2010-0392` (adaptive microphone-array beamforming), a full 12-message arc with its own prosecution history. |
| Transposed numbers | `MAL-2010-0329`, `MAL-2010-0932`, `MAL-2011-0392`, `MAL-2010-0392D`, `WO 2012/024513`, `特許第5617042号`. |
| Same clause, wrong agreement | ~30 messages carrying an `Annex A` / `別紙A` on a different agreement, several of them ownership provisions. |
| Name collisions | 東雲デバイスソリューションズ, 東雲セミコンダクター, Shinonome America, 東雲精密工業, 東雲興業 (unrelated). |
| Right person, wrong matter | 海田 隆志 signs ownership confirmations on `MAL-2009-0271` and `MAL-2012-0114` — with different terms. |
| **The near-miss twin** | **한영정밀 / Hanyoung Precision Co., Ltd.**, program `JD-HYP-10`. Confirmation dated **2011-05-18**, in Korean, near-identical wording — but 「본 확인은 공동개발계약의 유효기간 동안에 한한다」, limited to the term of the JDA, **which expired 2014-03-31**. Citing it inverts the verdict. |
| **The qualified twin** | `MAL-2009-0271` — Kaida's confirmation is limited 「日本国内において」, Japan only, so co-ownership stands everywhere else. |
| **The inverted premise** | `MAL-2011-0455` — genuinely co-owned with Shinonome, properly filed jointly under Art. 38, consents exchanged for every licence. Merging it with the signal produces "co-ownership with Shinonome was normal." |
| **The anti-precedent** | `MAL-2012-0688` — Chenwei Microsystems (辰威微电子), program `JD-CHW-12`. Same "lost in the 2016 migration" story, the journal archive is searched, **nothing exists**, Marsden concedes co-ownership and pays **USD 1,240,000**. |
| Adjacent-date collisions | A second ownership assertion against Marsden from 東雲精密工業 dated **2024-11-19**, one week after the real one. |

---

## 7. Language budget

| File | JA | KO | ZH | DE | EN |
|---|---|---|---|---|---|
| Signal (40) | 16 | 1 | 1 | 1 | 21 |
| Distractors (155) | ~40 | ~12 | ~12 | ~12 | ~79 |
| Filler (6,000) | ~18% | ~5% | ~5% | ~5% | ~67% |

A non-English message is written wholly in that language — body, signature block
and subject line. That is what makes the retrieval test real: an English-only
index cannot see it at all.

---

## 8. Verified legal facts this corpus depends on

Sources checked during the build; do not "correct" these.

1. **Japan Patent Act Art. 38** — where the right to obtain a patent is co-owned,
   the application may be filed only by all co-owners jointly. Breach → refusal
   under Art. 49(ii) and **invalidity under Art. 123(1)(ii)**.
2. **Art. 123(3)** — an invalidation trial may be requested even after the patent
   has lapsed, and there is **no statutory time limit** on requesting one. There
   is no Patent Act analogue to the five-year 除斥期間 in 商標法47条.
3. **Art. 74 (transfer claim)** — introduced by 平成23年法律第63号, in force
   **1 April 2012**. **附則第2条第9項 limits it to applications filed on or after
   that date.** Under Art. 184-3(1) a PCT application is deemed filed in Japan on
   its **international filing date** — here **August 17, 2011**. So the transfer
   claim is not available to SDS and invalidation is the only real lever. This is
   the single most load-bearing fact in the corpus.
4. **Art. 73** — (1) no co-owner may assign or pledge its share without the consent
   of all; (2) each may **work** the invention without consent unless otherwise
   agreed; (3) **no co-owner may grant an exclusive or non-exclusive licence
   without the consent of all**.
5. **Art. 33(3) / 34(1) / 34(4)** — a co-owned right to obtain a patent cannot have
   a share assigned without consent; a pre-filing succession is not effective
   against third parties unless the successor files; a post-filing transfer has no
   effect without notification to the Commissioner.
6. **Art. 98(1)(i)** — transfer of a granted patent (other than by general
   succession) **has no effect unless registered**. Registration is constitutive in
   Japan, unlike the USPTO.
7. **Art. 35, pre-2015** — for an invention made in **2010**, the right to obtain
   the patent **arises in the inventor** and passes to the employer by 予約承継
   under the 職務発明規程. Original employer vesting applies only to inventions made
   on or after 1 April 2016. Marsden's title is therefore derivative — and so
   would SDS's be.
   **The corpus must carry the chain, because the entities are not the same.**
   森末 and 一色 are employees of **マースデン・ジャパン株式会社**; the JDA party,
   the PCT applicant and the patentee everywhere is **Marsden Audio Laboratories,
   Inc.** So: inventors → Marsden Japan K.K. by 予約承継 → MAL by deed of
   assignment, recorded in the PCT filing receipt's docket note. And the 確認書,
   which is addressed to Marsden Japan, defines 「貴社」 as the two of them
   together (「貴社グループ」) in its preamble — the operative sentence of 第1項 is
   never touched, because it is quoted in four places.
8. **35 U.S.C. § 262** — absent agreement, each joint owner may make, use, offer to
   sell, sell or import "without the consent of and without accounting to the other
   owners." The **right to license** unilaterally is Federal Circuit gloss
   (*Schering v. Roussel-UCLAF*, 104 F.3d 341 (Fed. Cir. 1997)), not statutory text.
9. ***Ethicon v. U.S. Surgical*, 135 F.3d 1456 (Fed. Cir. 1998)** — all co-owners
   must ordinarily join as plaintiffs; a co-owner may impede suit by refusing.
   ***STC.UNM v. Intel*, 754 F.3d 940 (Fed. Cir. 2014)** — that right is substantive
   and defeats involuntary joinder under Rule 19(a).
10. **PRC Patent Law Art. 14** (2020 amendment, in force 1 June 2021; formerly
    Art. 15) — absent agreement, a co-owner may exploit alone **or grant a
    non-exclusive licence**, and royalties so received **must be distributed among
    the co-owners**. Anything else needs the consent of all.
11. **Korean Patent Act Art. 99(2)–(4)** — modelled on Japan's Art. 73: share
    transfer/pledge needs the consent of all; self-working is free absent agreement;
    exclusive (전용실시권) and non-exclusive (통상실시권) licences need the consent of
    all. **Art. 44** is the joint-application rule; breach is an invalidity ground.
12. **Germany / EPO** — Art. 74 EPC sends ownership to national law; Germany applies
    §§741 ff. BGB (Bruchteilsgemeinschaft). Self-use is free (BGH *Gummielastische
    Masse II*, X ZR 152/03); a **licence needs the consent of all co-owners**;
    a share may be transferred freely under §747 sent. 1 BGB.
13. **Civil Code prescription** — 改正民法附則10条4項: a claim that arose before
    1 April 2020 stays under the old **民法167条1項 ten-year objective** rule. A claim
    arising at the December 12, 2014 registration is therefore time-barred from
    December 12, 2024.
    **Two consequences for how the corpus must plead it.** (a) SDS must plead a
    *single claim accruing on registration*, quantified by reference to 2019–2024
    receipts — not an accounting for royalties received in those years, because
    each receipt would carry its own start date and none of it would be
    time-barred at all. Whitcomb says so expressly in her memo. (b) The
    November 12, 2024 letter is a **催告** under 旧民法153条 and gives SDS six
    months, to about May 12, 2025, to bring proceedings. Gamō must say so when he
    pleads 消滅時効 on February 10, 2025; a flat assertion that ten years have run
    is answerable in one line.
14. **Procedure** — national/regional phase: 30 months for JP, CN, US, BR; **31
    months for EP, KR, IN**; CN extendable to 32 with a surcharge. JP request for
    examination: **3 years from the filing date** (for a PCT case, the international
    filing date). JP response to a 拒絶理由通知: **3 months for applicants resident
    abroad**, extendable by 3. JP patent fees for years 1–3 due within 30 days of
    the 特許査定; annuities from year 4. **No annuities on pending applications in
    JP, KR or CN**; the EPO charges renewal fees from the third year and Germany
    from the third year on applications as well as patents. EPO opposition: **9
    months from the mention of grant**. Rule 71(3): four months, non-extendable, to
    pay the grant fee and file claim translations into the other two official
    languages. Unitary Patent and the UPC: **1 June 2023**. JP post-grant
    opposition 特許異議申立て: reintroduced **1 April 2015**, six months from
    publication of grant. SIPO → **CNIPA in 2018**; 专利复审委员会 → 复审和无效審理部
    on **1 April 2019**. KIPO became MOIP on **1 October 2025** (after this story
    ends). Korean office-action response period was **2 months** until 11 July 2025.
    JP patent numbers: 特許第5,617,402号 is right for December 2014
    (特許第5,500,000号 ≈ May 2014, 特許第5,800,000号 ≈ October 2015; 特許第6,000,000号
    is not reached until late September 2016).

---

## 9. House style

American English throughout the English text — Marsden is a US company with a US
house style, and its Munich, Yokohama, Seoul and Shanghai staff follow it when
writing English. Japanese messages use 敬語 appropriate to the relationship
(です・ます to counterparties, plainer register internally). Korean uses
합쇼체/해요체 as appropriate. German uses Sie. Chinese uses 您 to externals.
