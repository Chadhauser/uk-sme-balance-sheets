# UK SME Balance Sheets and Filing Behaviour

Aggregate figures from **366,209 XBRL accounts** filed at Companies House,
covering balance sheet positions, liquidity, working capital and filing
timeliness for UK companies.

There is no published benchmark for what a small UK company's balance sheet
normally looks like. This is that benchmark.

## Four findings

### 1. Negative net assets fall steadily with company size

| Employees | Companies | Negative net assets | Median net assets |
|---|---|---|---|
| 0 | 105,286 | **21.4%** | £2,374 |
| 1 | 87,391 | 20.8% | £3,674 |
| 2–4 | 76,240 | 18.6% | £11,230 |
| 5–9 | 16,887 | 15.9% | £49,615 |
| 10–19 | 8,421 | 13.7% | £150,329 |
| 20–49 | 4,821 | 10.8% | £415,274 |
| 50–249 | 1,670 | **9.7%** | £1,298,159 |
| 250+ | 224 | 10.2% | £2,893,842 |

More than one in five companies with no employees or a single employee has
negative net assets. That halves by fifty staff.

### 2. The textbook current ratio is wrong for UK SMEs

Standard guidance says a healthy current ratio is 2:1. The actual UK median is
nowhere near it.

| Employees | Median current ratio | Below 1.0 |
|---|---|---|
| 0 | 1.05 | **45.6%** |
| 1 | 1.20 | 39.8% |
| 2–4 | 1.27 | 38.0% |
| 5–9 | 1.39 | 33.4% |
| 10–19 | 1.49 | 29.2% |
| 20–49 | 1.55 | 26.8% |
| 50+ | **1.57** | 24.6% |

Nearly half of companies with no employees have current liabilities exceeding
current assets. Benchmarking a small company against 2:1 will mislead.

### 3. Growth converts cash into debtors

| Employees | Cash as % of current assets | Debtors as % |
|---|---|---|
| 1 | **63.1%** | 38.7% |
| 2–4 | 54.3% | 36.6% |
| 5–9 | 40.7% | 41.3% |
| 10–19 | 36.0% | 45.5% |
| 20–49 | 31.8% | 51.2% |
| 50+ | **23.7%** | **59.5%** |

A one-person company holds nearly two thirds of its current assets as cash. A
fifty-person company holds under a quarter, with most of the rest owed by
customers. This is why profitable businesses run short of cash as they scale.

### 4. Companies in a weaker position file later

| | Negative net assets | Positive net assets |
|---|---|---|
| Median days to file | **261** | 250 |
| Filed after 9 months | **25.6%** | 19.9% |
| Filed after 12 months | **6.3%** | 3.6% |
| Filed within 6 months | 23.2% | **30.8%** |

Companies with negative net assets are **75% more likely to file more than a
year after their balance sheet date**. Late filing is a signal, and this
quantifies it.

## What negative net assets means, and does not mean

Negative net assets means liabilities exceed assets on the balance sheet. It is
one indicator directors use when assessing whether a company can continue as a
going concern.

**It does not mean the company is failing.** Common benign explanations include
an overdrawn director's loan account, accumulated losses in an early-stage
company, and intra-group funding structures. Many of these companies trade
profitably and pay their debts as they fall due.

The figures are useful as a benchmark, not as a diagnosis.

## Method

- Source: XBRL accounts filed at Companies House, from the public filing history
- 366,209 filings parsed; 300,940 with a usable employee count
- Restricted to balance sheet dates from 1 January 2025, so the figures describe
  current filings rather than a historical series
- Employee counts rounded to the nearest whole number before banding
- Medians and quartiles rather than means, because the distribution is heavily
  skewed by a small number of large balance sheets
- Days to file measured as file date minus balance sheet date; filings with
  negative or implausible intervals excluded
- Ratios computed only where both components are present and the denominator is
  positive, which is why sample counts differ between tables

## Important limitations

**This is a cross-section, not a trend.** Filings before 2025 in the source data
are overwhelmingly late filings, an unrepresentative population. No year-on-year
comparison should be drawn from this dataset.

**Nine months is the statutory filing deadline for most private companies, but
not all.** First accounts, extended deadlines and public companies differ. The
figures describe interval from balance sheet date, not confirmed lateness
against each company's own deadline.

**Sample sizes vary enormously by field.** Net assets are present in 256,624
filings; cash in 89,138. The 250+ band has only 224 filings and should be
treated with caution.

**Micro-entity filings are minimal by design.** Companies filing under FRS 105
report very little, which is why the smallest bands have the largest gaps
between total filings and populated fields.

**The zero-employee band is mixed.** It contains dormant companies, holding
companies and companies whose only worker is an unpaid director, which is why it
sometimes behaves differently from the one-employee band.

**No sector breakdown.** SIC codes are not included in the filing data used
here.

## Files

| File | Contents |
|---|---|
| `uk_sme_balance_sheets_by_size.csv` | Net assets, cash, debtors, creditors, fixed and current assets by employee band, with quartiles |
| `uk_current_ratio_by_size.csv` | Current ratio quartiles and share below 1.0 |
| `uk_working_capital_composition_by_size.csv` | Cash and debtors as shares of current assets |
| `uk_filing_timeliness_by_size.csv` | Days to file and lateness shares by employee band |
| `uk_filing_timeliness_by_balance_sheet_position.csv` | Filing behaviour split by positive and negative net assets |

## Licence

CC BY 4.0. Free to use, including commercially, with attribution.

The underlying filings are public data published by Companies House under the
Open Government Licence v3.0.

## Citation

> Edwards, P. (2026). *UK SME Balance Sheets and Filing Behaviour*.
> Finance Clearly.

## Corrections

If you find an error, please open an issue. Corrections are published with a
visible note rather than quietly fixed.

---

Compiled by Peter Edwards ACMA CGMA, a chartered management accountant, at
[Finance Clearly](https://financeclearly.com).
