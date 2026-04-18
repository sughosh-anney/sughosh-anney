# Dynamic Portfolio Dashboard — Excel + VBA + PowerPoint

> Formula-driven, macro-based executive portfolio dashboard covering 18 investment portfolios — with automatic PowerPoint sync. Reduces report preparation from 3 hours to under 7 minutes.

![VBA](https://img.shields.io/badge/VBA-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![Excel](https://img.shields.io/badge/Advanced%20Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![SAP](https://img.shields.io/badge/SAP%20HANA-0FAAFF?style=flat-square&logo=sap&logoColor=white)
![QlikSense](https://img.shields.io/badge/QlikSense-009848?style=flat-square&logoColor=white)
![PowerPoint](https://img.shields.io/badge/PowerPoint-B7472A?style=flat-square&logo=microsoftpowerpoint&logoColor=white)
![Status](https://img.shields.io/badge/Status-Live%20at%20Deloitte-success?style=flat-square)

---

## What This Does

A fully formula-driven, macro-based executive portfolio dashboard built in Excel — with zero pivot tables. The dashboard auto-refreshes from SAP and QlikSense raw data and simultaneously updates a linked PowerPoint presentation ready for executive distribution.

Analysts previously spent **~3 hours** manually building this report each period. Now it takes **one click and 7 minutes**.

---

## Key Features

- **Zero pivot tables** — entirely built using Excel dynamic array functions: `SORT`, `UNIQUE`, `FILTER`, `OFFSET`, `COMBINE`
- **Full macro automation** — VBA handles data refresh, chart generation, and layout updates
- **18 portfolio views** — single dashboard switches between all 18 investment portfolios
- **10-year trend analysis** — historical trend lines built into every portfolio view
- **Auto-PPT sync** — linked PowerPoint template auto-populates on data refresh; analyst just downloads and sends
- **Multi-dimensional views:** Plan · Modified Plan · Actuals · Variances · WBS type · GL account · Cost center · Investment type · Account group
- **Microsoft Copilot integration** — notes and plan revisions enhanced via Copilot, reflected in dashboard immediately

---

## Dashboard Views

```
Portfolio Selector (dropdown)
    |
    ├── Summary View         → High-level actuals, plan, forecast, variance
    ├── Project Level        → Line-by-line project breakdown
    ├── Program Level        → Grouped programme summary
    ├── WBS Type View        → Capital vs Opex split
    ├── GL Account View      → General ledger dimension
    ├── Cost Center View     → Cost centre level breakdown
    ├── Investment Type View → Classification of spend
    ├── Trend View           → 10-year historical trend
    └── Variance Summary     → Actual vs Plan, Actual vs Forecast
```

---

## Technical Build

### Excel Functions Used (No Pivots)
```excel
=SORT(FILTER(data, criteria))          — Dynamic filtered views
=UNIQUE(range)                          — Dynamic dimension lists  
=OFFSET(ref, rows, cols, height, width) — Dynamic range references
=SUMIFS / AVERAGEIFS                    — Multi-condition aggregation
```

### VBA Macro Tasks
```vba
' On refresh:
1. Connect to SAP HANA / QlikSense data source
2. Load raw data to data sheet
3. Trigger formula recalculation
4. Refresh all charts and named ranges
5. Update PowerPoint linked objects
6. Format output for selected portfolio
7. Flag any data quality issues
```

---

## Impact Metrics

| Metric | Before | After |
|---|---|---|
| Report preparation time | ~3 hours | Under 7 minutes |
| Manual steps required | 15+ | 1 (click refresh) |
| Portfolios covered | Built separately | 18 in one dashboard |
| PPT preparation | Manual copy-paste | Auto-generated |
| Pivot tables | Multiple per report | Zero |
| Historical trend | Not consistently tracked | 10 years built-in |

---

## Data Sources

| Source | Data Provided |
|---|---|
| SAP HANA | Actuals, GL data, cost center postings |
| QlikSense | Consolidated reporting data |
| Excel Plan Sheet | Budget and modified plan inputs |
| Microsoft Copilot | Narrative note enhancement |

---

> Note: All data in this repo uses anonymised sample data. Deloitte-specific portfolio names, amounts, and configurations are confidential.

---

*Part of the [Sughosh Anney Finance × AI Portfolio](https://github.com/sughosh-anney)*
