# UK SME Balance Sheet Benchmarks by Company Size

Aggregate balance sheet figures for **300,940 UK companies**, computed from XBRL
accounts filed at Companies House and grouped by employee count.

There is no published benchmark for what a small UK company's balance sheet
normally looks like. This is that benchmark.

## Headline finding

**The proportion of companies with negative net assets falls steadily as
companies get larger.**

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
negative net assets. That halves by the time a company reaches fifty staff.

## What negative net assets means, and does not mean

Negative net assets means liabilities exceed assets on the balance sheet. It is
one indicator directors use when assessing whether a company can continue as a
going concern.

**It does not mean the company is failing.** Common benign explanations include
an overdrawn director's loan account, accumulated losses in an early-stage
company, and intra-group funding structures. Many of these companies trade
profitably and pay their debts as they fall due.

The figure is useful as a benchmark, not as a diagnosis.

## Method

- Source: XBRL accounts filed at Companies House, extracted from the public
  filing history
- 366,209 filings parsed; 300,940 with a usable employee count
- Restricted to balance sheet dates from 1 January 2025, so the figures describe
  current filings rather than a historical series
- Employee counts rounded to the nearest whole number before banding
- Medians and quartiles rather than means, because the distribution is heavily
  skewed by a small number of large balance sheets
- Each field reports its own sample count, because not every company files every
  figure. Cash and debtors in particular are absent from many micro-entity
  filings.

## Important limitations

**This is a cross-section, not a trend.** Filings before 2025 in the source data
are overwhelmingly late filings, which are an unrepresentative population. No
year-on-year comparison should be drawn from this dataset.

**Sample sizes vary enormously by field.** Net assets are present in 256,624
filings; cash in 89,138. Small-sample bands, particularly 250+, should be
treated with caution.

**Micro-entity filings are minimal by design.** Companies filing under FRS 105
report very little, which is why the 0 and 1 employee bands have the largest
gaps between total filings and populated fields.

**No sector breakdown.** SIC codes are not included in the filing data used
here.

## Files

- `uk_sme_balance_sheets_by_size.csv` — the aggregate table above, with
  quartiles and per-field sample counts

## Licence

CC BY 4.0. Free to use, including commercially, with attribution.

The underlying filings are public data published by Companies House under the
Open Government Licence.

## Citation

> Edwards, P. (2026). *UK SME Balance Sheet Benchmarks by Company Size*.
> Finance Clearly.

## Corrections

If you find an error, please open an issue. Corrections are published with a
visible note rather than quietly fixed.

---

Compiled by Peter Edwards ACMA CGMA, a chartered management accountant, at
[Finance Clearly](https://financeclearly.com).
