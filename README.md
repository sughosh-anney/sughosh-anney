# N8N Finance Automation Workflows

> 51 AI-driven automation workflows deployed across FP&A, P2P, and finance operations at Deloitte — built on N8N and Sidekick platform. Recognised with Deloitte's AI Integrated Award 2025.

![N8N](https://img.shields.io/badge/N8N-EA4B71?style=flat-square&logo=n8n&logoColor=white)
![GenAI](https://img.shields.io/badge/GenAI-0EA5E9?style=flat-square&logoColor=white)
![Power Automate](https://img.shields.io/badge/Power%20Automate-0066FF?style=flat-square&logo=microsoftpowerautomate&logoColor=white)
![Sidekick](https://img.shields.io/badge/Sidekick%20Platform-6D28D9?style=flat-square&logoColor=white)
![Award](https://img.shields.io/badge/Deloitte%20AI%20Award-2025-FFD700?style=flat-square)
![Status](https://img.shields.io/badge/Status-Deployed-success?style=flat-square)

---

## What This Does

This repository documents the design, structure, and logic of 51 AI-driven automation workflows built under Deloitte's US Guild Technology Program — deployed within Deloitte's internal Sidekick platform using N8N paid workflows.

These workflows automate repetitive finance processes across FP&A, P2P, and management reporting — reducing manual effort and enabling real-time finance operations at scale.

---

## Workflow Categories

### FP&A Automation
- Variance commentary trigger workflows (linked to Commentary Engine)
- Forecast submission reminder and validation workflows
- Budget vs actual alert workflows for leadership
- Period close checklist automation
- Executive MIS report generation triggers

### P2P Automation
- Invoice receipt and matching validation
- Vendor payment status notification workflows
- AP aging alert workflows
- Duplicate invoice detection triggers
- Accrual booking reminder workflows

### Management Reporting
- Dashboard refresh trigger workflows
- KPI threshold breach notifications to leadership
- Monthly and quarterly report distribution automation
- Data quality check workflows before report generation

### Finance Operations
- Headcount change alert workflows (linked to OPS Dashboard)
- Contract renewal notification workflows
- SLA breach alert automation
- Period-end task assignment workflows

---

## Tech Stack

| Component | Technology |
|---|---|
| Workflow Engine | N8N (paid workflows) |
| Deployment Platform | Sidekick (Deloitte internal) |
| AI Layer | GenAI, Claude AI |
| Supporting Automation | Power Automate |
| Trigger Sources | SAP HANA, QlikSense, SharePoint, Email |
| Notification Targets | Teams, Email, Dashboard alerts |

---

## Deployment Architecture

```
Trigger Sources
(SAP HANA · QlikSense · SharePoint · Email · Manual)
        |
        v
  N8N Workflow Engine (Sidekick Platform)
  ┌──────────────────────────────────┐
  │  51 Workflows across:            │
  │  · FP&A (variance, forecast)     │
  │  · P2P (invoice, AP, accruals)   │
  │  · Reporting (MIS, KPI alerts)   │
  │  · Ops (headcount, contracts)    │
  └──────────────────────────────────┘
        |
        v
  AI Processing Layer (GenAI / Claude AI)
        |
        v
  Output Actions
  (Teams Alerts · Email · Dashboard Updates · SAP Posting)
```

---

## Recognition

- **Deloitte AI Integrated Award — 2025** for this initiative
- Presented as part of the **Deloitte US Guild Program for Emerging Technologies**
- Led UAT deployment cycles and optimisation testing across all 51 workflows
- Delivered executive presentations on AI-driven financial transformation

---

## Sample Workflow Logic (Anonymised)

```
WORKFLOW: Monthly Variance Alert

TRIGGER: Period close date reached (SAP HANA signal)
  |
  STEP 1: Extract actuals vs plan data
  |
  STEP 2: Calculate variance % per service area
  |
  STEP 3: IF variance > threshold THEN
            → Send alert to Service Area lead via Teams
            → Trigger Commentary Engine (Python + Claude AI)
          ELSE
            → Log as within tolerance
  |
  STEP 4: Generate summary email to COO dashboard distribution list
  |
  END
```

> Note: Workflow logic shown uses anonymised structure. Deloitte-specific configurations, credentials, and data are confidential and not included in this repository.

---

*Part of the [Sughosh Anney Finance × AI Portfolio](https://github.com/sughosh-anney)*
