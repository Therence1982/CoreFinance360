# 📸 05-Screenshots — CoreFinance360 Platform Evidence

> **Visual proof of a fully operational enterprise lending platform**  
> Screenshots taken directly from the live Salesforce Developer Edition org (`IND56 · Org ID: 00DNS00000r86g1`)

---

## 📋 What This Folder Contains

This folder provides direct visual evidence of the CoreFinance360 platform in operation — capturing the data model, automation architecture, security design, multi-currency configuration, live transaction data, dashboards, and integration setup.

All screenshots were captured from the live org. No mockups. No staging data.

---

## 🗂️ Folder Structure

```
05-Screenshots/
├── 01-Data-Model/                  # Object architecture, fields, schema, role hierarchy
├── 02-Flow-Architecture/           # Flow manager, canvas views, stage gates, approvals
├── 03-Validation-Rules/            # Validation rule list and formula detail
├── 04-Security-Architecture/       # Permission sets, object-level access configuration
├── 05-Multi-Currency/              # 10-currency setup (XOF, XAF, NGN, GHS, KES, and more)
├── 06-Live-Data/                   # Active records, populated deal data, approval history
├── 07-Dashboards-Reports/          # Portfolio dashboards, analytical reports with live data
└── 09-Integrations/                # Named Credentials for SMS gateway integration
```

---

## 📁 Screenshot Index

### 01 · Data Model

| File | What It Shows |
|---|---|
| `SS-01_Object-Manager-Overview.png` | All 10 custom objects in Object Manager — API names, descriptions, deployed status |
| `SS-02a_Financing-Package-Fields.png` | Full field list on Financing Package — Risk Score formula, Stage, Currency, Total Amount |
| `SS-02b_Credit-Facility-Fields.png` | Full field list on Credit Facility — Loan Amount, Interest Rate, Maturity Date, Master-Detail relationship |
| `SS-03_Schema-Builder-Relationships.png` | Entity relationship diagram — Financing Package, Credit Facility, Borrowing Structure, Collateral, Covenant, Loan Document with relationship lines |
| `SS-04_Role-Hierarchy.png` | Full 18-role hierarchy expanded — CoreFinance360 Executive down to Mobile Money Agent, Microfinance Officer, Regulator View |

---

### 02 · Flow Architecture

| File | What It Shows |
|---|---|
| `SS-05_Flow-Manager-All-Flows.png` | All 50+ flows listed with Process Type and Active status |
| `SS-06a_Currency-Cascade-Collateral.png` | Currency cascade — Collateral inherits currency from Financing Package automatically |
| `SS-06b_Currency-Cascade-Credit-Facility.png` | Currency cascade — Credit Facility inherits currency from Financing Package |
| `SS-06c_Currency-Cascade-Opportunity.png` | Currency cascade — Opportunity inherits currency from Account |
| `SS-06d_Currency-Cascade-Account.png` | Currency cascade — selecting a country auto-sets currency on Account (Fast Field Updates) |
| `SS-07_Stage-Gate-Block-Underwriting.png` | Stage gate — Decision element blocking Underwriting without Credit Facility |
| `SS-07b_Block-Credit-Review-Without-Credit-Memo.png` | Stage gate — Decision element blocking Credit Review without Credit Memo |
| `SS-07c_Create-Underwriting-Tasks-Flow.png` | 3 tasks auto-created + email alert when deal enters Underwriting stage |
| `SS-07d_Create-Credit-Review-Tasks-Flow.png` | 2 tasks auto-created + email alert when deal enters Credit Review stage |
| `SS-07e_Create-Approval-Tasks-Flow.png` | 2 approval tasks auto-created when deal enters approval stage |
| `SS-08_Approval-Process-3-Level-Routing.png` | Financing Package approval — 3 levels: Credit Officer ≤$500K · CRO $500K–$2M · CFO >$2M |
| `SS-08b_Credit-Memo-Approval-Process.png` | Credit Memo approval — 3-level routing with criteria and assigned approvers |
| `SS-08c_Credit-Exception-Approval-Process.png` | Credit Exception approval — single level review by System Administrator |
| `SS-09_Covenant-Breach-Alert-Flow.png` | Covenant Breach Alert — triggered on Covenant update, creates task + sends email |

---

### 03 · Validation Rules

| File | What It Shows |
|---|---|
| `SS-10_Validation-Rules-List.png` | All 5 validation rules on Financing Package — bilingual error messages (EN + FR) |
| `SS-10b_Account-Validation-Rule-KYC.png` | Account KYC rule — Tax ID required before KYC Status can be set to Verified |
| `SS-10c_Covenant-Validation-Rules.png` | Covenant rule — Breach Date required when Covenant Status is set to Breached |
| `SS-10e_Credit-Facility-Validation-Rules.png` | Credit Facility rule — Outstanding Balance cannot exceed Loan Amount (bilingual) |
| `SS-11_Validation-Rule-Formula-Detail.png` | Exposure Limit Breach Check formula — AND logic with PRIORVALUE, cross-object reference, BCEAO/CEMAC compliance |

---

### 04 · Security Architecture

| File | What It Shows |
|---|---|
| `SS-12_Permission-Sets-List.png` | All 13 CF360 permission sets — Admin, Approval Levels 1/2/3, Auditor, Core Lending, Credit Analysis, Disbursement, Document Management, KYC Management, Portfolio Monitoring, Regulator |
| `SS-12b_Permission-Set-Groups-List.png` | All 16 CF360 permission set groups — one per role from Branch Manager to System Administrator |
| `SS-13_Permission-Set-Object-Settings.png` | Object-level CRUD access configuration inside CF360 Credit Analysis permission set |

---

### 05 · Multi-Currency Configuration

| File | What It Shows |
|---|---|
| `SS-14_Currency-Settings-10-Currencies.png` | All 10 active currencies with conversion rates — USD, XOF, XAF, NGN, GHS, LRD, KES, RWF, CDF, EUR |

---

### 06 · Live Data

| File | What It Shows |
|---|---|
| `SS-16_Financing-Package-Record-Detail.png` | Live FP-0025 record — Stage path bar, Account, Total Amount with USD conversion, Risk Score calculating, Currency, Purpose |
| `SS-16b_Financing-Package-Related-Lists.png` | All related lists on a Financing Package — Credit Facility, Borrowing Structure, Collateral, Loan Document, Credit Memos, Covenants, Credit Exceptions, Credit Committee Meetings, Audit Logs, Approval History |
| `SS-17_Risk-Score-Formula-Live.png` | Risk Score tooltip on live record showing scoring legend — 80-100 Excellent · 60-79 Good · 40-59 Moderate · 20-39 High Risk · 0-19 Very High Risk |
| `SS-18_Approval-History-On-Record.png` | Approval History related list on a Financing Package record |

---

### 07 · Dashboards & Reports

| File | What It Shows |
|---|---|
| `SS-19_Portfolio-Dashboard-Overview.png` | Portfolio Manager Dashboard — Pipeline by Stage, Active Packages by Account, Covenant Compliance, KYC Status charts |
| `SS-19a_Dashboard-List-View.png` | All 4 CF360 dashboards listed — Portfolio Manager, Credit Officer, Compliance, Regulator |
| `SS-19b_Credit-Officer-Dashboard.png` | Credit Officer Dashboard — Breached Covenants, Credit Exception Register, Audit Log by Event Type |
| `SS-19c_Compliance-Dashboard.png` | Compliance Dashboard — Expiring Documents, KYC Status, Covenant Compliance, Audit Log |
| `SS-20a_Reports-List-View.png` | All 10 CF360 reports listed with descriptions — Covenant Compliance, Pipeline by Stage, KYC Status, Approval Pipeline, and more |
| `SS-20_Report-With-Live-Data.png` | Analytical report running with live data |

---

### 08 · Integrations

| File | What It Shows |
|---|---|
| `SS-23_Named-Credentials-SMS-Gateway.png` | CF360 SMS Gateway Named Credential list — Secured Endpoint, Africa's Talking API URL |
| `SS-23b_Named-Credentials-SMS-Gateway-Detail.png` | CF360 SMS Gateway detail — Label, URL, Authentication, Callout Options configuration |

---

## 🔍 What These Screenshots Prove

| Capability | Evidence |
|---|---|
| **Object-Oriented Data Modeling** | 10 custom objects with 180+ fields platform-wide, visible relationships in Schema Builder |
| **Advanced Flow Automation** | 50+ flows across Record-Triggered, Screen, and Scheduled types |
| **Multi-Currency Architecture** | 10-currency system auto-cascaded across 6 object layers via 5 flows — zero manual selection |
| **Enterprise Security Design** | 18-role hierarchy, 13 permission sets, 16 permission set groups, object-level access control |
| **Credit Governance** | 8 validation rules across 4 objects, 3 multi-level approval processes, covenant monitoring |
| **Risk Scoring Engine** | Formula-based score with live tooltip showing 5-tier scoring legend |
| **Stage Gate Enforcement** | Flows blocking stage transitions without required related records |
| **Analytics & Reporting** | 4 dashboards, 10 reports — all running on live data |
| **Integration Architecture** | Named Credentials pointing to Africa's Talking SMS API — real African market integration |
| **Bilingual Platform** | Validation rule error messages in English and French — BCEAO/CEMAC compliance |

---

## 🌍 Market Context

CoreFinance360 was designed for banking institutions operating across **11 BCEAO/CEMAC and anglophone African markets**:

`Senegal` · `Ivory Coast` · `Mali` · `Burkina Faso` · `Cameroon` · `Congo` · `Nigeria` · `Ghana` · `Kenya` · `Rwanda` · `Liberia`

The platform handles formal and **informal-sector borrowers** — including alternative credit scoring based on mobile money history, utility payment records, and market association membership.

---

## 📎 Related Documentation

| Document | Location |
|---|---|
| Architecture Documentation (Live Site) | [GitHub Pages →](https://therence1982.github.io/CoreFinance360/CF360_Architecture_Documentation.html) |
| Master Project Summary (EN + FR) | [`01-Project-Summary/`](../01-Project-Summary/) |
| Salesforce Configuration Reference (EN + FR) | [`07-Salesforce-Configuration/`](../07-Salesforce-Configuration/) |
| Testing Guide — 10 Scenarios, 10 Countries (EN + FR) | [`03-Testing-Guide/`](../03-Testing-Guide/) |
| Demo Presentations — 20 Slide Decks (EN + FR) | [`04-Presentations/`](../04-Presentations/) |

---

*CoreFinance360 · Built on Salesforce Developer Edition · 100% Declarative · No Apex · All layers active*
