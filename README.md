# UK SME Balance Sheets and Filing Behaviour

Aggregate figures from **366,209 XBRL accounts** filed at Companies House,
covering balance sheet positions and filing timeliness for UK companies.

There is no published benchmark for what a small UK company's balance sheet
normally looks like, or for how filing behaviour relates to financial position.
This is both.

## Three findings

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

### 2. Companies in a weaker position file later

| | Negative net assets | Positive net assets |
|---|---|---|
| Median days to file | **261** | 250 |
| Filed after 9 months | **25.6%** | 19.9% |
| Filed after 12 months | **6.3%** | 3.6% |
| Filed within 6 months | 23.2% | **30.8%** |

Companies with negative net assets are **75% more likely to file more than a
year after their balance sheet date**. Late filing is a signal, and this
quantifies it.

### 3. Filing lateness is largely independent of size

Median days to file falls only modestly with size, from 251 days at zero
employees to 223 at 250+. The share filing more than nine months after their
balance sheet date sits between 17.7% and 21.9% across every band.

Larger companies file marginally sooner, but not dramatically so.

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
- Each field reports its own sample count, because not every company files every
  figure

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

**No sector breakdown.** SIC codes are not included in the filing data used
here.

## Files

| File | Contents |
|---|---|
| `uk_sme_balance_sheets_by_size.csv` | Net assets, cash, debtors, creditors, fixed and current assets by employee band, with quartiles |
| `uk_filing_timeliness_by_size.csv` | Days to file and lateness shares by employee band |
| `uk_filing_timeliness_by_balance_sheet_position.csv` | Filing behaviour split by positive and negative net assets |

## Licence

CC BY 4.0. Free to use, including commercially, with attribution.

The underlying filings are public data published by Companies House under the
Open Government Licence.

## Citation

> Edwards, P. (2026). *UK SME Balance Sheets and Filing Behaviour*.
> Finance Clearly.

## Corrections

If you find an error, please open an issue. Corrections are published with a
visible note rather than quietly fixed.

---

Compiled by Peter Edwards ACMA CGMA, a chartered management accountant, at
[Finance Clearly](https://financeclearly.com).
