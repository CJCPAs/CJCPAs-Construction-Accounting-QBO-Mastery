# Construction Software Integrations

## Overview

QuickBooks Online integrates with many construction-specific software tools. This guide covers the most common integrations, setup procedures, and best practices for keeping your systems in sync.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Third-party integrations may change without notice. Consult with software vendors for current capabilities. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Integration Overview](#integration-overview)
2. [Project Management Integrations](#project-management-integrations)
3. [Time Tracking Integrations](#time-tracking-integrations)
4. [Estimating Software Integrations](#estimating-software-integrations)
5. [Payment Processing Integrations](#payment-processing-integrations)
6. [Document Management](#document-management)
7. [Data Import/Export Best Practices](#data-importexport-best-practices)
8. [Troubleshooting Integration Issues](#troubleshooting-integration-issues)

---

## Integration Overview

### QBO App Marketplace

```
Navigation: Apps → Find Apps (or apps.intuit.com)

┌─────────────────────────────────────────────────────────────────────────────┐
│                    QBO APP CATEGORIES FOR CONSTRUCTION                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PROJECT MANAGEMENT                                                          │
│  ├── Procore                                                                 │
│  ├── Buildertrend                                                            │
│  ├── CoConstruct                                                             │
│  ├── JobTread                                                                │
│  └── Foundation Software                                                     │
│                                                                              │
│  TIME TRACKING                                                               │
│  ├── QuickBooks Time (TSheets)                                              │
│  ├── Clockify                                                                │
│  ├── BusyBusy                                                                │
│  └── ExakTime                                                                │
│                                                                              │
│  ESTIMATING                                                                  │
│  ├── Buildxact                                                               │
│  ├── Clear Estimates                                                         │
│  ├── JobNimbus                                                               │
│  └── Stack                                                                   │
│                                                                              │
│  PAYMENTS                                                                    │
│  ├── QuickBooks Payments                                                    │
│  ├── PaySimple                                                               │
│  └── Bill.com                                                                │
│                                                                              │
│  DOCUMENT MANAGEMENT                                                         │
│  ├── SmartVault                                                              │
│  ├── Hubdoc                                                                  │
│  └── Receipt Bank (Dext)                                                     │
│                                                                              │
│  PAYROLL/HR                                                                  │
│  ├── QuickBooks Payroll                                                     │
│  ├── Gusto                                                                   │
│  └── ADP                                                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Integration Types

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TYPES OF INTEGRATIONS                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TYPE 1: NATIVE/DIRECT INTEGRATION                                           │
│  ──────────────────────────────────                                          │
│  • Built-in connection through QBO Apps marketplace                         │
│  • Usually two-way sync                                                      │
│  • Supported by both vendors                                                │
│  • Examples: QuickBooks Time, Procore, Buildertrend                         │
│                                                                              │
│  TYPE 2: THIRD-PARTY CONNECTOR                                               │
│  ─────────────────────────────                                               │
│  • Uses middleware like Zapier, Workato, or custom connector                │
│  • May have limitations or delays                                           │
│  • Examples: Many CRMs, specialized tools                                   │
│                                                                              │
│  TYPE 3: MANUAL EXPORT/IMPORT                                                │
│  ────────────────────────────                                                │
│  • Export from one system, import to QBO                                    │
│  • No real-time sync                                                         │
│  • Requires careful mapping and verification                                │
│  • Examples: Legacy software, unsupported tools                             │
│                                                                              │
│  TYPE 4: API INTEGRATION                                                     │
│  ───────────────────────                                                     │
│  • Custom development using QBO API                                         │
│  • Requires developer resources                                              │
│  • Fully customizable                                                        │
│  • Examples: Custom ERP connections                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Project Management Integrations

### Procore Integration

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PROCORE + QBO INTEGRATION                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT SYNCS:                                                                 │
│  ───────────                                                                 │
│  Procore → QBO:                                                              │
│  • Commitments (Subcontracts) → Bills                                       │
│  • Change Orders → Bill adjustments                                          │
│  • Invoices → Vendor bills                                                   │
│  • Budget line items                                                         │
│                                                                              │
│  QBO → Procore:                                                              │
│  • Vendors                                                                   │
│  • Payment status                                                            │
│  • Cost codes (with mapping)                                                │
│                                                                              │
│  SETUP STEPS:                                                                │
│  ─────────────                                                               │
│  1. In Procore: Go to Company Level → Admin → App Management                │
│  2. Find QuickBooks Online integration                                       │
│  3. Click Install/Configure                                                  │
│  4. Authenticate with QBO credentials                                        │
│  5. Map Cost Codes to QBO accounts                                          │
│  6. Map Vendors                                                              │
│  7. Configure sync settings                                                  │
│                                                                              │
│  BEST PRACTICES:                                                             │
│  ────────────────                                                            │
│  • Keep Procore as source of truth for job costs                            │
│  • QBO for accounting/financials                                            │
│  • Sync daily or more frequently                                            │
│  • Review sync log for errors                                               │
│  • Maintain consistent naming (vendors, cost codes)                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Buildertrend Integration

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BUILDERTREND + QBO INTEGRATION                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT SYNCS:                                                                 │
│  ───────────                                                                 │
│  Buildertrend → QBO:                                                         │
│  • Customer invoices                                                         │
│  • Customer payments                                                         │
│  • Purchase orders → Bills                                                  │
│  • Time entries                                                              │
│  • Expenses                                                                  │
│                                                                              │
│  QBO → Buildertrend:                                                         │
│  • Customers                                                                 │
│  • Vendors                                                                   │
│  • Chart of accounts                                                         │
│                                                                              │
│  SETUP STEPS:                                                                │
│  ─────────────                                                               │
│  1. In Buildertrend: Settings → Integrations                                │
│  2. Select QuickBooks Online                                                │
│  3. Connect and authenticate                                                 │
│  4. Map categories to QBO accounts                                          │
│  5. Configure sync preferences                                               │
│  6. Test with sample transaction                                            │
│                                                                              │
│  IDEAL FOR:                                                                  │
│  ───────────                                                                 │
│  • Residential builders                                                      │
│  • Remodelers                                                                │
│  • Custom home builders                                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### CoConstruct Integration

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COCONSTRUCT + QBO INTEGRATION                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT SYNCS:                                                                 │
│  ───────────                                                                 │
│  • Estimates and budgets                                                     │
│  • Change orders                                                             │
│  • Invoices                                                                  │
│  • Bills                                                                     │
│  • Time tracking                                                             │
│                                                                              │
│  KEY FEATURES:                                                               │
│  ─────────────                                                               │
│  • Two-way sync                                                              │
│  • Automatic invoice creation                                               │
│  • Budget-to-actual tracking                                                │
│  • Selection/allowance management                                           │
│                                                                              │
│  IDEAL FOR:                                                                  │
│  ───────────                                                                 │
│  • Custom home builders                                                      │
│  • Design-build firms                                                        │
│  • Remodelers with complex selections                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Integration Comparison

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PROJECT MANAGEMENT COMPARISON                             │
├───────────────┬──────────────┬──────────────┬──────────────┬───────────────┤
│               │   Procore    │ Buildertrend │  CoConstruct │   JobTread    │
├───────────────┼──────────────┼──────────────┼──────────────┼───────────────┤
│ Best For      │ Commercial   │ Residential  │ Custom Home  │ Trade Contrs  │
│               │ Large GCs    │ Remodelers   │ Design-Build │ Smaller firms │
├───────────────┼──────────────┼──────────────┼──────────────┼───────────────┤
│ QBO Sync      │ ✅ Native    │ ✅ Native    │ ✅ Native    │ ✅ Native     │
├───────────────┼──────────────┼──────────────┼──────────────┼───────────────┤
│ Two-Way       │ ✅           │ ✅           │ ✅           │ ✅            │
├───────────────┼──────────────┼──────────────┼──────────────┼───────────────┤
│ Price Range   │ $$$$         │ $$$          │ $$$          │ $$            │
├───────────────┼──────────────┼──────────────┼──────────────┼───────────────┤
│ Learning      │ High         │ Medium       │ Medium       │ Low           │
│ Curve         │              │              │              │               │
└───────────────┴──────────────┴──────────────┴──────────────┴───────────────┘
```

---

## Time Tracking Integrations

### QuickBooks Time (TSheets)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QUICKBOOKS TIME + QBO                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  This is the NATIVE time tracking solution owned by Intuit.                 │
│                                                                              │
│  FEATURES:                                                                   │
│  ─────────                                                                   │
│  • Mobile app for field workers                                              │
│  • GPS tracking and geofencing                                               │
│  • Photo clock-in                                                            │
│  • Job/customer/class assignment                                            │
│  • Overtime calculation                                                      │
│  • PTO tracking                                                              │
│  • Direct sync to QBO Payroll                                               │
│  • Scheduling                                                                │
│                                                                              │
│  SYNC DETAILS:                                                               │
│  ─────────────                                                               │
│  QB Time → QBO:                                                              │
│  • Time entries (hours, job, class)                                         │
│  • Employee data                                                             │
│  • Overtime calculations                                                     │
│                                                                              │
│  QBO → QB Time:                                                              │
│  • Customers/Jobs                                                            │
│  • Classes                                                                   │
│  • Service items                                                             │
│                                                                              │
│  SETUP:                                                                      │
│  ──────                                                                      │
│  1. Go to Apps → Find Apps → QuickBooks Time                                │
│  2. Subscribe and connect                                                    │
│  3. Sync customers and jobs                                                  │
│  4. Configure job costing settings                                          │
│  5. Invite employees to mobile app                                          │
│  6. Set up approval workflow                                                │
│                                                                              │
│  PRICING (2024):                                                             │
│  ─────────────                                                               │
│  • Premium: $10/mo + $8/user                                                │
│  • Elite: $20/mo + $10/user                                                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### BusyBusy (Construction-Specific)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BUSYBUSY + QBO                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Built specifically for construction, includes:                              │
│                                                                              │
│  FEATURES:                                                                   │
│  ─────────                                                                   │
│  • GPS time tracking                                                         │
│  • Facial recognition clock-in                                              │
│  • Equipment time tracking                                                   │
│  • Material tracking                                                         │
│  • Safety checklists                                                         │
│  • Field notes and photos                                                    │
│  • Cost code tracking                                                        │
│                                                                              │
│  SYNC TO QBO:                                                                │
│  ─────────────                                                               │
│  • Time entries with job coding                                              │
│  • Employee hours                                                            │
│  • Equipment hours                                                           │
│                                                                              │
│  IDEAL FOR:                                                                  │
│  ───────────                                                                 │
│  • Contractors wanting construction-specific features                       │
│  • Equipment tracking alongside time                                        │
│  • Field documentation needs                                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Estimating Software Integrations

### Buildxact

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BUILDXACT + QBO                                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Cloud-based estimating for residential builders                            │
│                                                                              │
│  SYNC CAPABILITIES:                                                          │
│  ──────────────────                                                          │
│  Buildxact → QBO:                                                            │
│  • Estimates (as QBO Estimates)                                             │
│  • Invoices                                                                  │
│  • Purchase orders                                                           │
│  • Supplier invoices                                                         │
│                                                                              │
│  QBO → Buildxact:                                                            │
│  • Customers                                                                 │
│  • Suppliers                                                                 │
│  • Chart of accounts                                                         │
│                                                                              │
│  WORKFLOW:                                                                   │
│  ─────────                                                                   │
│  1. Create estimate in Buildxact (with takeoffs)                            │
│  2. Win job - convert to project                                            │
│  3. Sync customer and estimate to QBO                                       │
│  4. Create invoices in Buildxact                                            │
│  5. Sync invoices to QBO for AR tracking                                    │
│  6. Bills/POs sync to QBO for AP                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Estimating Integration Best Practices

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ESTIMATING INTEGRATION TIPS                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. MAP COST CODES CORRECTLY                                                 │
│     • Estimating cost codes → QBO expense accounts                          │
│     • Use consistent structure                                               │
│     • Document mapping                                                       │
│                                                                              │
│  2. SYNC ESTIMATES, NOT JUST INVOICES                                        │
│     • Estimate in QBO = budget reference                                    │
│     • Compare actual vs estimate                                            │
│                                                                              │
│  3. HANDLE CHANGE ORDERS                                                     │
│     • Update estimate in estimating software                                │
│     • Sync revised contract value to QBO                                    │
│                                                                              │
│  4. VERIFY TOTALS                                                            │
│     • Monthly reconcile: Estimating total = QBO total                       │
│     • Check for sync errors                                                  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Payment Processing Integrations

### QuickBooks Payments

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QUICKBOOKS PAYMENTS                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Native payment processing within QBO                                        │
│                                                                              │
│  PAYMENT METHODS:                                                            │
│  ─────────────────                                                           │
│  • ACH/Bank Transfer: 1% (up to $10 max)                                    │
│  • Credit Card: 2.9% + $0.25                                                │
│  • Invoice payment link                                                      │
│  • Pay Now button on invoices                                               │
│                                                                              │
│  AUTOMATIC RECORDING:                                                        │
│  ────────────────────                                                        │
│  When customer pays via link:                                               │
│  • Payment recorded automatically                                            │
│  • Deposit created                                                           │
│  • Invoice marked paid                                                       │
│  • No manual entry needed                                                    │
│                                                                              │
│  CONSTRUCTION CONSIDERATION:                                                 │
│  ────────────────────────────                                                │
│  For large draws ($50,000+):                                                │
│  CC Fee (2.9%): $1,450+                                                     │
│  ACH Fee (1%): $500 (or $10 cap depending on plan)                         │
│                                                                              │
│  RECOMMENDATION: Use ACH for large payments,                                │
│  CC for small change orders/service calls                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Bill.com Integration

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BILL.COM + QBO                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  AP automation and approval workflow                                         │
│                                                                              │
│  FEATURES:                                                                   │
│  ─────────                                                                   │
│  • Receive bills electronically                                              │
│  • OCR scanning of paper bills                                               │
│  • Approval workflows                                                        │
│  • Payment scheduling                                                        │
│  • ACH and check payments                                                    │
│  • International payments                                                    │
│                                                                              │
│  SYNC WITH QBO:                                                              │
│  ──────────────                                                              │
│  • Bills sync to QBO                                                         │
│  • Payments sync to QBO                                                      │
│  • Vendor records sync                                                       │
│  • Chart of accounts sync                                                    │
│                                                                              │
│  IDEAL FOR:                                                                  │
│  ───────────                                                                 │
│  • Multi-person approval requirements                                       │
│  • High volume of bills                                                      │
│  • Remote teams                                                              │
│  • Audit trail needs                                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Document Management

### Receipt/Document Capture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DOCUMENT CAPTURE OPTIONS                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  QBO RECEIPT CAPTURE (Built-in)                                              │
│  ──────────────────────────────                                              │
│  • Mobile app photo capture                                                  │
│  • Email receipts to QBO                                                     │
│  • Basic OCR                                                                 │
│  • Attach to transactions                                                    │
│  • Included with QBO subscription                                           │
│                                                                              │
│  HUBDOC (Owned by Intuit)                                                   │
│  ──────────────────────────                                                  │
│  • Advanced document capture                                                 │
│  • Auto-fetch from vendors                                                   │
│  • OCR data extraction                                                       │
│  • Create QBO bills automatically                                           │
│  • Included with QBO subscription                                           │
│                                                                              │
│  DEXT (formerly Receipt Bank)                                               │
│  ─────────────────────────────                                               │
│  • Professional-grade capture                                                │
│  • Multi-currency                                                            │
│  • Approval workflows                                                        │
│  • Accountant tools                                                          │
│  • Additional subscription                                                   │
│                                                                              │
│  CONSTRUCTION USE:                                                           │
│  ─────────────────                                                           │
│  • Capture field receipts (material purchases)                              │
│  • Subcontractor invoices                                                    │
│  • Equipment receipts                                                        │
│  • Expense reports                                                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Document Storage

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DOCUMENT STORAGE OPTIONS                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  QBO ATTACHMENTS (Built-in)                                                  │
│  ──────────────────────────                                                  │
│  • Attach to any transaction                                                │
│  • Limited organization                                                      │
│  • Storage limits apply                                                      │
│                                                                              │
│  SMARTVAULT                                                                  │
│  ──────────                                                                  │
│  • Document management integration                                           │
│  • Client portal                                                             │
│  • Organized folders                                                         │
│  • Version control                                                           │
│                                                                              │
│  GOOGLE DRIVE / DROPBOX                                                      │
│  ─────────────────────────                                                   │
│  • Manual organization                                                       │
│  • Link files in QBO notes                                                   │
│  • No direct integration                                                     │
│                                                                              │
│  RECOMMENDED STRUCTURE:                                                      │
│  ──────────────────────                                                      │
│  /Jobs                                                                       │
│    /2024-001 Smith Residence                                                │
│      /Contract                                                               │
│      /Pay Applications                                                       │
│      /Lien Waivers                                                           │
│      /Insurance                                                              │
│      /Photos                                                                 │
│    /2024-002 Johnson Remodel                                                │
│      /...                                                                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Data Import/Export Best Practices

### Importing Data to QBO

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DATA IMPORT BEST PRACTICES                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT CAN BE IMPORTED:                                                       │
│  ─────────────────────                                                       │
│  • Chart of Accounts                                                         │
│  • Customers                                                                 │
│  • Vendors                                                                   │
│  • Products/Services                                                         │
│  • Bank transactions                                                         │
│  • Invoices                                                                  │
│  • Bills                                                                     │
│                                                                              │
│  Navigation: ⚙️ → Import Data → [Select type]                               │
│                                                                              │
│  IMPORT TIPS:                                                                │
│  ─────────────                                                               │
│  1. PREPARE DATA CAREFULLY                                                   │
│     • Clean up source data first                                            │
│     • Remove duplicates                                                      │
│     • Standardize naming                                                     │
│     • Verify formats (dates, numbers)                                       │
│                                                                              │
│  2. USE QBO TEMPLATES                                                        │
│     • Download sample file first                                            │
│     • Match column headers exactly                                          │
│     • Use proper field formats                                              │
│                                                                              │
│  3. IMPORT IN SMALL BATCHES                                                  │
│     • Start with 10-20 records                                              │
│     • Verify import success                                                  │
│     • Then import larger batches                                            │
│                                                                              │
│  4. VERIFY AFTER IMPORT                                                      │
│     • Run reports to confirm data                                           │
│     • Check totals match source                                             │
│     • Spot-check individual records                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Exporting Data from QBO

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DATA EXPORT OPTIONS                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  REPORT EXPORT:                                                              │
│  ──────────────                                                              │
│  From any report: Export → Excel or PDF                                     │
│                                                                              │
│  LIST EXPORT:                                                                │
│  ─────────────                                                               │
│  From list pages: Export (if available)                                     │
│                                                                              │
│  BULK EXPORT (QBO Advanced):                                                 │
│  ────────────────────────────                                                │
│  • Export all transactions                                                   │
│  • Custom date ranges                                                        │
│  • Multiple formats                                                          │
│                                                                              │
│  THIRD-PARTY EXPORT TOOLS:                                                   │
│  ──────────────────────────                                                  │
│  • SaasAnt (Transaction export)                                             │
│  • Transaction Pro (Bulk export)                                            │
│  • Zed Axis (Advanced export)                                               │
│                                                                              │
│  EXPORT USES:                                                                │
│  ─────────────                                                               │
│  • Backup data                                                               │
│  • Analysis in Excel                                                         │
│  • Share with CPA/Bonding                                                   │
│  • WIP schedule preparation                                                  │
│  • Custom reporting                                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Data Pitfalls

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INTEGRATION PITFALLS TO AVOID                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ❌ DUPLICATE RECORDS                                                        │
│     Cause: Syncing same record multiple times                               │
│     Prevention: Check for existing before import                            │
│     Fix: Merge duplicates in QBO                                            │
│                                                                              │
│  ❌ MISMATCHED ACCOUNTS                                                      │
│     Cause: Poor account mapping                                              │
│     Prevention: Document mapping, test first                                │
│     Fix: Reclassify transactions                                            │
│                                                                              │
│  ❌ MISSING CLASS/JOB                                                        │
│     Cause: Integration doesn't pass job info                                │
│     Prevention: Verify job fields sync                                      │
│     Fix: Manual class assignment                                            │
│                                                                              │
│  ❌ SYNC TIMING ISSUES                                                       │
│     Cause: Data changed in both systems                                     │
│     Prevention: Designate "source of truth"                                 │
│     Fix: Reconcile and re-sync                                              │
│                                                                              │
│  ❌ DATE FORMAT ERRORS                                                       │
│     Cause: Different date formats between systems                           │
│     Prevention: Standardize to MM/DD/YYYY                                   │
│     Fix: Correct in source data                                             │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Troubleshooting Integration Issues

### Common Problems and Solutions

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TROUBLESHOOTING GUIDE                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PROBLEM: Integration won't connect                                          │
│  ───────────────────────────────────                                         │
│  Steps:                                                                      │
│  1. Verify QBO login credentials                                            │
│  2. Check if connected in Apps → My Apps                                    │
│  3. Disconnect and reconnect                                                │
│  4. Clear browser cache                                                      │
│  5. Try different browser                                                    │
│  6. Contact app support                                                      │
│                                                                              │
│  PROBLEM: Data not syncing                                                   │
│  ─────────────────────────────                                               │
│  Steps:                                                                      │
│  1. Check sync status in app                                                │
│  2. Review error logs                                                        │
│  3. Verify field mapping                                                    │
│  4. Check for required fields                                               │
│  5. Force manual sync                                                        │
│  6. Check both system's data                                                │
│                                                                              │
│  PROBLEM: Duplicate entries                                                  │
│  ──────────────────────────                                                  │
│  Steps:                                                                      │
│  1. Stop sync immediately                                                    │
│  2. Identify duplicate records                                               │
│  3. Delete duplicates in QBO                                                │
│  4. Check app sync settings                                                 │
│  5. Re-enable with correct settings                                         │
│                                                                              │
│  PROBLEM: Incorrect amounts                                                  │
│  ──────────────────────────                                                  │
│  Steps:                                                                      │
│  1. Compare source to QBO                                                   │
│  2. Check for rounding differences                                          │
│  3. Verify tax handling                                                     │
│  4. Check currency settings                                                 │
│  5. Correct in source, re-sync                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Integration Health Check

```
MONTHLY INTEGRATION REVIEW:

□ Check each integration's sync status
□ Review error logs for past month
□ Reconcile totals between systems
□ Verify new items synced correctly
□ Test sample transactions end-to-end
□ Update mappings if COA changed
□ Check for software updates
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INTEGRATION QUICK REFERENCE                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TO FIND APPS:                                                               │
│  Apps → Find Apps (or apps.intuit.com)                                      │
│                                                                              │
│  TO VIEW CONNECTED APPS:                                                     │
│  Apps → My Apps                                                              │
│                                                                              │
│  TO DISCONNECT AN APP:                                                       │
│  Apps → My Apps → [App] → Settings → Disconnect                             │
│                                                                              │
│  TOP CONSTRUCTION INTEGRATIONS:                                              │
│  • Time Tracking: QuickBooks Time                                           │
│  • Project Mgmt: Procore, Buildertrend, CoConstruct                        │
│  • Payments: QuickBooks Payments                                            │
│  • Documents: Hubdoc (included)                                             │
│                                                                              │
│  BEFORE CONNECTING:                                                          │
│  • Document your requirements                                               │
│  • Map accounts and fields                                                  │
│  • Test with sample data                                                    │
│  • Train users on workflow                                                  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With integrations configured:
- [Time Tracking Guide](../workflows/03-time-tracking-payroll.md) - Detailed time setup
- [Recording Transactions](../basics/03-recording-transactions.md) - Transaction workflows
- [Reporting Guide](./01-essential-reports.md) - Using integrated data

---

*[Back to Main Guide](../../README.md)*
