# Five-Year Financials for Five More Companies from SEC Filing Data

**FINAL — ready to submit.** Built from all three pulls. PULL 3 ran
19 Nov 2026 11:40 WIB (cron `synmerco-pull3-sec-fin`) and is byte-identical
to PULL 1 and PULL 2 (same SHA-256, 150 rows). Every table below is taken
from the last good pull (PULL 3), which is byte-identical to PULL 2 and PULL 1.

## Job

- Escrow: `esc_2bc2a980f676400ab29632a7` (funded 2026-11-17T04:15:19.858Z)
- Bid: $1.50 on a $12.00 budget; platform fee $0.04; net to seller $1.46 USDC
- Buyer: `did:pkh:eip155:8453:0x1bCEB0c42998B6E6Bc00a644Ec560869e15198Ab`
- Seller (Lord): `did:pkh:eip155:8453:0x97E5011A3F51dD1A126a2753D8A45C97d4b426af`
- Earliest submit: 2026-11-19T04:15:07Z; deliver by: 2026-11-21T12:15:07Z
- Source: data.sec.gov only (submissions endpoint + companyconcept endpoint),
  User-Agent header with contact shown throughout as `[redacted]`, max 10 req/s.
- Deliverables: D1 this report; D2 `sec-fin-five-more-pull1.csv`;
  D3 `sec-fin-five-more-pull2.csv`; D4 `sec-fin-five-more-pull3.csv`
  (attached as data files under Rule 25).

## Method (as specified)

For each company, the five latest 10-K filings (by filingDate) from the
submissions endpoint; each 10-K = one fiscal year, period end = reportDate,
10-K accession = accessionNumber. Original value = the companyconcept entry
whose accn = that 10-K accession and end = period end (for revenue, net income
and operating cash flow: the longest period ending there). Tags: revenue = first of
RevenueFromContractWithCustomerExcludingAssessedTax, Revenues, SalesRevenueNet,
RevenueFromContractWithCustomerIncludingAssessedTax that has that entry;
net income = NetIncomeLoss; total assets = Assets; total liabilities = Liabilities,
else derived = LiabilitiesAndStockholdersEquity − StockholdersEquity (tag "derived";
only when both exist; latest accession/filed from the later-filed of the two);
stockholders equity = StockholdersEquity; operating cash flow =
NetCashProvidedByUsedInOperatingActivities. Latest value = entry of the same tag,
same start (none for balance-sheet tags) and end, form 10-K or 10-K/A filed last
(ties: higher accn). A restatement is a row where both values exist and differ.
An unreported tag has no entry — that is not a failure. Values are in USD as
reported by the source. Ratios are computed from the ORIGINAL values, 2 decimals,
half-up; missing input or a zero divisor gives "not available".

## Per-company tables (original values, from the last good pull — PULL 3, byte-identical to PULL 2)

Each table lists, per fiscal year, the six original values plus net margin
(net income / revenue) and liabilities-to-equity (total liabilities /
stockholders equity). All six values and both ratios are traceable to the
matching row of the attached CSVs (key = CIK | metric | period end).

### Sherwin-Williams (CIK 89800, SHERWIN WILLIAMS CO)

| Fiscal year | Period end | 10-K accession | Revenue | Net income | Total assets | Total liabilities | Stockholders equity | Operating cash flow | Net margin | Liabilities-to-equity |
|---|---|---|---|---|---|---|---|---|---|---|
| FY2021 | 2021-12-31 | 0000089800-22-000007 | 19,944,600,000 | 1,864,400,000 | 20,666,700,000 | 18,229,500,000 | 2,437,200,000 | 2,244,600,000 | 9.35% | 7.48 |
| FY2022 | 2022-12-31 | 0000089800-23-000007 | 22,148,900,000 | 2,020,100,000 | 22,594,000,000 | 19,491,900,000 | 3,102,100,000 | 1,919,900,000 | 9.12% | 6.28 |
| FY2023 | 2023-12-31 | 0000089800-24-000033 | 23,051,900,000 | 2,388,800,000 | 22,954,400,000 | 19,238,600,000 | 3,715,800,000 | 3,521,900,000 | 10.36% | 5.18 |
| FY2024 | 2024-12-31 | 0000089800-25-000030 | 23,098,500,000 | 2,681,400,000 | 23,632,600,000 | 19,581,400,000 | 4,051,200,000 | 3,153,200,000 | 11.61% | 4.83 |
| FY2025 | 2025-12-31 | 0000089800-26-000008 | 23,574,300,000 | 2,568,500,000 | 25,901,700,000 | 21,303,400,000 | 4,598,300,000 | 3,451,600,000 | 10.90% | 4.63 |

- FY2021 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2022 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2023 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2024 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2025 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.

### Cintas (CIK 723254, CINTAS CORP)

| Fiscal year | Period end | 10-K accession | Revenue | Net income | Total assets | Total liabilities | Stockholders equity | Operating cash flow | Net margin | Liabilities-to-equity |
|---|---|---|---|---|---|---|---|---|---|---|
| FY2022 | 2022-05-31 | 0000723254-22-000019 | 7,854,459,000 | 1,235,757,000 | 8,147,256,000 | 4,839,060,000 | 3,308,196,000 | 1,537,625,000 | 15.73% | 1.46 |
| FY2023 | 2023-05-31 | 0000723254-23-000025 | 8,815,769,000 | 1,348,010,000 | 8,546,356,000 | 4,682,370,000 | 3,863,986,000 | 1,597,814,000 | 15.29% | 1.21 |
| FY2024 | 2024-05-31 | 0000723254-24-000036 | 9,596,615,000 | 1,571,592,000 | 9,168,817,000 | 4,852,445,000 | 4,316,372,000 | 2,079,781,000 | 16.38% | 1.12 |
| FY2025 | 2025-05-31 | 0000723254-25-000017 | 10,340,181,000 | 1,812,281,000 | 9,825,241,000 | 5,140,760,000 | 4,684,481,000 | 2,165,905,000 | 17.53% | 1.10 |
| FY2026 | 2026-05-31 | 0000723254-26-000028 | 11,264,761,000 | 1,999,968,000 | 10,529,140,000 | 5,389,253,000 | 5,139,887,000 | 2,276,280,000 | 17.75% | 1.05 |

- FY2022 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2023 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2024 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2025 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.
- FY2026 total liabilities is derived (LiabilitiesAndStockholdersEquity − StockholdersEquity); the company does not report a Liabilities tag.

### Lennar (CIK 920760, LENNAR CORP /NEW/)

| Fiscal year | Period end | 10-K accession | Revenue | Net income | Total assets | Total liabilities | Stockholders equity | Operating cash flow | Net margin | Liabilities-to-equity |
|---|---|---|---|---|---|---|---|---|---|---|
| FY2021 | 2021-11-30 | 0001628280-22-001450 | 27,130,676,000 | 4,430,111,000 | 33,207,778,000 | 12,211,496,000 | 20,816,425,000 | 2,532,774,000 | 16.33% | 0.59 |
| FY2022 | 2022-11-30 | 0001628280-23-001606 | not available | 4,614,125,000 | 37,984,295,000 | 13,743,928,000 | 24,100,500,000 | 3,265,668,000 | not available | 0.57 |
| FY2023 | 2023-11-30 | 0001628280-24-002371 | 34,233,366,000 | 3,938,511,000 | 39,234,303,000 | 12,532,337,000 | 26,580,664,000 | 5,179,738,000 | 11.50% | 0.47 |
| FY2024 | 2024-11-30 | 0001628280-25-002404 | 35,441,452,000 | 3,932,533,000 | 41,312,781,000 | 13,291,556,000 | 27,870,135,000 | 2,403,379,000 | 11.10% | 0.48 |
| FY2025 | 2025-11-30 | 0001628280-26-003870 | 34,186,934,000 | 2,078,179,000 | 34,430,437,000 | 12,289,828,000 | 21,959,417,000 | 216,812,000 | 6.08% | 0.56 |

- FY2022 revenue: original value not available — the original 10-K never reported Revenues for that period end; latest value 33,671,010,000 comes from 0001628280-25-002404 (filed 2025-01-23).

### Tractor Supply (CIK 916365, TRACTOR SUPPLY CO /DE/)

| Fiscal year | Period end | 10-K accession | Revenue | Net income | Total assets | Total liabilities | Stockholders equity | Operating cash flow | Net margin | Liabilities-to-equity |
|---|---|---|---|---|---|---|---|---|---|---|
| FY2021 | 2021-12-25 | 0000916365-22-000049 | 12,731,105,000 | 997,114,000 | 7,767,467,000 | 5,764,802,000 | 2,002,665,000 | 1,138,720,000 | 7.83% | 2.88 |
| FY2022 | 2022-12-31 | 0000916365-23-000045 | 14,204,717,000 | 1,088,712,000 | 8,489,990,000 | 6,447,574,000 | 2,042,416,000 | 1,356,979,000 | 7.66% | 3.16 |
| FY2023 | 2023-12-30 | 0000916365-24-000046 | 14,555,741,000 | 1,107,226,000 | 9,188,151,000 | 7,038,389,000 | 2,149,762,000 | 1,334,033,000 | 7.61% | 3.27 |
| FY2024 | 2024-12-28 | 0000916365-25-000076 | 14,883,231,000 | 1,101,240,000 | 9,805,485,000 | 7,535,151,000 | 2,270,334,000 | 1,420,835,000 | 7.40% | 3.32 |
| FY2025 | 2025-12-27 | 0000916365-26-000014 | 15,524,046,000 | 1,096,087,000 | 10,933,679,000 | 8,352,386,000 | 2,581,293,000 | 1,635,259,000 | 7.06% | 3.24 |

### Paychex (CIK 723531, PAYCHEX INC)

| Fiscal year | Period end | 10-K accession | Revenue | Net income | Total assets | Total liabilities | Stockholders equity | Operating cash flow | Net margin | Liabilities-to-equity |
|---|---|---|---|---|---|---|---|---|---|---|
| FY2022 | 2022-05-31 | 0000950170-22-012734 | 4,554,000,000 | not available | 9,635,200,000 | 6,550,000,000 | 3,085,200,000 | 1,505,500,000 | not available | 2.12 |
| FY2023 | 2023-05-31 | 0000950170-23-032988 | 4,907,300,000 | not available | 10,546,400,000 | 7,053,200,000 | 3,493,200,000 | 1,699,400,000 | not available | 2.02 |
| FY2024 | 2024-05-31 | 0000950170-24-082958 | 5,132,000,000 | not available | 10,383,100,000 | 6,582,100,000 | 3,801,000,000 | 1,897,700,000 | not available | 1.73 |
| FY2025 | 2025-05-31 | 0000950170-25-095300 | 5,410,000,000 | not available | 16,564,100,000 | 12,436,100,000 | 4,128,000,000 | 1,900,900,000 | not available | 3.01 |
| FY2026 | 2026-05-31 | 0001193125-26-307785 | 6,301,100,000 | 1,760,100,000 | 16,174,500,000 | 12,439,400,000 | 3,735,100,000 | 2,556,700,000 | 27.93% | 3.33 |

- FY2022 net income: not available in the original 10-K and in no later 10-K/10-K/A either — the tag was never reported for that period end.
- FY2023 net income: not available in the original 10-K and in no later 10-K/10-K/A either — the tag was never reported for that period end.
- FY2024 net income: original value not available — the original 10-K never reported NetIncomeLoss for that period end; latest value 1,690,400,000 comes from 0001193125-26-307785 (filed 2026-07-17).
- FY2025 net income: original value not available — the original 10-K never reported NetIncomeLoss for that period end; latest value 1,657,300,000 comes from 0001193125-26-307785 (filed 2026-07-17).

## Restatements (all pulls so far)

A restatement is a row where the original value and the latest value both exist
and differ. Verified from the CSVs (PULL 1, PULL 2 and PULL 3 are byte-identical):

| Company | Metric | Period end | Original value | Latest value | Latest accession | Latest filed |
|---|---|---|---|---|---|---|
| CINTAS CORP | operating cash flow | 2023-05-31 | 1,597,814,000 | 1,586,228,000 | 0000723254-25-000017 | 2025-07-28 |
| CINTAS CORP | operating cash flow | 2024-05-31 | 2,079,781,000 | 2,068,500,000 | 0000723254-26-000028 | 2026-07-29 |
| PAYCHEX INC | operating cash flow | 2022-05-31 | 1,505,500,000 | 1,589,700,000 | 0000950170-24-082958 | 2024-07-11 |
| PAYCHEX INC | operating cash flow | 2023-05-31 | 1,699,400,000 | 1,706,200,000 | 0000950170-25-095300 | 2025-07-11 |

Total restatements: 4 — all four are operating cash flow.
No other metric for any company restated between its original 10-K and the
latest 10-K/10-K/A filing for the same period end.

PULL 3 added no new restatements (total still 4). Re-checked on
`sec-fin-five-more-pull3.csv` after the 19 Nov 11:40 WIB pull: the file is
byte-identical to PULL 2, so the same four operating-cash-flow restatements
(Cintas FY2023/FY2024, Paychex FY2022/FY2023) stand.

## Per-pull filings counts and new filings

Filings count = `filings_count_recent` from the submissions endpoint for each
company at pull time. New accessions = accessionNumbers present in the later
pull's submissions data that were not present in the earlier pull's.

### PULL 1 — pulled 2026-11-17T04:29:54Z

| Company | CIK | Filings count (recent) | 10-K accessions used (5 latest) |
|---|---|---|---|
| Sherwin-Williams | 89800 | 1004 | 0000089800-26-000008, 0000089800-25-000030, 0000089800-24-000033, 0000089800-23-000007, 0000089800-22-000007 |
| Cintas | 723254 | 1000 | 0000723254-26-000028, 0000723254-25-000017, 0000723254-24-000036, 0000723254-23-000025, 0000723254-22-000019 |
| Lennar | 920760 | 1002 | 0001628280-26-003870, 0001628280-25-002404, 0001628280-24-002371, 0001628280-23-001606, 0001628280-22-001450 |
| Tractor Supply | 916365 | 1001 | 0000916365-26-000014, 0000916365-25-000076, 0000916365-24-000046, 0000916365-23-000045, 0000916365-22-000049 |
| Paychex | 723531 | 1004 | 0001193125-26-307785, 0000950170-25-095300, 0000950170-24-082958, 0000950170-23-032988, 0000950170-22-012734 |

### PULL 2 — pulled 2026-11-18T04:36:13Z

| Company | CIK | Filings count (recent) | 10-K accessions used (5 latest) |
|---|---|---|---|
| Sherwin-Williams | 89800 | 1004 | 0000089800-26-000008, 0000089800-25-000030, 0000089800-24-000033, 0000089800-23-000007, 0000089800-22-000007 |
| Cintas | 723254 | 1000 | 0000723254-26-000028, 0000723254-25-000017, 0000723254-24-000036, 0000723254-23-000025, 0000723254-22-000019 |
| Lennar | 920760 | 1002 | 0001628280-26-003870, 0001628280-25-002404, 0001628280-24-002371, 0001628280-23-001606, 0001628280-22-001450 |
| Tractor Supply | 916365 | 1001 | 0000916365-26-000014, 0000916365-25-000076, 0000916365-24-000046, 0000916365-23-000045, 0000916365-22-000049 |
| Paychex | 723531 | 1004 | 0001193125-26-307785, 0000950170-25-095300, 0000950170-24-082958, 0000950170-23-032988, 0000950170-22-012734 |

New accessionNumbers since PULL 1: none for any company
(`new_accessions_since_pull1` is empty for all five CIKs in `pull2-meta.json`).
Filings counts are unchanged from PULL 1 (1004 / 1000 / 1002 / 1001 / 1004).

### PULL 3 — pulled 2026-11-19T04:41:32Z

| Company | CIK | Filings count (recent) | 10-K accessions used (5 latest) |
|---|---|---|---|
| Sherwin-Williams | 89800 | 1004 | 0000089800-26-000008, 0000089800-25-000030, 0000089800-24-000033, 0000089800-23-000007, 0000089800-22-000007 |
| Cintas | 723254 | 1000 | 0000723254-26-000028, 0000723254-25-000017, 0000723254-24-000036, 0000723254-23-000025, 0000723254-22-000019 |
| Lennar | 920760 | 1000 | 0001628280-26-003870, 0001628280-25-002404, 0001628280-24-002371, 0001628280-23-001606, 0001628280-22-001450 |
| Tractor Supply | 916365 | 1001 | 0000916365-26-000014, 0000916365-25-000076, 0000916365-24-000046, 0000916365-23-000045, 0000916365-22-000049 |
| Paychex | 723531 | 1004 | 0001193125-26-307785, 0000950170-25-095300, 0000950170-24-082958, 0000950170-23-032988, 0000950170-22-012734 |

New accessionNumbers since PULL 2: none for any company (verified by comparing
the accessionNumber sets in `raw3/submissions-*.json` against `raw2/` — no new
accession in any company's recent list).

Filings counts are unchanged from PULL 2 except Lennar: 1002 → 1000. The two
accessions that left Lennar's recent list (`0001209191-15-068873` and
`0001209191-15-068875`, both 2015 filings) aged out of the SEC's recent-1000
window; they are not 10-Ks used by this job and no new filing replaced them.
The five 10-K accessions used are unchanged for every company, and the PULL 3
CSV is byte-identical to PULL 2.

## Changes

Each Changes section compares the two CSVs row by row, keyed by
`key` (CIK | metric | period end). Counts: new = keys only in the later pull,
gone = keys only in the earlier pull, changed = keys in both pulls whose row
differs in any column. The identity later = earlier + new − gone must hold,
or the section says "no change".

### Changes: PULL 2 vs PULL 1

- PULL 1 rows: 150 (150 data rows + header)
- PULL 2 rows: 150 (150 data rows + header)
- New keys: 0; gone keys: 0; changed rows: 0
- Check: 150 = 150 + 0 − 0 ✓
- SHA-256 PULL 1: `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d`
- SHA-256 PULL 2: `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d`
- **No change.** PULL 2 is byte-identical to PULL 1: same 150 rows, same
  SHA-256, no new, gone or changed rows, no new filings, no new restatements.

### Changes: PULL 3 vs PULL 2

- PULL 2 rows: 150 (150 data rows + header)
- PULL 3 rows: 150 (150 data rows + header)
- New keys: 0; gone keys: 0; changed rows: 0
- Check: 150 = 150 + 0 − 0 ✓
- SHA-256 PULL 2: `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d`
- SHA-256 PULL 3: `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d`
- **No change.** PULL 3 is byte-identical to PULL 2: same 150 rows, same
  SHA-256, no new, gone or changed rows, no new filings, no new restatements.

## PROOF

User-Agent sent on every request: `[redacted]` (contact redacted).
All times UTC. HTTP Date is the `Date` header returned by data.sec.gov for that
request; a blank HTTP Date means the request failed (HTTP 404 on a tag the
company never reported — expected, not an error — or a transport error).
The 404s are all on the `Liabilities` tag for Sherwin-Williams and Cintas,
which do not report it; their total liabilities are derived instead (see Method).

### HTTP Date headers per pull (first request of each pull)

- PULL 1 first request (submissions, CIK 89800): `Tue, 17 Nov 2026 04:29:57 GMT`
- PULL 2 first request (submissions, CIK 89800): `Wed, 18 Nov 2026 04:36:15 GMT`
- PULL 3 first request (submissions, CIK 89800): `Thu, 19 Nov 2026 04:41:34 GMT`
- PULL 3 first requests per company: CIK 89800 `Thu, 19 Nov 2026 04:41:34 GMT`;
  CIK 723254 `Thu, 19 Nov 2026 04:41:46 GMT`; CIK 920760
  `Thu, 19 Nov 2026 04:42:00 GMT`; CIK 916365 `Thu, 19 Nov 2026 04:42:21 GMT`;
  CIK 723531 `Thu, 19 Nov 2026 04:42:32 GMT`

### Requests — PULL 1 (47 requests, 2026-11-17T04:29:54Z–04:30:50Z)

| # | UTC time | URL | Status | HTTP Date |
|---|---|---|---|---|
| 1 | 2026-11-17T04:29:56Z | https://data.sec.gov/submissions/CIK0000089800.json | 200 | Tue, 17 Nov 2026 04:29:57 GMT |
| 2 | 2026-11-17T04:29:58Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Tue, 17 Nov 2026 04:29:59 GMT |
| 3 | 2026-11-17T04:30:00Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/NetIncomeLoss.json | 200 | Tue, 17 Nov 2026 04:30:00 GMT |
| 4 | 2026-11-17T04:30:02Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Assets.json | 200 | Tue, 17 Nov 2026 04:30:02 GMT |
| 5 | 2026-11-17T04:30:03Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 6 | 2026-11-17T04:30:05Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 7 | 2026-11-17T04:30:08Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/LiabilitiesAndStockholdersEquity.json | 200 | Tue, 17 Nov 2026 04:30:09 GMT |
| 8 | 2026-11-17T04:30:10Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/StockholdersEquity.json | 200 | Tue, 17 Nov 2026 04:30:10 GMT |
| 9 | 2026-11-17T04:30:12Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Tue, 17 Nov 2026 04:30:13 GMT |
| 10 | 2026-11-17T04:30:14Z | https://data.sec.gov/submissions/CIK0000723254.json | 200 | Tue, 17 Nov 2026 04:30:14 GMT |
| 11 | 2026-11-17T04:30:16Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Tue, 17 Nov 2026 04:30:16 GMT |
| 12 | 2026-11-17T04:30:17Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/NetIncomeLoss.json | 200 | Tue, 17 Nov 2026 04:30:17 GMT |
| 13 | 2026-11-17T04:30:17Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Assets.json | 200 | Tue, 17 Nov 2026 04:30:18 GMT |
| 14 | 2026-11-17T04:30:18Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 15 | 2026-11-17T04:30:20Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 16 | 2026-11-17T04:30:22Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/LiabilitiesAndStockholdersEquity.json | 200 | Tue, 17 Nov 2026 04:30:22 GMT |
| 17 | 2026-11-17T04:30:23Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/StockholdersEquity.json | 200 | Tue, 17 Nov 2026 04:30:23 GMT |
| 18 | 2026-11-17T04:30:24Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Tue, 17 Nov 2026 04:30:25 GMT |
| 19 | 2026-11-17T04:30:25Z | https://data.sec.gov/submissions/CIK0000920760.json | 200 | Tue, 17 Nov 2026 04:30:25 GMT |
| 20 | 2026-11-17T04:30:25Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 21 | 2026-11-17T04:30:27Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 22 | 2026-11-17T04:30:29Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Revenues.json | 200 | Tue, 17 Nov 2026 04:30:30 GMT |
| 23 | 2026-11-17T04:30:30Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/NetIncomeLoss.json | 200 | Tue, 17 Nov 2026 04:30:30 GMT |
| 24 | 2026-11-17T04:30:31Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Assets.json | 200 | Tue, 17 Nov 2026 04:30:31 GMT |
| 25 | 2026-11-17T04:30:31Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Liabilities.json | 200 | Tue, 17 Nov 2026 04:30:32 GMT |
| 26 | 2026-11-17T04:30:32Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/StockholdersEquity.json | 200 | Tue, 17 Nov 2026 04:30:33 GMT |
| 27 | 2026-11-17T04:30:33Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Tue, 17 Nov 2026 04:30:34 GMT |
| 28 | 2026-11-17T04:30:34Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/SalesRevenueNet.json | error: HTTP Error 404: Not Found |  |
| 29 | 2026-11-17T04:30:35Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/SalesRevenueNet.json | error: HTTP Error 404: Not Found |  |
| 30 | 2026-11-17T04:30:37Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerIncludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 31 | 2026-11-17T04:30:39Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerIncludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 32 | 2026-11-17T04:30:41Z | https://data.sec.gov/submissions/CIK0000916365.json | 200 | Tue, 17 Nov 2026 04:30:41 GMT |
| 33 | 2026-11-17T04:30:41Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 34 | 2026-11-17T04:30:43Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 35 | 2026-11-17T04:30:44Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Revenues.json | 200 | Tue, 17 Nov 2026 04:30:45 GMT |
| 36 | 2026-11-17T04:30:45Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/NetIncomeLoss.json | 200 | Tue, 17 Nov 2026 04:30:46 GMT |
| 37 | 2026-11-17T04:30:46Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Assets.json | 200 | Tue, 17 Nov 2026 04:30:47 GMT |
| 38 | 2026-11-17T04:30:47Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Liabilities.json | 200 | Tue, 17 Nov 2026 04:30:48 GMT |
| 39 | 2026-11-17T04:30:48Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/StockholdersEquity.json | 200 | Tue, 17 Nov 2026 04:30:49 GMT |
| 40 | 2026-11-17T04:30:49Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Tue, 17 Nov 2026 04:30:50 GMT |
| 41 | 2026-11-17T04:30:50Z | https://data.sec.gov/submissions/CIK0000723531.json | 200 | Tue, 17 Nov 2026 04:30:50 GMT |
| 42 | 2026-11-17T04:30:50Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Tue, 17 Nov 2026 04:30:51 GMT |
| 43 | 2026-11-17T04:30:51Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/NetIncomeLoss.json | 200 | Tue, 17 Nov 2026 04:30:52 GMT |
| 44 | 2026-11-17T04:30:52Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/Assets.json | 200 | Tue, 17 Nov 2026 04:30:53 GMT |
| 45 | 2026-11-17T04:30:53Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/Liabilities.json | 200 | Tue, 17 Nov 2026 04:30:54 GMT |
| 46 | 2026-11-17T04:30:54Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/StockholdersEquity.json | 200 | Tue, 17 Nov 2026 04:30:55 GMT |
| 47 | 2026-11-17T04:30:55Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Tue, 17 Nov 2026 04:30:56 GMT |

### Requests — PULL 2 (47 requests, 2026-11-18T04:36:13Z–04:37:09Z)

| # | UTC time | URL | Status | HTTP Date |
|---|---|---|---|---|
| 1 | 2026-11-18T04:36:14Z | https://data.sec.gov/submissions/CIK0000089800.json | 200 | Wed, 18 Nov 2026 04:36:15 GMT |
| 2 | 2026-11-18T04:36:15Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Wed, 18 Nov 2026 04:36:16 GMT |
| 3 | 2026-11-18T04:36:17Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/NetIncomeLoss.json | 200 | Wed, 18 Nov 2026 04:36:18 GMT |
| 4 | 2026-11-18T04:36:18Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Assets.json | 200 | Wed, 18 Nov 2026 04:36:19 GMT |
| 5 | 2026-11-18T04:36:19Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 6 | 2026-11-18T04:36:21Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 7 | 2026-11-18T04:36:22Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/LiabilitiesAndStockholdersEquity.json | 200 | Wed, 18 Nov 2026 04:36:23 GMT |
| 8 | 2026-11-18T04:36:24Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/StockholdersEquity.json | 200 | Wed, 18 Nov 2026 04:36:25 GMT |
| 9 | 2026-11-18T04:36:25Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Wed, 18 Nov 2026 04:36:26 GMT |
| 10 | 2026-11-18T04:36:26Z | https://data.sec.gov/submissions/CIK0000723254.json | 200 | Wed, 18 Nov 2026 04:36:27 GMT |
| 11 | 2026-11-18T04:36:28Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Wed, 18 Nov 2026 04:36:29 GMT |
| 12 | 2026-11-18T04:36:28Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/NetIncomeLoss.json | 200 | Wed, 18 Nov 2026 04:36:30 GMT |
| 13 | 2026-11-18T04:36:30Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Assets.json | 200 | Wed, 18 Nov 2026 04:36:31 GMT |
| 14 | 2026-11-18T04:36:31Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 15 | 2026-11-18T04:36:33Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 16 | 2026-11-18T04:36:35Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/LiabilitiesAndStockholdersEquity.json | 200 | Wed, 18 Nov 2026 04:36:36 GMT |
| 17 | 2026-11-18T04:36:36Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/StockholdersEquity.json | 200 | Wed, 18 Nov 2026 04:36:37 GMT |
| 18 | 2026-11-18T04:36:37Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Wed, 18 Nov 2026 04:36:38 GMT |
| 19 | 2026-11-18T04:36:38Z | https://data.sec.gov/submissions/CIK0000920760.json | 200 | Wed, 18 Nov 2026 04:36:39 GMT |
| 20 | 2026-11-18T04:36:38Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 21 | 2026-11-18T04:36:40Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 22 | 2026-11-18T04:36:42Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Revenues.json | 200 | Wed, 18 Nov 2026 04:36:43 GMT |
| 23 | 2026-11-18T04:36:44Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/NetIncomeLoss.json | 200 | Wed, 18 Nov 2026 04:36:45 GMT |
| 24 | 2026-11-18T04:36:45Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Assets.json | 200 | Wed, 18 Nov 2026 04:36:46 GMT |
| 25 | 2026-11-18T04:36:47Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Liabilities.json | 200 | Wed, 18 Nov 2026 04:36:48 GMT |
| 26 | 2026-11-18T04:36:48Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/StockholdersEquity.json | 200 | Wed, 18 Nov 2026 04:36:49 GMT |
| 27 | 2026-11-18T04:36:49Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Wed, 18 Nov 2026 04:36:50 GMT |
| 28 | 2026-11-18T04:36:50Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/SalesRevenueNet.json | error: HTTP Error 404: Not Found |  |
| 29 | 2026-11-18T04:36:51Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/SalesRevenueNet.json | error: HTTP Error 404: Not Found |  |
| 30 | 2026-11-18T04:36:53Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerIncludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 31 | 2026-11-18T04:36:55Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerIncludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 32 | 2026-11-18T04:36:57Z | https://data.sec.gov/submissions/CIK0000916365.json | 200 | Wed, 18 Nov 2026 04:36:58 GMT |
| 33 | 2026-11-18T04:36:58Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 34 | 2026-11-18T04:36:59Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 35 | 2026-11-18T04:37:01Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Revenues.json | 200 | Wed, 18 Nov 2026 04:37:02 GMT |
| 36 | 2026-11-18T04:37:02Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/NetIncomeLoss.json | 200 | Wed, 18 Nov 2026 04:37:03 GMT |
| 37 | 2026-11-18T04:37:04Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Assets.json | 200 | Wed, 18 Nov 2026 04:37:05 GMT |
| 38 | 2026-11-18T04:37:05Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Liabilities.json | 200 | Wed, 18 Nov 2026 04:37:06 GMT |
| 39 | 2026-11-18T04:37:06Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/StockholdersEquity.json | 200 | Wed, 18 Nov 2026 04:37:07 GMT |
| 40 | 2026-11-18T04:37:07Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Wed, 18 Nov 2026 04:37:08 GMT |
| 41 | 2026-11-18T04:37:08Z | https://data.sec.gov/submissions/CIK0000723531.json | 200 | Wed, 18 Nov 2026 04:37:09 GMT |
| 42 | 2026-11-18T04:37:09Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Wed, 18 Nov 2026 04:37:10 GMT |
| 43 | 2026-11-18T04:37:10Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/NetIncomeLoss.json | 200 | Wed, 18 Nov 2026 04:37:11 GMT |
| 44 | 2026-11-18T04:37:11Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/Assets.json | 200 | Wed, 18 Nov 2026 04:37:12 GMT |
| 45 | 2026-11-18T04:37:13Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/Liabilities.json | 200 | Wed, 18 Nov 2026 04:37:14 GMT |
| 46 | 2026-11-18T04:37:14Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/StockholdersEquity.json | 200 | Wed, 18 Nov 2026 04:37:15 GMT |
| 47 | 2026-11-18T04:37:15Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Wed, 18 Nov 2026 04:37:16 GMT |

### Requests — PULL 3 (47 requests, 2026-11-19T04:41:32Z–04:42:40Z)

| # | UTC time | URL | Status | HTTP Date |
|---|---|---|---|---|
| 1 | 2026-11-19T04:41:34Z | https://data.sec.gov/submissions/CIK0000089800.json | 200 | Thu, 19 Nov 2026 04:41:34 GMT |
| 2 | 2026-11-19T04:41:35Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Thu, 19 Nov 2026 04:41:35 GMT |
| 3 | 2026-11-19T04:41:36Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/NetIncomeLoss.json | 200 | Thu, 19 Nov 2026 04:41:37 GMT |
| 4 | 2026-11-19T04:41:37Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Assets.json | 200 | Thu, 19 Nov 2026 04:41:38 GMT |
| 5 | 2026-11-19T04:41:39Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 6 | 2026-11-19T04:41:40Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 7 | 2026-11-19T04:41:42Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/LiabilitiesAndStockholdersEquity.json | 200 | Thu, 19 Nov 2026 04:41:43 GMT |
| 8 | 2026-11-19T04:41:44Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/StockholdersEquity.json | 200 | Thu, 19 Nov 2026 04:41:44 GMT |
| 9 | 2026-11-19T04:41:45Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000089800/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Thu, 19 Nov 2026 04:41:45 GMT |
| 10 | 2026-11-19T04:41:46Z | https://data.sec.gov/submissions/CIK0000723254.json | 200 | Thu, 19 Nov 2026 04:41:46 GMT |
| 11 | 2026-11-19T04:41:47Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Thu, 19 Nov 2026 04:41:48 GMT |
| 12 | 2026-11-19T04:41:48Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/NetIncomeLoss.json | 200 | Thu, 19 Nov 2026 04:41:49 GMT |
| 13 | 2026-11-19T04:41:49Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Assets.json | 200 | Thu, 19 Nov 2026 04:41:50 GMT |
| 14 | 2026-11-19T04:41:50Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 15 | 2026-11-19T04:41:52Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/Liabilities.json | error: HTTP Error 404: Not Found |  |
| 16 | 2026-11-19T04:41:55Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/LiabilitiesAndStockholdersEquity.json | 200 | Thu, 19 Nov 2026 04:41:55 GMT |
| 17 | 2026-11-19T04:41:56Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/StockholdersEquity.json | 200 | Thu, 19 Nov 2026 04:41:57 GMT |
| 18 | 2026-11-19T04:41:58Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723254/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Thu, 19 Nov 2026 04:41:58 GMT |
| 19 | 2026-11-19T04:42:00Z | https://data.sec.gov/submissions/CIK0000920760.json | 200 | Thu, 19 Nov 2026 04:42:00 GMT |
| 20 | 2026-11-19T04:42:01Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 21 | 2026-11-19T04:42:03Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 22 | 2026-11-19T04:42:05Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Revenues.json | 200 | Thu, 19 Nov 2026 04:42:06 GMT |
| 23 | 2026-11-19T04:42:06Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/NetIncomeLoss.json | 200 | Thu, 19 Nov 2026 04:42:07 GMT |
| 24 | 2026-11-19T04:42:08Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Assets.json | 200 | Thu, 19 Nov 2026 04:42:08 GMT |
| 25 | 2026-11-19T04:42:09Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/Liabilities.json | 200 | Thu, 19 Nov 2026 04:42:09 GMT |
| 26 | 2026-11-19T04:42:10Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/StockholdersEquity.json | 200 | Thu, 19 Nov 2026 04:42:11 GMT |
| 27 | 2026-11-19T04:42:11Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Thu, 19 Nov 2026 04:42:12 GMT |
| 28 | 2026-11-19T04:42:12Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/SalesRevenueNet.json | error: HTTP Error 404: Not Found |  |
| 29 | 2026-11-19T04:42:14Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/SalesRevenueNet.json | error: HTTP Error 404: Not Found |  |
| 30 | 2026-11-19T04:42:16Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerIncludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 31 | 2026-11-19T04:42:18Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000920760/us-gaap/RevenueFromContractWithCustomerIncludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 32 | 2026-11-19T04:42:20Z | https://data.sec.gov/submissions/CIK0000916365.json | 200 | Thu, 19 Nov 2026 04:42:21 GMT |
| 33 | 2026-11-19T04:42:21Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 34 | 2026-11-19T04:42:23Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | error: HTTP Error 404: Not Found |  |
| 35 | 2026-11-19T04:42:25Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Revenues.json | 200 | Thu, 19 Nov 2026 04:42:26 GMT |
| 36 | 2026-11-19T04:42:26Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/NetIncomeLoss.json | 200 | Thu, 19 Nov 2026 04:42:27 GMT |
| 37 | 2026-11-19T04:42:27Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Assets.json | 200 | Thu, 19 Nov 2026 04:42:28 GMT |
| 38 | 2026-11-19T04:42:29Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/Liabilities.json | 200 | Thu, 19 Nov 2026 04:42:29 GMT |
| 39 | 2026-11-19T04:42:30Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/StockholdersEquity.json | 200 | Thu, 19 Nov 2026 04:42:30 GMT |
| 40 | 2026-11-19T04:42:31Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000916365/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Thu, 19 Nov 2026 04:42:32 GMT |
| 41 | 2026-11-19T04:42:32Z | https://data.sec.gov/submissions/CIK0000723531.json | 200 | Thu, 19 Nov 2026 04:42:32 GMT |
| 42 | 2026-11-19T04:42:34Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/RevenueFromContractWithCustomerExcludingAssessedTax.json | 200 | Thu, 19 Nov 2026 04:42:34 GMT |
| 43 | 2026-11-19T04:42:35Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/NetIncomeLoss.json | 200 | Thu, 19 Nov 2026 04:42:36 GMT |
| 44 | 2026-11-19T04:42:36Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/Assets.json | 200 | Thu, 19 Nov 2026 04:42:37 GMT |
| 45 | 2026-11-19T04:42:37Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/Liabilities.json | 200 | Thu, 19 Nov 2026 04:42:38 GMT |
| 46 | 2026-11-19T04:42:39Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/StockholdersEquity.json | 200 | Thu, 19 Nov 2026 04:42:39 GMT |
| 47 | 2026-11-19T04:42:40Z | https://data.sec.gov/api/xbrl/companyconcept/CIK0000723531/us-gaap/NetCashProvidedByUsedInOperatingActivities.json | 200 | Thu, 19 Nov 2026 04:42:41 GMT |

### Raw excerpts behind each table value (last good pull — PULL 3, byte-identical to PULL 2)

One excerpt per CSV row: the source entry behind the ORIGINAL value, then the
source entry behind the LATEST value, taken verbatim from the raw companyconcept
responses saved under `raw3/` (verified: all 30 companyconcept files in `raw3/`
are byte-identical to `raw2/`; the only file that differs is
`submissions-920760.json`, which carries no excerpted values). For derived total-liabilities rows, both component
entries (LiabilitiesAndStockholdersEquity and StockholdersEquity) are shown.
`val` is the value as reported by the SEC; `filed`/`form`/`accn` identify the filing.
Rows whose value is "not available" have no source entry — that is stated, not
hidden. Excerpts are grouped by company and fiscal year, in the same order as
the tables above, so each table cell can be checked against its excerpt here.

#### Sherwin-Williams (CIK 89800) — PULL 2 excerpts

**FY2021 (period end 2021-12-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 19,944,600,000, latest = 19,944,600,000
  - original: `{"accn":"0000089800-22-000007","end":"2021-12-31","start":"2021-01-01","val":19944600000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000089800-24-000033","end":"2021-12-31","start":"2021-01-01","val":19944600000,"filed":"2024-02-20","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,864,400,000, latest = 1,864,400,000
  - original: `{"accn":"0000089800-22-000007","end":"2021-12-31","start":"2021-01-01","val":1864400000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000089800-24-000033","end":"2021-12-31","start":"2021-01-01","val":1864400000,"filed":"2024-02-20","form":"10-K"}`
- total assets (tag `Assets`): original = 20,666,700,000, latest = 20,666,700,000
  - original: `{"accn":"0000089800-22-000007","end":"2021-12-31","val":20666700000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000089800-24-000033","end":"2021-12-31","val":20666700000,"filed":"2024-02-20","form":"10-K"}`
- total liabilities (tag `derived`): original = 18,229,500,000, latest = 18,229,500,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000089800-22-000007","end":"2021-12-31","val":20666700000,"filed":"2022-02-17","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000089800-24-000033","end":"2021-12-31","val":20666700000,"filed":"2024-02-20","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000089800-22-000007","end":"2021-12-31","val":2437200000,"filed":"2022-02-17","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000089800-25-000030","end":"2021-12-31","val":2437200000,"filed":"2025-02-20","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 2,437,200,000, latest = 2,437,200,000
  - original: `{"accn":"0000089800-22-000007","end":"2021-12-31","val":2437200000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000089800-25-000030","end":"2021-12-31","val":2437200000,"filed":"2025-02-20","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 2,244,600,000, latest = 2,244,600,000
  - original: `{"accn":"0000089800-22-000007","end":"2021-12-31","start":"2021-01-01","val":2244600000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000089800-24-000033","end":"2021-12-31","start":"2021-01-01","val":2244600000,"filed":"2024-02-20","form":"10-K"}`

**FY2022 (period end 2022-12-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 22,148,900,000, latest = 22,148,900,000
  - original: `{"accn":"0000089800-23-000007","end":"2022-12-31","start":"2022-01-01","val":22148900000,"filed":"2023-02-22","form":"10-K"}`
  - latest: `{"accn":"0000089800-25-000030","end":"2022-12-31","start":"2022-01-01","val":22148900000,"filed":"2025-02-20","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 2,020,100,000, latest = 2,020,100,000
  - original: `{"accn":"0000089800-23-000007","end":"2022-12-31","start":"2022-01-01","val":2020100000,"filed":"2023-02-22","form":"10-K"}`
  - latest: `{"accn":"0000089800-25-000030","end":"2022-12-31","start":"2022-01-01","val":2020100000,"filed":"2025-02-20","form":"10-K"}`
- total assets (tag `Assets`): original = 22,594,000,000, latest = 22,594,000,000
  - original: `{"accn":"0000089800-23-000007","end":"2022-12-31","val":22594000000,"filed":"2023-02-22","form":"10-K"}`
  - latest: `{"accn":"0000089800-25-000030","end":"2022-12-31","val":22594000000,"filed":"2025-02-20","form":"10-K"}`
- total liabilities (tag `derived`): original = 19,491,900,000, latest = 19,491,900,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000089800-23-000007","end":"2022-12-31","val":22594000000,"filed":"2023-02-22","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000089800-25-000030","end":"2022-12-31","val":22594000000,"filed":"2025-02-20","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000089800-23-000007","end":"2022-12-31","val":3102100000,"filed":"2023-02-22","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000089800-26-000008","end":"2022-12-31","val":3102100000,"filed":"2026-02-19","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,102,100,000, latest = 3,102,100,000
  - original: `{"accn":"0000089800-23-000007","end":"2022-12-31","val":3102100000,"filed":"2023-02-22","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2022-12-31","val":3102100000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,919,900,000, latest = 1,919,900,000
  - original: `{"accn":"0000089800-23-000007","end":"2022-12-31","start":"2022-01-01","val":1919900000,"filed":"2023-02-22","form":"10-K"}`
  - latest: `{"accn":"0000089800-25-000030","end":"2022-12-31","start":"2022-01-01","val":1919900000,"filed":"2025-02-20","form":"10-K"}`

**FY2023 (period end 2023-12-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 23,051,900,000, latest = 23,051,900,000
  - original: `{"accn":"0000089800-24-000033","end":"2023-12-31","start":"2023-01-01","val":23051900000,"filed":"2024-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2023-12-31","start":"2023-01-01","val":23051900000,"filed":"2026-02-19","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 2,388,800,000, latest = 2,388,800,000
  - original: `{"accn":"0000089800-24-000033","end":"2023-12-31","start":"2023-01-01","val":2388800000,"filed":"2024-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2023-12-31","start":"2023-01-01","val":2388800000,"filed":"2026-02-19","form":"10-K"}`
- total assets (tag `Assets`): original = 22,954,400,000, latest = 22,954,400,000
  - original: `{"accn":"0000089800-24-000033","end":"2023-12-31","val":22954400000,"filed":"2024-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2023-12-31","val":22954400000,"filed":"2026-02-19","form":"10-K"}`
- total liabilities (tag `derived`): original = 19,238,600,000, latest = 19,238,600,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000089800-24-000033","end":"2023-12-31","val":22954400000,"filed":"2024-02-20","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000089800-26-000008","end":"2023-12-31","val":22954400000,"filed":"2026-02-19","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000089800-24-000033","end":"2023-12-31","val":3715800000,"filed":"2024-02-20","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000089800-26-000008","end":"2023-12-31","val":3715800000,"filed":"2026-02-19","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,715,800,000, latest = 3,715,800,000
  - original: `{"accn":"0000089800-24-000033","end":"2023-12-31","val":3715800000,"filed":"2024-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2023-12-31","val":3715800000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 3,521,900,000, latest = 3,521,900,000
  - original: `{"accn":"0000089800-24-000033","end":"2023-12-31","start":"2023-01-01","val":3521900000,"filed":"2024-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2023-12-31","start":"2023-01-01","val":3521900000,"filed":"2026-02-19","form":"10-K"}`

**FY2024 (period end 2024-12-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 23,098,500,000, latest = 23,098,500,000
  - original: `{"accn":"0000089800-25-000030","end":"2024-12-31","start":"2024-01-01","val":23098500000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2024-12-31","start":"2024-01-01","val":23098500000,"filed":"2026-02-19","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 2,681,400,000, latest = 2,681,400,000
  - original: `{"accn":"0000089800-25-000030","end":"2024-12-31","start":"2024-01-01","val":2681400000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2024-12-31","start":"2024-01-01","val":2681400000,"filed":"2026-02-19","form":"10-K"}`
- total assets (tag `Assets`): original = 23,632,600,000, latest = 23,632,600,000
  - original: `{"accn":"0000089800-25-000030","end":"2024-12-31","val":23632600000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2024-12-31","val":23632600000,"filed":"2026-02-19","form":"10-K"}`
- total liabilities (tag `derived`): original = 19,581,400,000, latest = 19,581,400,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000089800-25-000030","end":"2024-12-31","val":23632600000,"filed":"2025-02-20","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000089800-26-000008","end":"2024-12-31","val":23632600000,"filed":"2026-02-19","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000089800-25-000030","end":"2024-12-31","val":4051200000,"filed":"2025-02-20","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000089800-26-000008","end":"2024-12-31","val":4051200000,"filed":"2026-02-19","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 4,051,200,000, latest = 4,051,200,000
  - original: `{"accn":"0000089800-25-000030","end":"2024-12-31","val":4051200000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2024-12-31","val":4051200000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 3,153,200,000, latest = 3,153,200,000
  - original: `{"accn":"0000089800-25-000030","end":"2024-12-31","start":"2024-01-01","val":3153200000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2024-12-31","start":"2024-01-01","val":3153200000,"filed":"2026-02-19","form":"10-K"}`

**FY2025 (period end 2025-12-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 23,574,300,000, latest = 23,574,300,000
  - original: `{"accn":"0000089800-26-000008","end":"2025-12-31","start":"2025-01-01","val":23574300000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2025-12-31","start":"2025-01-01","val":23574300000,"filed":"2026-02-19","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 2,568,500,000, latest = 2,568,500,000
  - original: `{"accn":"0000089800-26-000008","end":"2025-12-31","start":"2025-01-01","val":2568500000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2025-12-31","start":"2025-01-01","val":2568500000,"filed":"2026-02-19","form":"10-K"}`
- total assets (tag `Assets`): original = 25,901,700,000, latest = 25,901,700,000
  - original: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":25901700000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":25901700000,"filed":"2026-02-19","form":"10-K"}`
- total liabilities (tag `derived`): original = 21,303,400,000, latest = 21,303,400,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":25901700000,"filed":"2026-02-19","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":25901700000,"filed":"2026-02-19","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":4598300000,"filed":"2026-02-19","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":4598300000,"filed":"2026-02-19","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 4,598,300,000, latest = 4,598,300,000
  - original: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":4598300000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2025-12-31","val":4598300000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 3,451,600,000, latest = 3,451,600,000
  - original: `{"accn":"0000089800-26-000008","end":"2025-12-31","start":"2025-01-01","val":3451600000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000089800-26-000008","end":"2025-12-31","start":"2025-01-01","val":3451600000,"filed":"2026-02-19","form":"10-K"}`

#### Cintas (CIK 723254) — PULL 2 excerpts

**FY2022 (period end 2022-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 7,854,459,000, latest = 7,854,459,000
  - original: `{"accn":"0000723254-22-000019","end":"2022-05-31","start":"2021-06-01","val":7854459000,"filed":"2022-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-24-000036","end":"2022-05-31","start":"2021-06-01","val":7854459000,"filed":"2024-07-25","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,235,757,000, latest = 1,235,757,000
  - original: `{"accn":"0000723254-22-000019","end":"2022-05-31","start":"2021-06-01","val":1235757000,"filed":"2022-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-24-000036","end":"2022-05-31","start":"2021-06-01","val":1235757000,"filed":"2024-07-25","form":"10-K"}`
- total assets (tag `Assets`): original = 8,147,256,000, latest = 8,147,256,000
  - original: `{"accn":"0000723254-22-000019","end":"2022-05-31","val":8147256000,"filed":"2022-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-24-000036","end":"2022-05-31","val":8147256000,"filed":"2024-07-25","form":"10-K"}`
- total liabilities (tag `derived`): original = 4,839,060,000, latest = 4,839,060,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000723254-22-000019","end":"2022-05-31","val":8147256000,"filed":"2022-07-27","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000723254-23-000025","end":"2022-05-31","val":8147256000,"filed":"2023-07-27","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000723254-22-000019","end":"2022-05-31","val":3308196000,"filed":"2022-07-27","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000723254-25-000017","end":"2022-05-31","val":3308196000,"filed":"2025-07-28","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,308,196,000, latest = 3,308,196,000
  - original: `{"accn":"0000723254-22-000019","end":"2022-05-31","val":3308196000,"filed":"2022-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-25-000017","end":"2022-05-31","val":3308196000,"filed":"2025-07-28","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,537,625,000, latest = 1,537,625,000
  - original: `{"accn":"0000723254-22-000019","end":"2022-05-31","start":"2021-06-01","val":1537625000,"filed":"2022-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-24-000036","end":"2022-05-31","start":"2021-06-01","val":1537625000,"filed":"2024-07-25","form":"10-K"}`

**FY2023 (period end 2023-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 8,815,769,000, latest = 8,815,769,000
  - original: `{"accn":"0000723254-23-000025","end":"2023-05-31","start":"2022-06-01","val":8815769000,"filed":"2023-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-25-000017","end":"2023-05-31","start":"2022-06-01","val":8815769000,"filed":"2025-07-28","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,348,010,000, latest = 1,348,010,000
  - original: `{"accn":"0000723254-23-000025","end":"2023-05-31","start":"2022-06-01","val":1348010000,"filed":"2023-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-25-000017","end":"2023-05-31","start":"2022-06-01","val":1348010000,"filed":"2025-07-28","form":"10-K"}`
- total assets (tag `Assets`): original = 8,546,356,000, latest = 8,546,356,000
  - original: `{"accn":"0000723254-23-000025","end":"2023-05-31","val":8546356000,"filed":"2023-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-25-000017","end":"2023-05-31","val":8546356000,"filed":"2025-07-28","form":"10-K"}`
- total liabilities (tag `derived`): original = 4,682,370,000, latest = 4,682,370,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000723254-23-000025","end":"2023-05-31","val":8546356000,"filed":"2023-07-27","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000723254-24-000036","end":"2023-05-31","val":8546356000,"filed":"2024-07-25","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000723254-23-000025","end":"2023-05-31","val":3863986000,"filed":"2023-07-27","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000723254-26-000028","end":"2023-05-31","val":3863986000,"filed":"2026-07-29","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,863,986,000, latest = 3,863,986,000
  - original: `{"accn":"0000723254-23-000025","end":"2023-05-31","val":3863986000,"filed":"2023-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2023-05-31","val":3863986000,"filed":"2026-07-29","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,597,814,000, latest = 1,586,228,000
  - original: `{"accn":"0000723254-23-000025","end":"2023-05-31","start":"2022-06-01","val":1597814000,"filed":"2023-07-27","form":"10-K"}`
  - latest: `{"accn":"0000723254-25-000017","end":"2023-05-31","start":"2022-06-01","val":1586228000,"filed":"2025-07-28","form":"10-K"}`

**FY2024 (period end 2024-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 9,596,615,000, latest = 9,596,615,000
  - original: `{"accn":"0000723254-24-000036","end":"2024-05-31","start":"2023-06-01","val":9596615000,"filed":"2024-07-25","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2024-05-31","start":"2023-06-01","val":9596615000,"filed":"2026-07-29","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,571,592,000, latest = 1,571,592,000
  - original: `{"accn":"0000723254-24-000036","end":"2024-05-31","start":"2023-06-01","val":1571592000,"filed":"2024-07-25","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2024-05-31","start":"2023-06-01","val":1571592000,"filed":"2026-07-29","form":"10-K"}`
- total assets (tag `Assets`): original = 9,168,817,000, latest = 9,168,817,000
  - original: `{"accn":"0000723254-24-000036","end":"2024-05-31","val":9168817000,"filed":"2024-07-25","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2024-05-31","val":9168817000,"filed":"2026-07-29","form":"10-K"}`
- total liabilities (tag `derived`): original = 4,852,445,000, latest = 4,852,445,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000723254-24-000036","end":"2024-05-31","val":9168817000,"filed":"2024-07-25","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000723254-25-000017","end":"2024-05-31","val":9168817000,"filed":"2025-07-28","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000723254-24-000036","end":"2024-05-31","val":4316372000,"filed":"2024-07-25","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000723254-26-000028","end":"2024-05-31","val":4316372000,"filed":"2026-07-29","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 4,316,372,000, latest = 4,316,372,000
  - original: `{"accn":"0000723254-24-000036","end":"2024-05-31","val":4316372000,"filed":"2024-07-25","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2024-05-31","val":4316372000,"filed":"2026-07-29","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 2,079,781,000, latest = 2,068,500,000
  - original: `{"accn":"0000723254-24-000036","end":"2024-05-31","start":"2023-06-01","val":2079781000,"filed":"2024-07-25","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2024-05-31","start":"2023-06-01","val":2068500000,"filed":"2026-07-29","form":"10-K"}`

**FY2025 (period end 2025-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 10,340,181,000, latest = 10,340,181,000
  - original: `{"accn":"0000723254-25-000017","end":"2025-05-31","start":"2024-06-01","val":10340181000,"filed":"2025-07-28","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2025-05-31","start":"2024-06-01","val":10340181000,"filed":"2026-07-29","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,812,281,000, latest = 1,812,281,000
  - original: `{"accn":"0000723254-25-000017","end":"2025-05-31","start":"2024-06-01","val":1812281000,"filed":"2025-07-28","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2025-05-31","start":"2024-06-01","val":1812281000,"filed":"2026-07-29","form":"10-K"}`
- total assets (tag `Assets`): original = 9,825,241,000, latest = 9,825,241,000
  - original: `{"accn":"0000723254-25-000017","end":"2025-05-31","val":9825241000,"filed":"2025-07-28","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2025-05-31","val":9825241000,"filed":"2026-07-29","form":"10-K"}`
- total liabilities (tag `derived`): original = 5,140,760,000, latest = 5,140,760,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000723254-25-000017","end":"2025-05-31","val":9825241000,"filed":"2025-07-28","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000723254-26-000028","end":"2025-05-31","val":9825241000,"filed":"2026-07-29","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000723254-25-000017","end":"2025-05-31","val":4684481000,"filed":"2025-07-28","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000723254-26-000028","end":"2025-05-31","val":4684481000,"filed":"2026-07-29","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 4,684,481,000, latest = 4,684,481,000
  - original: `{"accn":"0000723254-25-000017","end":"2025-05-31","val":4684481000,"filed":"2025-07-28","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2025-05-31","val":4684481000,"filed":"2026-07-29","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 2,165,905,000, latest = 2,165,905,000
  - original: `{"accn":"0000723254-25-000017","end":"2025-05-31","start":"2024-06-01","val":2165905000,"filed":"2025-07-28","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2025-05-31","start":"2024-06-01","val":2165905000,"filed":"2026-07-29","form":"10-K"}`

**FY2026 (period end 2026-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 11,264,761,000, latest = 11,264,761,000
  - original: `{"accn":"0000723254-26-000028","end":"2026-05-31","start":"2025-06-01","val":11264761000,"filed":"2026-07-29","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2026-05-31","start":"2025-06-01","val":11264761000,"filed":"2026-07-29","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,999,968,000, latest = 1,999,968,000
  - original: `{"accn":"0000723254-26-000028","end":"2026-05-31","start":"2025-06-01","val":1999968000,"filed":"2026-07-29","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2026-05-31","start":"2025-06-01","val":1999968000,"filed":"2026-07-29","form":"10-K"}`
- total assets (tag `Assets`): original = 10,529,140,000, latest = 10,529,140,000
  - original: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":10529140000,"filed":"2026-07-29","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":10529140000,"filed":"2026-07-29","form":"10-K"}`
- total liabilities (tag `derived`): original = 5,389,253,000, latest = 5,389,253,000
  - LiabilitiesAndStockholdersEquity original: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":10529140000,"filed":"2026-07-29","form":"10-K"}`
  - LiabilitiesAndStockholdersEquity latest: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":10529140000,"filed":"2026-07-29","form":"10-K"}`
  - StockholdersEquity original: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":5139887000,"filed":"2026-07-29","form":"10-K"}`
  - StockholdersEquity latest: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":5139887000,"filed":"2026-07-29","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 5,139,887,000, latest = 5,139,887,000
  - original: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":5139887000,"filed":"2026-07-29","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2026-05-31","val":5139887000,"filed":"2026-07-29","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 2,276,280,000, latest = 2,276,280,000
  - original: `{"accn":"0000723254-26-000028","end":"2026-05-31","start":"2025-06-01","val":2276280000,"filed":"2026-07-29","form":"10-K"}`
  - latest: `{"accn":"0000723254-26-000028","end":"2026-05-31","start":"2025-06-01","val":2276280000,"filed":"2026-07-29","form":"10-K"}`

#### Lennar (CIK 920760) — PULL 2 excerpts

**FY2021 (period end 2021-11-30)**

- revenue (tag `Revenues`): original = 27,130,676,000, latest = 27,130,676,000
  - original: `{"accn":"0001628280-22-001450","end":"2021-11-30","start":"2020-12-01","val":27130676000,"filed":"2022-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-24-002371","end":"2021-11-30","start":"2020-12-01","val":27130676000,"filed":"2024-01-26","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 4,430,111,000, latest = 4,430,111,000
  - original: `{"accn":"0001628280-22-001450","end":"2021-11-30","start":"2020-12-01","val":4430111000,"filed":"2022-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-24-002371","end":"2021-11-30","start":"2020-12-01","val":4430111000,"filed":"2024-01-26","form":"10-K"}`
- total assets (tag `Assets`): original = 33,207,778,000, latest = 33,207,778,000
  - original: `{"accn":"0001628280-22-001450","end":"2021-11-30","val":33207778000,"filed":"2022-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-23-001606","end":"2021-11-30","val":33207778000,"filed":"2023-01-26","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 12,211,496,000, latest = 12,211,496,000
  - original: `{"accn":"0001628280-22-001450","end":"2021-11-30","val":12211496000,"filed":"2022-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-23-001606","end":"2021-11-30","val":12211496000,"filed":"2023-01-26","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 20,816,425,000, latest = 20,816,425,000
  - original: `{"accn":"0001628280-22-001450","end":"2021-11-30","val":20816425000,"filed":"2022-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-23-001606","end":"2021-11-30","val":20816425000,"filed":"2023-01-26","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 2,532,774,000, latest = 2,532,774,000
  - original: `{"accn":"0001628280-22-001450","end":"2021-11-30","start":"2020-12-01","val":2532774000,"filed":"2022-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-24-002371","end":"2021-11-30","start":"2020-12-01","val":2532774000,"filed":"2024-01-26","form":"10-K"}`

**FY2022 (period end 2022-11-30)**

- revenue (tag `Revenues`): original = not available, latest = 33,671,010,000
  - original: `no entry reported for this 10-K accession and period end`
  - latest: `{"accn":"0001628280-25-002404","end":"2022-11-30","start":"2021-12-01","val":33671010000,"filed":"2025-01-23","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 4,614,125,000, latest = 4,614,125,000
  - original: `{"accn":"0001628280-23-001606","end":"2022-11-30","start":"2021-12-01","val":4614125000,"filed":"2023-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-25-002404","end":"2022-11-30","start":"2021-12-01","val":4614125000,"filed":"2025-01-23","form":"10-K"}`
- total assets (tag `Assets`): original = 37,984,295,000, latest = 37,984,295,000
  - original: `{"accn":"0001628280-23-001606","end":"2022-11-30","val":37984295000,"filed":"2023-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-24-002371","end":"2022-11-30","val":37984295000,"filed":"2024-01-26","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 13,743,928,000, latest = 13,743,928,000
  - original: `{"accn":"0001628280-23-001606","end":"2022-11-30","val":13743928000,"filed":"2023-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-24-002371","end":"2022-11-30","val":13743928000,"filed":"2024-01-26","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 24,100,500,000, latest = 24,100,500,000
  - original: `{"accn":"0001628280-23-001606","end":"2022-11-30","val":24100500000,"filed":"2023-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-24-002371","end":"2022-11-30","val":24100500000,"filed":"2024-01-26","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 3,265,668,000, latest = 3,265,668,000
  - original: `{"accn":"0001628280-23-001606","end":"2022-11-30","start":"2021-12-01","val":3265668000,"filed":"2023-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-25-002404","end":"2022-11-30","start":"2021-12-01","val":3265668000,"filed":"2025-01-23","form":"10-K"}`

**FY2023 (period end 2023-11-30)**

- revenue (tag `Revenues`): original = 34,233,366,000, latest = 34,233,366,000
  - original: `{"accn":"0001628280-24-002371","end":"2023-11-30","start":"2022-12-01","val":34233366000,"filed":"2024-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2023-11-30","start":"2022-12-01","val":34233366000,"filed":"2026-01-28","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 3,938,511,000, latest = 3,938,511,000
  - original: `{"accn":"0001628280-24-002371","end":"2023-11-30","start":"2022-12-01","val":3938511000,"filed":"2024-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2023-11-30","start":"2022-12-01","val":3938511000,"filed":"2026-01-28","form":"10-K"}`
- total assets (tag `Assets`): original = 39,234,303,000, latest = 39,234,303,000
  - original: `{"accn":"0001628280-24-002371","end":"2023-11-30","val":39234303000,"filed":"2024-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-25-002404","end":"2023-11-30","val":39234303000,"filed":"2025-01-23","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 12,532,337,000, latest = 12,532,337,000
  - original: `{"accn":"0001628280-24-002371","end":"2023-11-30","val":12532337000,"filed":"2024-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-25-002404","end":"2023-11-30","val":12532337000,"filed":"2025-01-23","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 26,580,664,000, latest = 26,580,664,000
  - original: `{"accn":"0001628280-24-002371","end":"2023-11-30","val":26580664000,"filed":"2024-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-25-002404","end":"2023-11-30","val":26580664000,"filed":"2025-01-23","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 5,179,738,000, latest = 5,179,738,000
  - original: `{"accn":"0001628280-24-002371","end":"2023-11-30","start":"2022-12-01","val":5179738000,"filed":"2024-01-26","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2023-11-30","start":"2022-12-01","val":5179738000,"filed":"2026-01-28","form":"10-K"}`

**FY2024 (period end 2024-11-30)**

- revenue (tag `Revenues`): original = 35,441,452,000, latest = 35,441,452,000
  - original: `{"accn":"0001628280-25-002404","end":"2024-11-30","start":"2023-12-01","val":35441452000,"filed":"2025-01-23","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2024-11-30","start":"2023-12-01","val":35441452000,"filed":"2026-01-28","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 3,932,533,000, latest = 3,932,533,000
  - original: `{"accn":"0001628280-25-002404","end":"2024-11-30","start":"2023-12-01","val":3932533000,"filed":"2025-01-23","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2024-11-30","start":"2023-12-01","val":3932533000,"filed":"2026-01-28","form":"10-K"}`
- total assets (tag `Assets`): original = 41,312,781,000, latest = 41,312,781,000
  - original: `{"accn":"0001628280-25-002404","end":"2024-11-30","val":41312781000,"filed":"2025-01-23","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2024-11-30","val":41312781000,"filed":"2026-01-28","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 13,291,556,000, latest = 13,291,556,000
  - original: `{"accn":"0001628280-25-002404","end":"2024-11-30","val":13291556000,"filed":"2025-01-23","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2024-11-30","val":13291556000,"filed":"2026-01-28","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 27,870,135,000, latest = 27,870,135,000
  - original: `{"accn":"0001628280-25-002404","end":"2024-11-30","val":27870135000,"filed":"2025-01-23","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2024-11-30","val":27870135000,"filed":"2026-01-28","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 2,403,379,000, latest = 2,403,379,000
  - original: `{"accn":"0001628280-25-002404","end":"2024-11-30","start":"2023-12-01","val":2403379000,"filed":"2025-01-23","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2024-11-30","start":"2023-12-01","val":2403379000,"filed":"2026-01-28","form":"10-K"}`

**FY2025 (period end 2025-11-30)**

- revenue (tag `Revenues`): original = 34,186,934,000, latest = 34,186,934,000
  - original: `{"accn":"0001628280-26-003870","end":"2025-11-30","start":"2024-12-01","val":34186934000,"filed":"2026-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2025-11-30","start":"2024-12-01","val":34186934000,"filed":"2026-01-28","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 2,078,179,000, latest = 2,078,179,000
  - original: `{"accn":"0001628280-26-003870","end":"2025-11-30","start":"2024-12-01","val":2078179000,"filed":"2026-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2025-11-30","start":"2024-12-01","val":2078179000,"filed":"2026-01-28","form":"10-K"}`
- total assets (tag `Assets`): original = 34,430,437,000, latest = 34,430,437,000
  - original: `{"accn":"0001628280-26-003870","end":"2025-11-30","val":34430437000,"filed":"2026-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2025-11-30","val":34430437000,"filed":"2026-01-28","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 12,289,828,000, latest = 12,289,828,000
  - original: `{"accn":"0001628280-26-003870","end":"2025-11-30","val":12289828000,"filed":"2026-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2025-11-30","val":12289828000,"filed":"2026-01-28","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 21,959,417,000, latest = 21,959,417,000
  - original: `{"accn":"0001628280-26-003870","end":"2025-11-30","val":21959417000,"filed":"2026-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2025-11-30","val":21959417000,"filed":"2026-01-28","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 216,812,000, latest = 216,812,000
  - original: `{"accn":"0001628280-26-003870","end":"2025-11-30","start":"2024-12-01","val":216812000,"filed":"2026-01-28","form":"10-K"}`
  - latest: `{"accn":"0001628280-26-003870","end":"2025-11-30","start":"2024-12-01","val":216812000,"filed":"2026-01-28","form":"10-K"}`

#### Tractor Supply (CIK 916365) — PULL 2 excerpts

**FY2021 (period end 2021-12-25)**

- revenue (tag `Revenues`): original = 12,731,105,000, latest = 12,731,105,000
  - original: `{"accn":"0000916365-22-000049","end":"2021-12-25","start":"2020-12-27","val":12731105000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000916365-24-000046","end":"2021-12-25","start":"2020-12-27","val":12731105000,"filed":"2024-02-23","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 997,114,000, latest = 997,114,000
  - original: `{"accn":"0000916365-22-000049","end":"2021-12-25","start":"2020-12-27","val":997114000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000916365-24-000046","end":"2021-12-25","start":"2020-12-27","val":997114000,"filed":"2024-02-23","form":"10-K"}`
- total assets (tag `Assets`): original = 7,767,467,000, latest = 7,767,467,000
  - original: `{"accn":"0000916365-22-000049","end":"2021-12-25","val":7767467000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000916365-23-000045","end":"2021-12-25","val":7767467000,"filed":"2023-02-23","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 5,764,802,000, latest = 5,764,802,000
  - original: `{"accn":"0000916365-22-000049","end":"2021-12-25","val":5764802000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000916365-23-000045","end":"2021-12-25","val":5764802000,"filed":"2023-02-23","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 2,002,665,000, latest = 2,002,665,000
  - original: `{"accn":"0000916365-22-000049","end":"2021-12-25","val":2002665000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000916365-25-000076","end":"2021-12-25","val":2002665000,"filed":"2025-02-20","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,138,720,000, latest = 1,138,720,000
  - original: `{"accn":"0000916365-22-000049","end":"2021-12-25","start":"2020-12-27","val":1138720000,"filed":"2022-02-17","form":"10-K"}`
  - latest: `{"accn":"0000916365-24-000046","end":"2021-12-25","start":"2020-12-27","val":1138720000,"filed":"2024-02-23","form":"10-K"}`

**FY2022 (period end 2022-12-31)**

- revenue (tag `Revenues`): original = 14,204,717,000, latest = 14,204,717,000
  - original: `{"accn":"0000916365-23-000045","end":"2022-12-31","start":"2021-12-26","val":14204717000,"filed":"2023-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-25-000076","end":"2022-12-31","start":"2021-12-26","val":14204717000,"filed":"2025-02-20","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,088,712,000, latest = 1,088,712,000
  - original: `{"accn":"0000916365-23-000045","end":"2022-12-31","start":"2021-12-26","val":1088712000,"filed":"2023-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-25-000076","end":"2022-12-31","start":"2021-12-26","val":1088712000,"filed":"2025-02-20","form":"10-K"}`
- total assets (tag `Assets`): original = 8,489,990,000, latest = 8,489,990,000
  - original: `{"accn":"0000916365-23-000045","end":"2022-12-31","val":8489990000,"filed":"2023-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-24-000046","end":"2022-12-31","val":8489990000,"filed":"2024-02-23","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 6,447,574,000, latest = 6,447,574,000
  - original: `{"accn":"0000916365-23-000045","end":"2022-12-31","val":6447574000,"filed":"2023-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-24-000046","end":"2022-12-31","val":6447574000,"filed":"2024-02-23","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 2,042,416,000, latest = 2,042,416,000
  - original: `{"accn":"0000916365-23-000045","end":"2022-12-31","val":2042416000,"filed":"2023-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2022-12-31","val":2042416000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,356,979,000, latest = 1,356,979,000
  - original: `{"accn":"0000916365-23-000045","end":"2022-12-31","start":"2021-12-26","val":1356979000,"filed":"2023-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-25-000076","end":"2022-12-31","start":"2021-12-26","val":1356979000,"filed":"2025-02-20","form":"10-K"}`

**FY2023 (period end 2023-12-30)**

- revenue (tag `Revenues`): original = 14,555,741,000, latest = 14,555,741,000
  - original: `{"accn":"0000916365-24-000046","end":"2023-12-30","start":"2023-01-01","val":14555741000,"filed":"2024-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2023-12-30","start":"2023-01-01","val":14555741000,"filed":"2026-02-19","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,107,226,000, latest = 1,107,226,000
  - original: `{"accn":"0000916365-24-000046","end":"2023-12-30","start":"2023-01-01","val":1107226000,"filed":"2024-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2023-12-30","start":"2023-01-01","val":1107226000,"filed":"2026-02-19","form":"10-K"}`
- total assets (tag `Assets`): original = 9,188,151,000, latest = 9,188,151,000
  - original: `{"accn":"0000916365-24-000046","end":"2023-12-30","val":9188151000,"filed":"2024-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-25-000076","end":"2023-12-30","val":9188151000,"filed":"2025-02-20","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 7,038,389,000, latest = 7,038,389,000
  - original: `{"accn":"0000916365-24-000046","end":"2023-12-30","val":7038389000,"filed":"2024-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-25-000076","end":"2023-12-30","val":7038389000,"filed":"2025-02-20","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 2,149,762,000, latest = 2,149,762,000
  - original: `{"accn":"0000916365-24-000046","end":"2023-12-30","val":2149762000,"filed":"2024-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2023-12-30","val":2149762000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,334,033,000, latest = 1,334,033,000
  - original: `{"accn":"0000916365-24-000046","end":"2023-12-30","start":"2023-01-01","val":1334033000,"filed":"2024-02-23","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2023-12-30","start":"2023-01-01","val":1334033000,"filed":"2026-02-19","form":"10-K"}`

**FY2024 (period end 2024-12-28)**

- revenue (tag `Revenues`): original = 14,883,231,000, latest = 14,883,231,000
  - original: `{"accn":"0000916365-25-000076","end":"2024-12-28","start":"2023-12-31","val":14883231000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2024-12-28","start":"2023-12-31","val":14883231000,"filed":"2026-02-19","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,101,240,000, latest = 1,101,240,000
  - original: `{"accn":"0000916365-25-000076","end":"2024-12-28","start":"2023-12-31","val":1101240000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2024-12-28","start":"2023-12-31","val":1101240000,"filed":"2026-02-19","form":"10-K"}`
- total assets (tag `Assets`): original = 9,805,485,000, latest = 9,805,485,000
  - original: `{"accn":"0000916365-25-000076","end":"2024-12-28","val":9805485000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2024-12-28","val":9805485000,"filed":"2026-02-19","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 7,535,151,000, latest = 7,535,151,000
  - original: `{"accn":"0000916365-25-000076","end":"2024-12-28","val":7535151000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2024-12-28","val":7535151000,"filed":"2026-02-19","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 2,270,334,000, latest = 2,270,334,000
  - original: `{"accn":"0000916365-25-000076","end":"2024-12-28","val":2270334000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2024-12-28","val":2270334000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,420,835,000, latest = 1,420,835,000
  - original: `{"accn":"0000916365-25-000076","end":"2024-12-28","start":"2023-12-31","val":1420835000,"filed":"2025-02-20","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2024-12-28","start":"2023-12-31","val":1420835000,"filed":"2026-02-19","form":"10-K"}`

**FY2025 (period end 2025-12-27)**

- revenue (tag `Revenues`): original = 15,524,046,000, latest = 15,524,046,000
  - original: `{"accn":"0000916365-26-000014","end":"2025-12-27","start":"2024-12-29","val":15524046000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2025-12-27","start":"2024-12-29","val":15524046000,"filed":"2026-02-19","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,096,087,000, latest = 1,096,087,000
  - original: `{"accn":"0000916365-26-000014","end":"2025-12-27","start":"2024-12-29","val":1096087000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2025-12-27","start":"2024-12-29","val":1096087000,"filed":"2026-02-19","form":"10-K"}`
- total assets (tag `Assets`): original = 10,933,679,000, latest = 10,933,679,000
  - original: `{"accn":"0000916365-26-000014","end":"2025-12-27","val":10933679000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2025-12-27","val":10933679000,"filed":"2026-02-19","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 8,352,386,000, latest = 8,352,386,000
  - original: `{"accn":"0000916365-26-000014","end":"2025-12-27","val":8352386000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2025-12-27","val":8352386000,"filed":"2026-02-19","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 2,581,293,000, latest = 2,581,293,000
  - original: `{"accn":"0000916365-26-000014","end":"2025-12-27","val":2581293000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2025-12-27","val":2581293000,"filed":"2026-02-19","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,635,259,000, latest = 1,635,259,000
  - original: `{"accn":"0000916365-26-000014","end":"2025-12-27","start":"2024-12-29","val":1635259000,"filed":"2026-02-19","form":"10-K"}`
  - latest: `{"accn":"0000916365-26-000014","end":"2025-12-27","start":"2024-12-29","val":1635259000,"filed":"2026-02-19","form":"10-K"}`

#### Paychex (CIK 723531) — PULL 2 excerpts

**FY2022 (period end 2022-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 4,554,000,000, latest = 4,554,000,000
  - original: `{"accn":"0000950170-22-012734","end":"2022-05-31","start":"2021-06-01","val":4554000000,"filed":"2022-07-15","form":"10-K"}`
  - latest: `{"accn":"0000950170-24-082958","end":"2022-05-31","start":"2021-06-01","val":4554000000,"filed":"2024-07-11","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = not available, latest = not available
  - original: `no entry reported for this 10-K accession and period end`
  - latest: `no entry reported in any 10-K/10-K/A for this period end`
- total assets (tag `Assets`): original = 9,635,200,000, latest = 9,635,200,000
  - original: `{"accn":"0000950170-22-012734","end":"2022-05-31","val":9635200000,"filed":"2022-07-15","form":"10-K"}`
  - latest: `{"accn":"0000950170-23-032988","end":"2022-05-31","val":9635200000,"filed":"2023-07-14","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 6,550,000,000, latest = 6,550,000,000
  - original: `{"accn":"0000950170-22-012734","end":"2022-05-31","val":6550000000,"filed":"2022-07-15","form":"10-K"}`
  - latest: `{"accn":"0000950170-23-032988","end":"2022-05-31","val":6550000000,"filed":"2023-07-14","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,085,200,000, latest = 3,085,200,000
  - original: `{"accn":"0000950170-22-012734","end":"2022-05-31","val":3085200000,"filed":"2022-07-15","form":"10-K"}`
  - latest: `{"accn":"0000950170-25-095300","end":"2022-05-31","val":3085200000,"filed":"2025-07-11","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,505,500,000, latest = 1,589,700,000
  - original: `{"accn":"0000950170-22-012734","end":"2022-05-31","start":"2021-06-01","val":1505500000,"filed":"2022-07-15","form":"10-K"}`
  - latest: `{"accn":"0000950170-24-082958","end":"2022-05-31","start":"2021-06-01","val":1589700000,"filed":"2024-07-11","form":"10-K"}`

**FY2023 (period end 2023-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 4,907,300,000, latest = 4,907,300,000
  - original: `{"accn":"0000950170-23-032988","end":"2023-05-31","start":"2022-06-01","val":4907300000,"filed":"2023-07-14","form":"10-K"}`
  - latest: `{"accn":"0000950170-25-095300","end":"2023-05-31","start":"2022-06-01","val":4907300000,"filed":"2025-07-11","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = not available, latest = not available
  - original: `no entry reported for this 10-K accession and period end`
  - latest: `no entry reported in any 10-K/10-K/A for this period end`
- total assets (tag `Assets`): original = 10,546,400,000, latest = 10,546,400,000
  - original: `{"accn":"0000950170-23-032988","end":"2023-05-31","val":10546400000,"filed":"2023-07-14","form":"10-K"}`
  - latest: `{"accn":"0000950170-24-082958","end":"2023-05-31","val":10546400000,"filed":"2024-07-11","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 7,053,200,000, latest = 7,053,200,000
  - original: `{"accn":"0000950170-23-032988","end":"2023-05-31","val":7053200000,"filed":"2023-07-14","form":"10-K"}`
  - latest: `{"accn":"0000950170-24-082958","end":"2023-05-31","val":7053200000,"filed":"2024-07-11","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,493,200,000, latest = 3,493,200,000
  - original: `{"accn":"0000950170-23-032988","end":"2023-05-31","val":3493200000,"filed":"2023-07-14","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2023-05-31","val":3493200000,"filed":"2026-07-17","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,699,400,000, latest = 1,706,200,000
  - original: `{"accn":"0000950170-23-032988","end":"2023-05-31","start":"2022-06-01","val":1699400000,"filed":"2023-07-14","form":"10-K"}`
  - latest: `{"accn":"0000950170-25-095300","end":"2023-05-31","start":"2022-06-01","val":1706200000,"filed":"2025-07-11","form":"10-K"}`

**FY2024 (period end 2024-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 5,132,000,000, latest = 5,132,000,000
  - original: `{"accn":"0000950170-24-082958","end":"2024-05-31","start":"2023-06-01","val":5132000000,"filed":"2024-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2024-05-31","start":"2023-06-01","val":5132000000,"filed":"2026-07-17","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = not available, latest = 1,690,400,000
  - original: `no entry reported for this 10-K accession and period end`
  - latest: `{"accn":"0001193125-26-307785","end":"2024-05-31","start":"2023-06-01","val":1690400000,"filed":"2026-07-17","form":"10-K"}`
- total assets (tag `Assets`): original = 10,383,100,000, latest = 10,383,100,000
  - original: `{"accn":"0000950170-24-082958","end":"2024-05-31","val":10383100000,"filed":"2024-07-11","form":"10-K"}`
  - latest: `{"accn":"0000950170-25-095300","end":"2024-05-31","val":10383100000,"filed":"2025-07-11","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 6,582,100,000, latest = 6,582,100,000
  - original: `{"accn":"0000950170-24-082958","end":"2024-05-31","val":6582100000,"filed":"2024-07-11","form":"10-K"}`
  - latest: `{"accn":"0000950170-25-095300","end":"2024-05-31","val":6582100000,"filed":"2025-07-11","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,801,000,000, latest = 3,801,000,000
  - original: `{"accn":"0000950170-24-082958","end":"2024-05-31","val":3801000000,"filed":"2024-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2024-05-31","val":3801000000,"filed":"2026-07-17","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,897,700,000, latest = 1,897,700,000
  - original: `{"accn":"0000950170-24-082958","end":"2024-05-31","start":"2023-06-01","val":1897700000,"filed":"2024-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2024-05-31","start":"2023-06-01","val":1897700000,"filed":"2026-07-17","form":"10-K"}`

**FY2025 (period end 2025-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 5,410,000,000, latest = 5,410,000,000
  - original: `{"accn":"0000950170-25-095300","end":"2025-05-31","start":"2024-06-01","val":5410000000,"filed":"2025-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2025-05-31","start":"2024-06-01","val":5410000000,"filed":"2026-07-17","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = not available, latest = 1,657,300,000
  - original: `no entry reported for this 10-K accession and period end`
  - latest: `{"accn":"0001193125-26-307785","end":"2025-05-31","start":"2024-06-01","val":1657300000,"filed":"2026-07-17","form":"10-K"}`
- total assets (tag `Assets`): original = 16,564,100,000, latest = 16,564,100,000
  - original: `{"accn":"0000950170-25-095300","end":"2025-05-31","val":16564100000,"filed":"2025-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2025-05-31","val":16564100000,"filed":"2026-07-17","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 12,436,100,000, latest = 12,436,100,000
  - original: `{"accn":"0000950170-25-095300","end":"2025-05-31","val":12436100000,"filed":"2025-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2025-05-31","val":12436100000,"filed":"2026-07-17","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 4,128,000,000, latest = 4,128,000,000
  - original: `{"accn":"0000950170-25-095300","end":"2025-05-31","val":4128000000,"filed":"2025-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2025-05-31","val":4128000000,"filed":"2026-07-17","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 1,900,900,000, latest = 1,900,900,000
  - original: `{"accn":"0000950170-25-095300","end":"2025-05-31","start":"2024-06-01","val":1900900000,"filed":"2025-07-11","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2025-05-31","start":"2024-06-01","val":1900900000,"filed":"2026-07-17","form":"10-K"}`

**FY2026 (period end 2026-05-31)**

- revenue (tag `RevenueFromContractWithCustomerExcludingAssessedTax`): original = 6,301,100,000, latest = 6,301,100,000
  - original: `{"accn":"0001193125-26-307785","end":"2026-05-31","start":"2025-06-01","val":6301100000,"filed":"2026-07-17","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2026-05-31","start":"2025-06-01","val":6301100000,"filed":"2026-07-17","form":"10-K"}`
- net income (tag `NetIncomeLoss`): original = 1,760,100,000, latest = 1,760,100,000
  - original: `{"accn":"0001193125-26-307785","end":"2026-05-31","start":"2025-06-01","val":1760100000,"filed":"2026-07-17","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2026-05-31","start":"2025-06-01","val":1760100000,"filed":"2026-07-17","form":"10-K"}`
- total assets (tag `Assets`): original = 16,174,500,000, latest = 16,174,500,000
  - original: `{"accn":"0001193125-26-307785","end":"2026-05-31","val":16174500000,"filed":"2026-07-17","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2026-05-31","val":16174500000,"filed":"2026-07-17","form":"10-K"}`
- total liabilities (tag `Liabilities`): original = 12,439,400,000, latest = 12,439,400,000
  - original: `{"accn":"0001193125-26-307785","end":"2026-05-31","val":12439400000,"filed":"2026-07-17","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2026-05-31","val":12439400000,"filed":"2026-07-17","form":"10-K"}`
- stockholders equity (tag `StockholdersEquity`): original = 3,735,100,000, latest = 3,735,100,000
  - original: `{"accn":"0001193125-26-307785","end":"2026-05-31","val":3735100000,"filed":"2026-07-17","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2026-05-31","val":3735100000,"filed":"2026-07-17","form":"10-K"}`
- operating cash flow (tag `NetCashProvidedByUsedInOperatingActivities`): original = 2,556,700,000, latest = 2,556,700,000
  - original: `{"accn":"0001193125-26-307785","end":"2026-05-31","start":"2025-06-01","val":2556700000,"filed":"2026-07-17","form":"10-K"}`
  - latest: `{"accn":"0001193125-26-307785","end":"2026-05-31","start":"2025-06-01","val":2556700000,"filed":"2026-07-17","form":"10-K"}`

### Raw excerpts — PULL 3

PULL 3 is byte-identical to PULL 2 (SHA-256 `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d` for both), verified — so
the PULL 2 excerpts above stand unchanged for PULL 3. Verified independently:
all 30 companyconcept files in `raw3/` are byte-identical to `raw2/`; the only
file that differs is `submissions-920760.json` (two 2015 accessions aged out of
Lennar's recent list), which carries no excerpted values.

## Files delivered with this report

- D1: this report (`sec-fin-five-more-report.md` at delivery time).
- D2: `sec-fin-five-more-pull1.csv` — 150 rows,
  SHA-256 `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d`.
- D3: `sec-fin-five-more-pull2.csv` — 150 rows,
  SHA-256 `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d`.
- D4: `sec-fin-five-more-pull3.csv` — 150 rows,
  SHA-256 `3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d`.

```synmerco-data
3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d sec-fin-five-more-pull1.csv
3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d sec-fin-five-more-pull2.csv
3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d sec-fin-five-more-pull3.csv
```

## Final checklist — completed before submitting

- [x] PULL 3 ran (19 Nov 11:40 WIB) and its progress note was filed
  (recordedAt 2026-11-19T04:43:06.217717Z, 24h05m after the PULL 2 note)
- [x] PULL 3 CSV/meta/proof read; rows + SHA-256 recorded in Changes and Files
- [x] Restatements re-checked on the PULL 3 CSV; confirmed unchanged (total still 4)
- [x] PULL 3 filings counts + new accessions table filled (none new; Lennar 1002 → 1000, two 2015 accessions aged out)
- [x] PULL 3 request table pasted into PROOF (47 requests)
- [x] PROOF excerpts re-pointed at the last good pull (PULL 3; raw3/ companyconcept files byte-identical to raw2/)
- [x] Per-company tables re-checked against the last good pull CSV (match exactly)
- [x] All PULL 3 placeholder markers removed
- [x] Report character count ≤ 2,000,000
- [x] Submit only at/after 2026-11-19T04:15:07Z and by 2026-11-21T12:15:07Z,
      declaring all three CSVs as data files first (declare → PUT → complete → verify)

---

*Final report prepared 2026-11-19 from PULL 1 (2026-11-17), PULL 2 (2026-11-18)
and PULL 3 (2026-11-19) files. All three CSVs are byte-identical
(SHA-256 3341328dd16783089f839d069af02b6000fc4568291f624ae8fd24812d000c3d).*
