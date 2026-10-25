# Exception Tracking & Seasonal Demand Analysis

A Python project that shows how to monitor a large product catalogue without reviewing it line by line: automated validation rules surface only the records that need attention, and seasonal forecasting shows when demand will peak.

**Scale:** 40,000+ SKUs across 120 categories, with daily changes.

**Data:** Simulated dataset built to mirror a large retail catalogue.

---

## The problem

When a catalogue changes every day, manual review doesn't scale. Errors and outliers (missing values, sudden jumps, records out of line with a benchmark) get missed, and planning teams don't see seasonal peaks early enough to prepare stock and budgets.

## What the project does

### 1. Data validation & exceptions queue
Rule-based checks in pandas flag:
- **Missing values** (e.g. blank prices)
- **Abnormal changes** greater than 20% day on day
- **Benchmark gaps**, where an item sits more than 5% above the comparison value

Flagged records are written to `exceptions_queue.csv`, so review effort goes only where it is needed.

**Result:** daily review scope reduced from ~40,000 SKUs to ~50 high-risk items (>99% reduction).

### 2. Index tracking against a benchmark
A monthly index (own value ÷ best benchmark value), aggregated at SKU and category level, highlights categories drifting out of line.

**Result:** flagged at-risk categories, e.g. Garden Tools with an index above 1.10.

### 3. Seasonal demand forecasting
Trend and seasonality decomposition with Holt-Winters (statsmodels) produces baseline demand forecasts and seasonal multipliers by category, to support stock and budget planning.

**Result:** projected demand peaks ahead of time, e.g. a December uplift.

### 4. Promotion impact analysis
Promotion windows are detected as month-on-month drops of 15% or more. Units sold before, during and after each window are compared to weigh volume uplift against margin impact.

**Result:** showed where extra volume did and did not justify the margin given up.

---

## Tech stack
- **Python:** pandas, numpy, matplotlib, statsmodels
- **Jupyter Notebook** for a reproducible ETL and analysis workflow
- **Star-schema outputs** designed to feed Power BI dashboards

## Files
| File | Purpose |
|---|---|
| `Pricing.ipynb` | Full workflow: validation, exceptions queue, index, forecasting, promotion analysis |
| `README.md` | This document |

## Next steps
- Add cost data (COGS) for accurate margin figures
- Extend Power BI dashboards with exception alerts and KPI tracking
- Add data-quality testing (e.g. Great Expectations) and scheduled runs

## License
MIT
