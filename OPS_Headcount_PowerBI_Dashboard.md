# OPS Headcount Power BI Dashboard

> Intelligent headcount tracking dashboard for Deloitte's Operations function — with automated notice-period flags, contract renewal alerts, and real-time forecasting priority signals. Reduced forecasting errors by ~80%.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=microsoftpowerbi&logoColor=black)
![SAP SQL](https://img.shields.io/badge/SAP%20SQL-0FAAFF?style=flat-square&logo=sap&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat-square&logoColor=black)
![Status](https://img.shields.io/badge/Status-Live%20at%20Deloitte-success?style=flat-square)

---

## What This Does

The OPS Headcount Power BI Dashboard tracks all internal and external OPS headcount across Deloitte — including internal labor, third-party contractors, sublet vendors, outsourcing vendors, and eco-partner vendors.

The dashboard automatically flags employees serving notice periods as **priority forecasting items**, alerting analysts to adjust forward-period headcount planning assumptions before the numbers go wrong.

---

## Key Features

- **Notice period detection:** Automatically highlights employees on notice with a priority flag — triggering analysts to reforecast that headcount slot
- **Multi-vendor tracking:** Covers internal labor, third-party contractors, sublet, outsourcing, and eco-partner vendor headcount in one view
- **Contract renewal alerts:** Flags contracts approaching expiry before renewal deadlines are missed
- **Exit interview tracking:** Shows whether exit interview has been completed for departing headcount
- **AOP & planning support:** Rate card provided by leadership is embedded — analysts adjust planning based on flagged changes
- **Forecast accuracy improvement:** ~80% reduction in headcount forecasting errors after deployment

---

## Headcount Categories Tracked

```
OPS Headcount
├── Internal Labor
│   └── Full-time employees, rates, grade, notice status
├── External / Third-Party
│   └── Contractor details, contract end dates, renewals
├── Sublet Vendors
│   └── Vendor name, deployed headcount, contract status
├── Outsourcing Vendors
│   └── Outsourced FTE count, SLA compliance
└── Eco-Partner Vendors
    └── Partner-deployed staff, engagement status
```

---

## Smart Alerts & Flags

| Alert Type | Trigger | Action Required |
|---|---|---|
| Notice Period Flag | Employee submits resignation | Reforecast that headcount slot |
| Contract Expiry Alert | Contract end date within 30 days | Initiate renewal or offboard |
| Exit Interview Pending | Employee exiting, interview not done | Schedule exit interview |
| Rate Card Change | Leadership updates rate card | Replan affected headcount cost |
| AOP Variance Flag | Actual headcount differs from AOP | Review and explain variance |

---

## Technical Build

### Data Source
- **SAP SQL** — primary data source for all headcount records

### Power BI Components
- **DAX measures** for notice-period detection, contract expiry countdown, and forecasting priority scoring
- **Conditional formatting** to visually highlight priority flags in red/amber/green
- **Drill-through pages** — from summary → vendor level → individual headcount record
- **Slicers** — filter by vendor type, cost center, service area, notice status, contract status

### DAX Sample Logic
```dax
Notice Period Flag = 
IF(
    [Resignation Date] <> BLANK() && [Last Working Day] >= TODAY(),
    "Priority - Reforecast",
    "Active"
)

Days to Contract Expiry = 
DATEDIFF(TODAY(), [Contract End Date], DAY)
```

---

## Impact Metrics

| Metric | Before | After |
|---|---|---|
| Headcount forecasting errors | High | ~80% reduction |
| Notice period visibility | Manual tracking | Automated flag |
| Contract renewal misses | Occasional | Near zero |
| Vendor types tracked | Separately | All in one view |
| AOP planning accuracy | Dependent on manual inputs | Real-time flag driven |

---

> Note: All data in this repo uses anonymised sample data. Deloitte headcount figures and vendor names are confidential.

---

*Part of the [Sughosh Anney Finance × AI Portfolio](https://github.com/sughosh-anney)*
