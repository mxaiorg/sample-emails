# Cast and Trap Sheet — securities-regulation-distractors

**NEVER INGEST THIS FILE INTO THE CORPUS.** Authoring brief only.

The distractor file is ~155 hand-authored hard negatives whose only job is to be
wrong in a way that is expensive to detect. They surround the signal thread
`marchwood-0447.md`, whose story is summarised in §0.

---

## 0. What the signal says (do not contradict it, do not duplicate it)

The SEC's Philadelphia Regional Office examined **Marchwood Asset Management LLC**
(SEC File No. 801-64719) in 2011 under legacy examination number **2011-0447**.
Item 4 of the April 20, 2011 deficiency letter found that the firm's standing
authority to instruct client custodians to debit advisory fees was custody under
Rule 206(4)-2. On **June 2, 2011** the firm's CCO **Marguerite Vasseur-Kyle**
wrote to the staff accepting Item 4, moving 214 accounts to **Signal Peak Trust
Company**, discontinuing the practice firm-wide, and undertaking to apply the same
treatment to accounts acquired or onboarded in the future, **without an expiration
date**. The staff closed on June 28, 2011 with disposition **C-4 (closed on
registrant undertaking)**.

The 2016 **EXAMTRAC → SENTRY** migration did not carry pre-2014 correspondence, and
collapsed legacy code C-4 into **C-2 (closed, no further action)**. In 2024 the firm,
charged in **AP File No. 3-21987** over a 2019–2023 resumption, moved for summary
disposition on the basis that the 2011 examination closed with no findings. The
**electronic mail journal archive** — never migrated, destruction suspended agency-wide
since September 2011 — produced the June 2, 2011 undertaking and the **October 21,
2013** letter in which the firm voluntarily applied the undertaking to 61 accounts
acquired from **Hollis Grange Advisers, Inc.** The motion was withdrawn February 21,
2025 and the firm settled for **$2,150,000** on March 14, 2025.

**Nothing in the distractor file may be a correct answer to any demo query.**
Marchwood *Asset Management LLC* must never appear in the distractor file. The
other Marchwood-named firms (§2) may and should.

---

## 1. Format — reproduce exactly

```
**Email-1**
To: Display Name <local@domain>
From: Display Name <local@domain>
Cc: Display Name <local@domain>, Display Name <local@domain>
Subject: Realistic subject line
Date: April 20, 2011, 14:08
References: Email-3
Body:
Body text starts on the next line. Multiple paragraphs allowed.
```

Rules that fail the build if broken:

- `Date:` is exactly `Month DD, YYYY, HH:MM` — full month name, **zero-padded day**,
  24-hour clock.
- Hours between **07:00 and 19:00**. Never a weekend, never a US federal holiday.
- `References:` names **only lower-numbered emails inside your own batch**, and the
  referencing email must be dated on or after its parent. A reply must **not** reuse
  its parent's minute value. Thread starters have an empty `References:`.
- `**Email-N**` numbering is sequential from 1 **within your own batch**, no gaps.
  Numbering and ordering across batches is handled by the merge script — do not
  worry about it, and do not try to order your batch by date.
- Every `To:`/`From:`/`Cc:` address is `Display Name <local@domain>`. **A given
  display name must always use the same address and vice versa, everywhere.** Use
  the cast table in §2 verbatim; do not invent people who are not in it, and do not
  vary a person's spelling.
- American spelling throughout.
- No attachments. Do not emit `Attachment:` lines.
- Do not use the strings `Marchwood Asset Management`, `Signal Peak`,
  `Vasseur-Kyle` (except where §2 explicitly assigns her a later employer),
  `Hollis Grange Advisers, Inc.`, `Penhaligon`, `3-21987`, `Quillen and Marsh`,
  `Aperture Billing`, or `Ballentine Roe`.
- Era discipline: **OCIE** before December 2020, **Division of Examinations** after.
  No Form CRS or Regulation Best Interest before 2019, no Marketing Rule before 2021,
  no COVID/pandemic before 2020, no Microsoft Teams before 2017, no ChatGPT before 2023.

---

## 2. Cast — use these exact strings

### SEC — Philadelphia Regional Office (shared with the signal; this is the "right person, wrong matter" trap)

| Display name | Address | Role |
|---|---|---|
| Rosalind Achterberg | rosalind.achterberg@sec.gov | Branch Chief, IA/IC Examinations (to 2019) |
| Desmond Whitlatch | desmond.whitlatch@sec.gov | Senior Examiner (to 2015) |
| Priya Raghunathan | priya.raghunathan@sec.gov | Examiner (to 2017) |
| Nathaniel Okuma | nathaniel.okuma@sec.gov | Assistant Regional Director (to 2021) |
| Yolanda Bricenio | yolanda.bricenio@sec.gov | Branch Chief, Division of Examinations (2016–) |
| Camille Ostrowski | camille.ostrowski@sec.gov | Assistant Director, Enforcement |
| Terrence Aubuchon | terrence.aubuchon@sec.gov | Senior Counsel, Enforcement |
| Gretchen Sallenave | gretchen.sallenave@sec.gov | Associate General Counsel |
| Delphine Karrasch | delphine.karrasch@sec.gov | Paralegal Specialist, Enforcement |
| Han-Wei Loh | hanwei.loh@sec.gov | Records Officer |
| Marcus Ellenbogen | marcus.ellenbogen@sec.gov | Office of Information Technology |
| Colton Peavey | colton.peavey@sec.gov | Private Funds Unit |
| Elias Fontanet | elias.fontanet@sec.gov | FOIA Officer |
| Nadine Chalfont-Reyes | nadine.chalfont-reyes@sec.gov | Office of Market Intelligence |

### SEC — other offices (distractor-only)

| Display name | Address | Role |
|---|---|---|
| Garrett Nkemelu | garrett.nkemelu@sec.gov | Branch Chief, IA/IC Examinations, Denver Regional Office |
| Sylvia Brandtford | sylvia.brandtford@sec.gov | Senior Examiner, Denver Regional Office |
| Ronan Delacoeur | ronan.delacoeur@sec.gov | Branch Chief, Boston Regional Office |
| Aparna Vellanki | aparna.vellanki@sec.gov | Assistant Regional Director, Fort Worth Regional Office |
| Warrick Osunde | warrick.osunde@sec.gov | Senior Counsel, Enforcement, Philadelphia |
| Beatrix Follansbee | beatrix.follansbee@sec.gov | Examiner, Philadelphia |
| Tomasz Wiercinski | tomasz.wiercinski@sec.gov | Examiner, Philadelphia |
| Imelda Sarrazin | imelda.sarrazin@sec.gov | Branch Chief, Broker-Dealer Examinations, Chicago |
| Percival Rathbone | percival.rathbone@sec.gov | Records Management Specialist |
| Anneke Vogelsang | anneke.vogelsang@sec.gov | Assistant Director, Enforcement, New York |

### Registrants and counterparties

| Entity | People | Addresses |
|---|---|---|
| **Braxton-Ferrer Advisors LLC** (Denver, 801-66031) — Denver's exam 2011-0447 | Corinne Ferrer, CCO; Dale Braxton, Managing Principal | cferrer@braxtonferrer.com; dbraxton@braxtonferrer.com |
| **Vandergrift Rowe Investment Counsel** (Philadelphia, 801-63127) — exam 2011-0463, the near-miss twin | Estelle Vandergrift, CCO; Howard Rowe, Principal | evandergrift@vandergriftrowe.com; hrowe@vandergriftrowe.com |
| **Ellersby Kinnaird Advisors LLC** (Pittsburgh, 801-64402) — exam 2012-0288, the qualified twin | Sinead Kinnaird, CCO | skinnaird@ellersbykinnaird.com |
| **Corrigan Weld Asset Management LLC** (Philadelphia, 801-65780) — the inverted premise | Miriam Weld, CCO | mweld@corriganweld.com |
| **Ottoway Trask Advisers LLC** (Philadelphia, 801-70118) — the anti-precedent | Bartholomew Trask, Managing Member; Lucia Ottoway, CCO | btrask@ottowaytrask.com; lottoway@ottowaytrask.com |
| **Marchwood Capital Partners LP** (New York, 801-71204) — name collision, private funds | Devon Marchwood-Reyes, CFO | dreyes@marchwoodcap.com |
| **Marchwood Wealth Advisors, Inc.** (Cleveland, 801-69955) — name collision | Peter Halvorsen, CCO | phalvorsen@marchwoodwealth.com |
| **Marchwood Securities LLC** (Chicago, CRD 45118) — name collision, broker-dealer | Ingrid Sattler, CCO | isattler@marchwoodsec.com |
| **Marchwood Fiduciary Services LLC** (Wilmington, DE) — name collision, trust company | Roland Pike, General Counsel | rpike@marchwoodfiduciary.com |
| **Hollis Grange Municipal Advisors LLC** (Harrisburg) — name collision | Teodora Vasquez-Lindh, Principal | tvasquez@hollisgrangema.com |
| **Ashgrove Pincott Advisors** (Philadelphia, 801-64810) — exam 2011-0477 | Neville Pincott, CCO | npincott@ashgrovepincott.com |
| **Delamere Quill Asset Management** (Philadelphia, 801-63944) — exam 2011-0417 | Ottoline Quill, CCO | oquill@delamerequill.com |
| **Wexford Trelaine Capital Management** (Boston, 801-61225) — exam 2010-0447 | Fergus Trelaine, CCO | ftrelaine@wexfordtrelaine.com |
| **Salomé Ridge Advisers LLC** (Fort Worth, 801-67733) — exam 2012-0447 | Jacinta Salomé, CCO | jsalome@salomeridge.com |
| **Trentmoor Wickham Advisers** (Philadelphia, 801-62119) — exam 2011-0392 | Alicia Wickham, CCO | awickham@trentmoorwickham.com |
| **Fenwick Alder Capital LLC** (Philadelphia, 801-66914) — exam 2011-0501 | Gideon Alder, CCO | galder@fenwickalder.com |
| **Rosslyn Padgett Investment Counsel** (Philadelphia, 801-65310) — exam 2012-0118 | Cora Padgett, CCO | cpadgett@rosslynpadgett.com |
| **Everly Sound Advisors LLC** (Philadelphia, 801-72440) — where Marguerite Vasseur-Kyle went in 2017 | Marguerite Vasseur-Kyle, CCO | m.vasseurkyle@everlysound.com |
| **Thackston Meade & Partners LLP** — counsel to several registrants | Ruth Thackston | rthackston@thackstonmeade.com |
| **Norbury Halstead LLP** — counsel to several registrants | Julian Halstead | jhalstead@norburyhalstead.com |
| **Pemberton Ivey LLP** — independent public accountants (surprise examinations) | Aurelio Pemberton | apemberton@pembertonivey.com |
| **Cranleigh Trust Company** (qualified custodian) | Delia Marchetti | dmarchetti@cranleightrust.com |
| **Wexbury Fiduciary Trust** (qualified custodian) | Owen Kastelic | okastelic@wexburyft.com |

**Marguerite Vasseur-Kyle is the single most dangerous person in this file.** She
is the author of the signal's needle. In the distractor file she appears **only**
at `m.vasseurkyle@everlysound.com`, from 2017 onward, as CCO of Everly Sound
Advisors — a different firm, a different examination, a different finding. A
retrieval tool that scopes by person will surface her Everly Sound correspondence
and must not cite it as the Marchwood undertaking.

---

## 3. Trap classes and what each must contain

Every one of these must appear. The counts are targets, not quotas — hit them
within ±2.

| # | Trap class | Count | What it is |
|---|---|---|---|
| A | **Same examination number, wrong registrant** | 14 | Denver's **2011-0447** is an advertising and performance-presentation examination of Braxton-Ferrer Advisors LLC — notice, deficiency letter, response, closing letter, and 2024–25 traffic that cites "2011-0447" without an office. Also Boston's **2010-0447** (Wexford Trelaine) and Fort Worth's **2012-0447** (Salomé Ridge). |
| B | **Transposed near-misses** | 10 | Philadelphia's **2011-0477** (Ashgrove Pincott) and **2011-0417** (Delamere Quill). At least two emails must contain a genuine human transposition — someone writes 0447 when they mean 0477 and is corrected. |
| C | **Name collisions** | 18 | Marchwood Capital Partners LP, Marchwood Wealth Advisors Inc., Marchwood Securities LLC, Marchwood Fiduciary Services LLC, Hollis Grange Municipal Advisors LLC. Ordinary regulatory traffic — filings, delinquencies, exam notices, a broker-dealer sweep. At least three must be dated 2024–2025 so they compete with the present-day era. |
| D | **Right person, wrong matter** | 14 | Achterberg issuing deficiency and closing letters on 2011-0392 (Trentmoor Wickham), 2011-0501 (Fenwick Alder) and 2012-0118 (Rosslyn Padgett); Whitlatch as examiner in charge elsewhere; Vasseur-Kyle at **Everly Sound Advisors** from 2017 writing to the staff about a *books-and-records* finding — same voice, same register, wrong firm, wrong subject. |
| E | **The near-miss twin** | 12 | **Vandergrift Rowe Investment Counsel**, examination **2011-0463**, Philadelphia, same branch chief, same examiner, fieldwork three weeks after Marchwood's. Same custody finding at **Item 4**. Its undertaking letter is dated **May 31, 2011** — two days before the signal's — and is worded almost identically. This is the closest look-alike in the corpus. |
| F | **The qualified twin (the answer inverts)** | 10 | Vandergrift Rowe's undertaking is **expressly limited to calendar years 2011 and 2012** and lapsed by its terms on December 31, 2012. In 2023 the firm resumed the practice; the Division reviewed the same archive, found the same kind of letter, and **declined to charge** the post-2013 conduct because the undertaking had expired. Separately, **Ellersby Kinnaird Advisors** gave an undertaking limited to "the accounts identified in Schedule A," so accounts acquired later fall outside it. Anyone who reads the headline and stops gets the opposite answer. |
| G | **The inverted premise** | 10 | **Corrigan Weld Asset Management** never held fee-debit authority at all — it billed by invoice throughout. Its custody exposure arose solely because an affiliate is a qualified custodian, which it cured with an internal control report. Nothing was ever undertaken because nothing was ever required. Merged with the signal it produces a corroborated wrong answer about what Rule 206(4)-2 requires. |
| H | **The anti-precedent** | 12 | **Ottoway Trask Advisers LLC**, 2024–2025. The Division asserted in an OIP that a 2012 examination had produced a written undertaking lost in the 2016 migration. The journal archive was searched on the same theory and with the same tooling, and **found nothing**, because no undertaking was ever obtained. The Division withdrew the allegation and dropped the count. Same story, opposite outcome — this is what proves a tool is reading evidence rather than pattern-matching. |
| I | **Adjacent-date collisions** | 8 | Deficiency letters issued April 19 and April 21, 2011 by the same branch chief to other registrants. Administrative proceedings instituted the same week as the signal's — **AP File No. 3-21985** and **3-21991** — one of them also involving custody. |
| J | **Same finding number, wrong matter — "Item 4"** | 16 | Sixteen deficiency letters whose **Item 4** is about something else: best execution, proxy voting, business continuity, advertising, principal transactions, wrap-fee disclosure, valuation, solicitor arrangements, cybersecurity, electronic communications. Spread these across registrants and years. Each must say "Item 4" explicitly. |
| K | **Custody traffic that is not the needle** | 12 | Other advisers' surprise examinations, Form ADV-E filings, internal control reports, qualified custodian changes, Item 9 amendments. Ordinary and correct. |
| L | **Migration-gap claims on other matters** | 10 | Other matters where "we cannot find the pre-2014 file" came up and was resolved some other way — a restore from EXAMTRAC, a registrant's own copy, a FINRA file, or simply an accepted gap. At least two must state the C-4/C-2 mapping problem in a *different* matter, so the mapping story is not unique to the signal. |
| M | **EAJA applications elsewhere** | 9 | Other respondents applying for fees under the Equal Access to Justice Act — one granted in part, one denied, one withdrawn for unrelated reasons. |

---

## 4. Voice

These are working emails inside a federal agency and between a regulator and its
registrants. Short paragraphs. Institutional register, not corporate cheer. Staff
write to each other bluntly and to registrants formally. Registrants and their
counsel are polite and careful. Nobody explains the story to the reader.

Vary length: some are three lines, some are five paragraphs. Repeat nothing.
