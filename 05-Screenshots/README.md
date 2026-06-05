# 📸 05-Screenshots — CoreFinance360 Platform Evidence

> **Visual proof of a fully operational enterprise lending platform**  
> Screenshots taken directly from the live Salesforce Developer Edition org (`IND56 · Org ID: 00DNS00000r86g1`)

---

## 📋 What This Folder Contains

This folder provides direct visual evidence of the CoreFinance360 platform in operation — capturing the data model, automation architecture, security design, multi-currency configuration, live transaction data, dashboards, and the borrower portal.

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
├── 08-Experience-Cloud/            # CoreFinance Client Portal builder and screen flow embed
└── 09-Integrations/                # Named Credentials for simulated SMS and credit bureau
```

---

## 📁 Screenshot Index

### 01 · Data Model

| File | What It Shows |
|---|---|
| `SS-01_Object-Manager-Overview.png` | All 12 custom objects in Object Manager with API names |
| `SS-02_Financing-Package-Fields.png` | Full custom field list on the Financing Package object (180+ fields platform-wide) |
| `SS-03_Schema-Builder-Relationships.png` | Entity relationship diagram — Financing Package, Credit Facility, Borrowing Structure, Collateral, Covenant |
| `SS-04_Role-Hierarchy.png` | Full 17-role hierarchy expanded — from System Admin to Field Agent and Regulator View |

---

### 02 · Flow Architecture

| File | What It Shows |
|---|---|
| `SS-05_Flow-Manager-All-Flows.png` | All 27+ flows listed with Type and Active status |
| `SS-06_Currency-Cascade-Flow-Canvas.png` | Canvas view of the currency cascade flow — 5-flow chain that auto-sets currency on all linked objects |
| `SS-07_Stage-Gate-Flow-Decision-Logic.png` | Decision element in the Stage Gate flow — branch conditions for each Financing Package stage transition |
| `SS-08_Approval-Process-3-Level-Routing.png` | 3-level approval process on Financing Package (Ngozi ≤$500K · Kwame $500K–$2M · Fatima >$2M) |
| `SS-09_Covenant-Breach-Alert-Flow.png` | Covenant Breach Alert flow canvas — trigger on `Covenant_Status__c = Breached`, Task creation + email action |

---

### 03 · Validation Rules

| File | What It Shows |
|---|---|
| `SS-10_Validation-Rules-List.png` | All 8 active validation rules on the Financing Package object |
| `SS-11_Validation-Rule-Formula-Detail.png` | Formula editor view of the KYC compliance or exposure limit rule |

---

### 04 · Security Architecture

| File | What It Shows |
|---|---|
| `SS-12_Permission-Sets-List.png` | All 13 permission sets listed (granular access control by role) |
| `SS-13_Permission-Set-Object-Settings.png` | Object-level CRUD configuration inside one permission set (e.g., CF360 Senior Credit Officer) |

---

### 05 · Multi-Currency Configuration

| File | What It Shows |
|---|---|
| `SS-14_Currency-Settings-10-Currencies.png` | All 10 active currencies: USD, XOF, XAF, NGN, GHS, LRD, KES, RWF, CDF, EUR |

---

### 06 · Live Data

| File | What It Shows |
|---|---|
| `SS-15_Financing-Package-List-View.png` | Active deal pipeline — multiple records across countries, stages, and currencies |
| `SS-16_Financing-Package-Record-Detail.png` | Fully populated deal record — all field sections, related lists (Credit Facility, Collateral, Covenant, Loan Document, Credit Memo) |
| `SS-17_Risk-Score-Formula-Live.png` | Risk Score formula result on a live record — 5-dimension score (KYC 20 + Risk Level 30 + Sector 15 + Deal Size 15 + Customer Type 20) |
| `SS-18_Approval-History-On-Record.png` | Approval History related list on a Financing Package — steps, approvers, and status |

---

### 07 · Dashboards & Reports

| File | What It Shows |
|---|---|
| `SS-19_Portfolio-Dashboard-Overview.png` | CF360 Portfolio Dashboard — deal pipeline, risk distribution, approval status, and key metrics |
| `SS-20_Report-With-Live-Data.png` | Analytical report running with live data — multi-column, grouped, cross-object |

---

### 08 · Experience Cloud

| File | What It Shows |
|---|---|
| `SS-21_Experience-Cloud-Portal-Builder.png` | CoreFinance Client Portal home page in Experience Builder |
| `SS-22_Document-Upload-Flow-Embedded.png` | CF360 Document Upload Screen Flow embedded in the borrower portal page |

---

### 09 · Integrations

| File | What It Shows |
|---|---|
| `SS-23_Named-Credentials-SMS-Gateway.png` | CF360 SMS Gateway Named Credential — URL, authentication protocol, security configuration |

---

## 🔍 What These Screenshots Prove

| Capability | Evidence |
|---|---|
| **Object-Oriented Data Modeling** | 12 custom objects with 180+ fields, visible relationships in Schema Builder |
| **Advanced Flow Automation** | 27+ flows across Record-Triggered, Screen, and Scheduled types |
| **Multi-Currency Architecture** | 10-currency system auto-cascaded across 6 object layers via 5 flows — zero manual selection |
| **Enterprise Security Design** | 17-role hierarchy, 13 permission sets, object- and field-level access control |
| **Credit Governance** | 8 validation rules, 3 multi-level approval processes, covenant monitoring |
| **Risk Scoring Engine** | 100-point formula-based score across 5 weighted dimensions |
| **Borrower Self-Service Portal** | Experience Cloud site with embedded screen flows for document upload and loan status |
| **Analytics & Reporting** | 4 dashboards, 10 reports, 5 custom report types — all running on live data |
| **Integration Architecture** | Named Credentials + simulated SMS/credit bureau callout flows |

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
