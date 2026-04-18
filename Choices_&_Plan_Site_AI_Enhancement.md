# Choices & Plan Site AI Enhancement

> AI-powered AOP planning platform for 380+ product leaders at Deloitte Technology US — reducing per-WBS update time by 83% using Claude AI, Python, and SQL.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Claude AI](https://img.shields.io/badge/Claude%20AI-D97706?style=flat-square&logoColor=white)
![SharePoint](https://img.shields.io/badge/SharePoint-0078D4?style=flat-square&logo=microsoftsharepoint&logoColor=white)
![SAP HANA](https://img.shields.io/badge/SAP%20HANA-0FAAFF?style=flat-square&logo=sap&logoColor=white)
![Status](https://img.shields.io/badge/Status-Live%20at%20Deloitte-success?style=flat-square)

---

## What This Does

The Choices & Plan Site Enhancement is a SharePoint-hosted AOP (Annual Operating Plan) planning platform that uses Claude AI to read uploaded documents (SLAs, service agreements, tax agreements), extract key financial details, and auto-populate WBS descriptions, investment amounts, and cost center data.

Previously, each WBS entry took **60 minutes of manual effort**. This tool reduces it to **10 minutes** — an **83% reduction** — while also cutting overall process time by **60–70%**.

---

## Key Features

- **AI Document Reading:** Claude AI reads uploaded SLA, contract, and agreement documents and extracts key dates, amounts, and descriptions automatically
- **Drag-and-drop Excel upload:** Users upload plan data via Excel; the site parses and loads it automatically
- **Multi-platform sync:** On AOP completion, data pushes to QlikSense, SAP HANA, Anaplan, and Oracle via SQL
- **Division → Project → Product → Service Area hierarchy:** Full planning hierarchy supported
- **800+ users:** Product leaders, program owners, portfolio owners, and senior leaders across Deloitte Technology US

---

## Architecture

```
User Uploads (Excel / Word / PDF documents)
        |
        v
  SharePoint Server (Python + SQL backend)
        |
  Claude AI reads documents
  Extracts: dates, amounts, descriptions, WBS context
        |
        v
  Plan Site (Drag-and-drop UI)
  User reviews AI suggestions → Updates Cost Center + WBS
        |
        v
  SQL Integration Layer
        |
  ┌─────┬──────┬─────────┬────────┐
  ▼     ▼      ▼         ▼        ▼
QlikSense  SAP HANA  Anaplan  Oracle  (All platforms updated simultaneously)
```

---

## Impact Metrics

| Metric | Before | After |
|---|---|---|
| Time per WBS update | 60 minutes | 10 minutes |
| Time reduction | — | 83% |
| Overall process reduction | — | 60–70% |
| Users on platform | Fragmented across tools | 360+ on single platform |
| Data entry accuracy | Manual, error-prone | AI-validated |
| Platform integrations | Siloed | 4 platforms synced |

---

## Tools & Technologies

| Layer | Technology |
|---|---|
| AI Document Parser | Claude AI (Anthropic) |
| Backend | Python, SQL |
| Frontend / Hosting | SharePoint Server |
| Data Sources | SAP HANA, QlikSense, Anaplan, Oracle |
| Upload Format | Excel, Word, PDF |
| Integration | SQL push to all platforms on AOP close |

---

## User Workflow

```
1. Portfolio / product leader opens the Plan Site on SharePoint
2. Uploads baseline Excel or SLA document
3. Claude AI reads the document and suggests:
      - WBS description
      - Investment amount
      - Key dates and milestones
4. User reviews AI suggestions, updates Cost Center + WBS if needed
5. Submits → SQL pushes to all Deloitte analytics platforms
6. AOP is complete — all platforms reflect same plan data
```

---

## Project Context

Built and deployed within Deloitte Technology Finance. Standardised a previously fragmented multi-team AOP process into a single governed workflow. Presented as part of Deloitte's AI-in-Finance use cases.

> Note: All data in this repo uses anonymised sample data. Deloitte-specific configurations are confidential.

---

*Part of the [Sughosh Anney Finance × AI Portfolio](https://github.com/sughosh-anney)*
