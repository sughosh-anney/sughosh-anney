# Variance Analysis Dashboard with Commentary Engine LLM

> AI-powered FP&A commentary generator using Claude AI — reducing variance analysis time from 45 minutes to 2 minutes per service area.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Claude AI](https://img.shields.io/badge/Claude%20AI-D97706?style=flat-square&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=microsoftpowerbi&logoColor=black)
![SAP HANA](https://img.shields.io/badge/SAP%20HANA-0FAAFF?style=flat-square&logo=sap&logoColor=white)
![Status](https://img.shields.io/badge/Status-Live%20at%20Deloitte-success?style=flat-square)

---

## What This Does

The Variance Analysis Commentary Engine is an LLM-powered FP&A dashboard that automatically generates narrative business commentary explaining financial variances — across service areas, business units, and time periods.

Finance analysts previously spent **45 minutes per service area** manually writing variance commentary. This tool reduces that to **under 2 minutes** — a **97% time reduction**.

---

## Key Features

- Pulls actuals, plan, and forecast data from SAP HANA and QlikSense
- Calculates three variance dimensions automatically:
  - Actual vs Plan
  - Actual vs Forecast
  - Plan vs Forecast
- Sends variance data to **Claude AI (Anthropic)** which generates structured, readable business commentary
- Covers **16 service areas**, **2 business units** and **4 Member Firms** — monthly and quarterly cadence
- Used by **220+ finance users and executive leadership** monthly
- Human-in-the-loop: analysts validate and refine AI commentary for business context

---

## Architecture

```
SAP HANA / QlikSense
        |
        v
  Python Data Layer
  (Extract, Transform, Calculate Variances)
        |
        v
  Claude AI (Anthropic API)
  (Generate narrative commentary per service area)
        |
        v
  Power BI Dashboard
  (Actuals | Plan | Forecast | Variance tables)
        |
        v
  Executive Review & Sign-off
```

---

## Impact Metrics

| Metric | Before | After |
|---|---|---|
| Time per service area commentary | 45 minutes | 2 minutes |
| Time reduction | — | 97% |
| Monthly active users | — | 220+ |
| Service areas covered | — | 16 |
| Business units | — | 2 |
| Member Firms | — | 4 |
| Reporting cadence | Manual, irregular | Monthly + Quarterly |

---

## Tools & Technologies

| Layer | Technology |
|---|---|
| AI Commentary Engine | Claude AI (Anthropic) |
| Data Extraction | Python (Pandas, SQLAlchemy) |
| Data Sources | SAP HANA, QlikSense |
| Dashboard | Power BI |
| Variance Calculation | Python |

---

## Sample Output Structure

The engine generates commentary in this format for each service area:

```
Service Area: [CXO]
Period: [Month - Period 07]

Actual vs Plan:
Revenue is above plan by 3.337% driven by higher-than-expected volume growth and improved realization rates across key service lines. The upside was supported by strong client demand, ramp-up of new projects, and better billing efficiency, partially offset by minor delays in a few planned engagements..
Cost variance of +2.10% reflects incremental resource deployment to support higher delivery volumes, including increased contractor utilization and selective backfills, along with timing of certain operating expenses initially planned for later periods. Overall, cost increase remains largely aligned with revenue outperformance, indicating controlled spend.

Actual vs Forecast:
Performance vs forecast shows a favorable variance, with revenue exceeding expectations due to stronger execution in key accounts and accelerated project milestones achieved within the period.
On the cost side, slightly higher-than-forecasted expenses were observed, primarily due to unplanned resource ramp-up and short-term contractor dependencies to meet delivery timelines. However, cost discipline across discretionary spends helped partially offset these increases, resulting in stable margin delivery versus forecast.

Outlook:
Based on current trends, revenue momentum is expected to sustain in the near term, supported by a healthy pipeline and continued strength in client demand. However, margin expansion may remain moderate, as ongoing investments in capacity building and project delivery could continue to exert pressure on costs.
Focus will remain on optimizing resource mix, improving utilization, and driving operational efficiencies to balance growth with profitability in the upcoming periods.
```

> Note: All data shown in this repo uses anonymised sample data. Deloitte-specific figures are confidential.

---

## Project Context

Built at Deloitte as part of the FP&A Technology Finance team. Presented as a Generative AI use case within Deloitte's US Guild Program for Emerging Technologies.

---

*Part of the [Sughosh Anney Finance × AI Portfolio](https://github.com/sughosh-anney)*
