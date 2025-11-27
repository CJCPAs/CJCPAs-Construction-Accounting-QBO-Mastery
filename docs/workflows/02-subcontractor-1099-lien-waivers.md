# Subcontractor Management: 1099s and Lien Waivers

## Overview

Subcontractor management is one of the most critical aspects of construction accounting. This guide covers vendor setup for subs, the complete 1099 compliance workflow, and lien waiver tracking—all within QuickBooks Online.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Tax laws and lien requirements vary by state. Consult with a qualified CPA and attorney before implementing. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Subcontractor vs. Employee](#subcontractor-vs-employee)
2. [Setting Up Subcontractors in QBO](#setting-up-subcontractors-in-qbo)
3. [The Complete 1099 Workflow](#the-complete-1099-workflow)
4. [Tracking Subcontractor Compliance](#tracking-subcontractor-compliance)
5. [Lien Waiver Management](#lien-waiver-management)
6. [Pay Application Processing](#pay-application-processing)
7. [Insurance Certificate Tracking](#insurance-certificate-tracking)
8. [Best Practices and Common Mistakes](#best-practices-and-common-mistakes)

---

## Subcontractor vs. Employee

### Why Classification Matters

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MISCLASSIFICATION RISKS                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Treating an EMPLOYEE as a SUBCONTRACTOR can result in:                     │
│                                                                              │
│  IRS Penalties:                                                              │
│  • 100% of employee's FICA (employer + employee portions)                   │
│  • 100% of federal income tax withholding                                   │
│  • Penalties up to 40% of unreported wages                                  │
│  • Interest on all amounts                                                   │
│                                                                              │
│  State Penalties:                                                            │
│  • State tax withholding                                                     │
│  • Unemployment insurance                                                    │
│  • Workers' comp premium back charges                                        │
│  • Potential criminal charges in some states                                │
│                                                                              │
│  Example: $50,000 misclassified worker                                       │
│  ─────────────────────────────────────────────────────────────────────────  │
│  FICA (15.3%):                    $7,650                                    │
│  Federal withholding (est 22%):   $11,000                                   │
│  State withholding (est 5%):      $2,500                                    │
│  Penalty (35%):                   $17,500                                   │
│  Interest (est):                  $2,000                                    │
│  ─────────────────────────────────────────────────────────────────────────  │
│  TOTAL EXPOSURE:                  $40,650+                                  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### IRS Classification Factors

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    EMPLOYEE VS. SUBCONTRACTOR                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  FACTOR               │  EMPLOYEE           │  SUBCONTRACTOR                │
│  ─────────────────────┼─────────────────────┼──────────────────────────────│
│  Who controls HOW     │  Company directs    │  Sub controls their          │
│  work is done?        │  methods            │  own methods                  │
│                       │                     │                               │
│  Who provides tools/  │  Company provides   │  Sub provides own            │
│  equipment?           │                     │                               │
│                       │                     │                               │
│  Can work for others? │  Generally no       │  Yes, has multiple           │
│                       │                     │  customers                    │
│                       │                     │                               │
│  Set work hours?      │  Company sets       │  Sub sets own hours          │
│                       │  schedule           │                               │
│                       │                     │                               │
│  Paid how?            │  Hourly/salary      │  Per job/contract            │
│                       │  regularly          │                               │
│                       │                     │                               │
│  Risk of loss?        │  Company bears      │  Sub can profit or           │
│                       │  risk               │  lose on job                  │
│                       │                     │                               │
│  Business entity?     │  Individual         │  Often LLC/Corp              │
│                       │                     │                               │
│  Own insurance?       │  No                 │  Yes, GL and WC              │
│                       │                     │                               │
│                                                                              │
│  ⚠️ No single factor is determinative—IRS looks at the total relationship  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Safe Harbor for Subcontractors

```
To support subcontractor classification:

✅ Written subcontract agreement
✅ W-9 on file with EIN or SSN
✅ Sub has own business entity (LLC, Corp)
✅ Sub has own general liability insurance
✅ Sub has own workers' compensation (or valid exemption)
✅ Sub provides own tools and equipment
✅ Sub controls their workers and methods
✅ Sub can work for other contractors
✅ Sub invoices for completed work
✅ No withholding from payments
```

---

## Setting Up Subcontractors in QBO

### Step-by-Step: Create Subcontractor Vendor

**Step 1: Navigate to Vendors**

```
Navigation: Expenses → Vendors → New Vendor
```

**Step 2: Enter Basic Information**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  NEW VENDOR                                                   [Save] [X]    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Company: ABC Electrical Services, LLC                                       │
│  └── Use legal business name (as on W-9)                                    │
│                                                                              │
│  Display name as: ABC Electric - Smith, John                                 │
│  └── Optional: Add owner name for easy identification                       │
│                                                                              │
│  Print on check as: ABC Electrical Services, LLC                            │
│  └── Must match legal name for check cashing                                │
│                                                                              │
│  Address:                                                                    │
│  123 Contractor Lane                                                         │
│  Anytown, ST 12345                                                           │
│  └── Use address from W-9                                                   │
│                                                                              │
│  Email: john@abcelectric.com                                                 │
│  Phone: (555) 234-5678                                                       │
│  Mobile: (555) 345-6789                                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Step 3: Enter Tax Information (Critical!)**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  TAX INFO TAB                                                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Tax ID: [XX-XXXXXXX]                                                        │
│  └── Enter EIN or SSN from W-9                                              │
│      EIN format: XX-XXXXXXX                                                 │
│      SSN format: XXX-XX-XXXX                                                │
│                                                                              │
│  ☑️ Track payments for 1099                                                 │
│  └── CRITICAL: Must be checked for 1099 reporting!                          │
│                                                                              │
│  Business ID type:                                                           │
│  ○ EIN (Employer Identification Number)                                     │
│  ○ SSN (Social Security Number)                                             │
│  └── Select based on W-9 provided                                           │
│                                                                              │
│  Default expense account: 50200 - Subcontractor Costs                       │
│  └── Pre-fills on bills for this vendor                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Step 4: Add Custom Fields**

```
If you've created custom fields for vendors:

Trade: [Electrical ▼]
Options: Electrical, Plumbing, HVAC, Framing, Concrete, Roofing, etc.

Insurance Expiration: [12/31/2024]

License Number: [ELEC-12345]
```

**Step 5: Add Additional Information**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  ADDITIONAL INFO TAB                                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Account #: [Your account number with vendor, if any]                       │
│                                                                              │
│  Payment terms: [Net 30 ▼]                                                  │
│  └── Per your subcontract agreement                                         │
│                                                                              │
│  Opening balance: [Leave at $0]                                              │
│  └── Enter via bill if there's existing balance                             │
│                                                                              │
│  Attachments:                                                                │
│  └── Attach: W-9, Insurance cert, License, Subcontract                      │
│                                                                              │
│  Notes:                                                                      │
│  └── "Preferred electrical sub. Has done Smith, Johnson, Martinez jobs."    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Vendor Categories/Groups

Organize subcontractors for easy filtering:

```
Consider creating vendor categories in notes or custom fields:

TRADE CATEGORIES:
├── Electrical
├── Plumbing
├── HVAC
├── Framing
├── Concrete/Masonry
├── Roofing
├── Drywall/Paint
├── Flooring
├── Landscaping
├── Site Work
└── General Labor
```

---

## The Complete 1099 Workflow

### Annual 1099 Calendar

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    1099 ANNUAL CALENDAR                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  THROUGHOUT YEAR:                                                            │
│  • Collect W-9 before first payment                                          │
│  • Verify TIN matches W-9                                                    │
│  • Check "Track payments for 1099" on vendor                                │
│  • Record payments accurately by vendor                                      │
│                                                                              │
│  NOVEMBER - DECEMBER:                                                        │
│  • Review 1099 vendor list                                                   │
│  • Verify contact information                                                │
│  • Update missing W-9s                                                       │
│  • Verify TINs (consider TIN matching)                                      │
│                                                                              │
│  JANUARY 1-15:                                                               │
│  • Close prior year books                                                    │
│  • Run 1099 report in QBO                                                   │
│  • Review for accuracy                                                       │
│  • Verify $600+ threshold by vendor                                         │
│                                                                              │
│  JANUARY 31:                                                                 │
│  • File 1099-NEC with IRS                                                   │
│  • Furnish copies to vendors                                                 │
│  • ⚠️ DEADLINE - Penalties for late filing!                                │
│                                                                              │
│  FEBRUARY - MARCH:                                                           │
│  • Respond to vendor inquiries                                               │
│  • File corrections if needed                                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### W-9 Collection Process

**Before First Payment:**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    W-9 COLLECTION WORKFLOW                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  STEP 1: Request W-9                                                         │
│  ─────────────────────                                                       │
│  Send W-9 form to new subcontractor before any work begins                  │
│                                                                              │
│  Sample Request Email:                                                       │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Subject: W-9 Required - ABC Construction                                    │
│                                                                              │
│  Hi [Name],                                                                  │
│                                                                              │
│  Before we can process your first payment, we need a completed W-9 form.   │
│  Please complete and return the attached form.                              │
│                                                                              │
│  Required information:                                                       │
│  • Legal business name                                                       │
│  • Business type (Individual, LLC, Corp, etc.)                              │
│  • Tax ID (EIN or SSN)                                                       │
│  • Address                                                                   │
│  • Signature and date                                                        │
│                                                                              │
│  We cannot process payment without this form.                               │
│                                                                              │
│  Thanks,                                                                     │
│  [Your name]                                                                 │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  STEP 2: Verify W-9                                                          │
│  ──────────────────                                                          │
│  □ Form is complete (no blank fields)                                       │
│  □ Signed and dated                                                          │
│  □ Business name matches who you're paying                                  │
│  □ Tax ID format is correct                                                  │
│  □ Business type indicated                                                   │
│                                                                              │
│  STEP 3: Enter in QBO                                                        │
│  ────────────────────                                                        │
│  □ Create vendor with legal name                                            │
│  □ Enter Tax ID exactly as shown                                            │
│  □ Check "Track payments for 1099"                                          │
│  □ Attach W-9 to vendor record                                              │
│                                                                              │
│  STEP 4: Store W-9                                                           │
│  ─────────────────                                                           │
│  □ Attached to vendor in QBO (Attachments)                                  │
│  □ Filed in secure location (physical or digital)                           │
│  □ Retain for 4+ years                                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Who Gets a 1099-NEC?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    1099-NEC REQUIREMENTS                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  MUST ISSUE 1099-NEC IF:                                                    │
│  ✅ Paid $600 or more during calendar year                                  │
│  ✅ Paid for services (not products)                                        │
│  ✅ Paid to non-employee                                                    │
│  ✅ Paid to individual, partnership, LLC, or estate                         │
│                                                                              │
│  DO NOT ISSUE 1099 IF:                                                       │
│  ❌ Paid to corporation (C-Corp or S-Corp)*                                 │
│  ❌ Payments under $600 for the year                                        │
│  ❌ Payments for merchandise/products only                                  │
│  ❌ Payments to employees (use W-2)                                         │
│                                                                              │
│  *EXCEPTION: Attorneys/legal services get 1099 even if corporation         │
│                                                                              │
│  COMMON CONSTRUCTION 1099 RECIPIENTS:                                        │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Subcontractors (individuals, LLCs, partnerships)                         │
│  • Independent consultants                                                   │
│  • Architects/engineers (if not corporations)                               │
│  • Equipment rental with operator                                           │
│  • Owner/operators (trucking, equipment)                                    │
│                                                                              │
│  TYPICALLY NOT 1099:                                                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Material suppliers (product purchases)                                   │
│  • Corporations (verify on W-9)                                             │
│  • Equipment rental without operator                                        │
│  • Utilities                                                                 │
│  • Credit card payments (card company reports)                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Running 1099 Reports in QBO

**Step 1: Review Vendor Settings**

```
Navigation: Reports → 1099 Contractor Report (or Vendors → Prepare 1099s)

Review shows:
• Vendors with "Track payments for 1099" checked
• Total payments to each vendor
• Missing Tax IDs
• Missing addresses
```

**Step 2: Fix Issues**

```
Common issues and fixes:

MISSING TAX ID:
→ Contact vendor for W-9
→ Enter TIN in vendor record

WRONG TAX ID:
→ Get new W-9 with correct number
→ Update vendor record

VENDOR NOT TRACKED FOR 1099:
→ Edit vendor → Check "Track payments for 1099"
→ Note: Only tracks going forward; may need manual adjustment

CORPORATION SHOWING ON LIST:
→ Verify W-9 shows corporation
→ Uncheck "Track payments for 1099" if confirmed corp
```

**Step 3: Generate 1099s**

```
Navigation: Taxes → 1099 filings → Prepare 1099s (or use 1099 wizard)

Steps:
1. Select tax year
2. Review/confirm account mapping
3. Review vendor list
4. Verify amounts
5. E-file or print forms
```

### Account Mapping for 1099

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    1099 ACCOUNT MAPPING                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  QBO needs to know which expense accounts contain 1099-reportable payments  │
│                                                                              │
│  TYPICAL CONSTRUCTION MAPPING:                                               │
│                                                                              │
│  Account                          │  1099 Box          │  Include?          │
│  ─────────────────────────────────┼────────────────────┼───────────────────│
│  50200 Subcontractor Costs        │  Box 1 (NEC)       │  ✅ Yes           │
│  50400 Direct Labor (1099)        │  Box 1 (NEC)       │  ✅ Yes           │
│  60500 Professional Fees          │  Box 1 (NEC)       │  ✅ Yes           │
│  60510 Legal Fees                 │  Box 1 (NEC)       │  ✅ Yes           │
│  50100 Materials                  │  N/A               │  ❌ No (products) │
│  50300 Equipment Rental           │  Box 1 (if w/op)   │  ⚠️ Maybe        │
│  60200 Rent                       │  Box 1 (MISC)      │  ⚠️ Maybe        │
│                                                                              │
│  ⚠️ CRITICAL: Map accounts correctly BEFORE running 1099 wizard            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 1099 Filing Options

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    1099 FILING OPTIONS                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  OPTION 1: E-FILE THROUGH QBO                                               │
│  ──────────────────────────────                                              │
│  • QBO submits to IRS electronically                                        │
│  • Additional fee applies (~$15-20/form depending on plan)                  │
│  • QBO mails copy to vendors (or email)                                     │
│  • Easiest option, maintains records in QBO                                 │
│                                                                              │
│  OPTION 2: PRINT AND MAIL                                                    │
│  ─────────────────────────                                                   │
│  • Purchase official 1099 forms (from IRS or office supply)                 │
│  • Print from QBO                                                            │
│  • Mail Copy B to vendors by Jan 31                                         │
│  • File Copy A with IRS (e-file if 10+ forms)                               │
│  • Keep Copy C for your records                                              │
│                                                                              │
│  OPTION 3: USE THIRD-PARTY SERVICE                                           │
│  ─────────────────────────────────                                           │
│  • Export data from QBO                                                      │
│  • Upload to service (Tax1099.com, Track1099, etc.)                         │
│  • Service files with IRS and mails to vendors                              │
│  • Good if you have many forms                                              │
│                                                                              │
│  DEADLINE REMINDER:                                                          │
│  ─────────────────────────────────────────────────────────────────────────  │
│  January 31: File with IRS AND furnish to recipients                        │
│  Both due same day for 1099-NEC!                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Tracking Subcontractor Compliance

### Compliance Checklist by Subcontractor

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SUBCONTRACTOR COMPLIANCE TRACKER                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Vendor: ABC Electrical Services, LLC                                        │
│  Trade: Electrical                                                           │
│                                                                              │
│  DOCUMENT              │  STATUS      │  EXPIRATION    │  ON FILE          │
│  ──────────────────────┼──────────────┼────────────────┼──────────────────│
│  W-9                   │  ✅ Current  │  N/A           │  ✅ Attached      │
│  Subcontract Signed    │  ✅ Complete │  N/A           │  ✅ Attached      │
│  General Liability     │  ✅ Current  │  12/31/2024    │  ✅ Attached      │
│  Workers' Comp         │  ✅ Current  │  01/15/2025    │  ✅ Attached      │
│  Auto Insurance        │  ✅ Current  │  06/30/2024    │  ✅ Attached      │
│  State License         │  ✅ Active   │  12/31/2024    │  ✅ Attached      │
│  Bond (if required)    │  N/A         │  N/A           │  N/A              │
│                                                                              │
│  NOTES:                                                                      │
│  Auto insurance expiring soon - request renewal cert by 06/15/2024          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Tracking Expiration Dates

**Option 1: QBO Vendor Notes**

```
In vendor record → Notes field:

"COMPLIANCE DATES:
GL Exp: 12/31/2024
WC Exp: 01/15/2025
Auto Exp: 06/30/2024
License Exp: 12/31/2024"
```

**Option 2: Custom Fields (QBO Advanced)**

```
Create custom fields:
• GL Expiration Date
• WC Expiration Date
• License Expiration Date

Run reports filtered by expiration date
```

**Option 3: External Tracking**

```
Maintain spreadsheet or use compliance tracking software:
• Expiration dates with auto-reminders
• Document uploads
• Renewal request templates
```

### Monthly Compliance Review

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MONTHLY COMPLIANCE CHECKLIST                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Complete by: 5th of each month                                              │
│                                                                              │
│  □ Review insurance certificates expiring within 60 days                    │
│  □ Send renewal requests to expiring subs                                   │
│  □ Update received certificates in vendor records                           │
│  □ Flag vendors with lapsed insurance                                       │
│  □ Verify new vendors have all required documents                           │
│  □ Update compliance tracker                                                 │
│                                                                              │
│  INSURANCE RENEWAL REQUEST TEMPLATE:                                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Subject: Insurance Certificate Renewal Required                             │
│                                                                              │
│  Hi [Name],                                                                  │
│                                                                              │
│  Our records show your [GL/WC/Auto] insurance certificate expires on        │
│  [Date]. Please send an updated certificate to continue working on          │
│  our projects.                                                               │
│                                                                              │
│  Requirements:                                                               │
│  • General Liability: $1,000,000/$2,000,000                                 │
│  • Workers' Comp: Statutory limits                                          │
│  • Additional Insured: [Your Company Name]                                  │
│                                                                              │
│  Please send updated certificate to [email] by [date].                      │
│                                                                              │
│  Thanks,                                                                     │
│  [Name]                                                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Lien Waiver Management

### Understanding Lien Waivers

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LIEN WAIVER FUNDAMENTALS                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT IS A LIEN WAIVER?                                                      │
│  ─────────────────────                                                       │
│  A legal document where a contractor/subcontractor/supplier waives          │
│  their right to file a mechanic's lien against the property for             │
│  work performed or materials supplied.                                       │
│                                                                              │
│  WHY LIEN WAIVERS MATTER:                                                    │
│  ─────────────────────────                                                   │
│  • Protect property owner from double payment                               │
│  • Protect GC from sub's liens                                               │
│  • Required by most contracts and lenders                                   │
│  • Failure to collect = potential liability                                 │
│                                                                              │
│  TYPES OF LIEN WAIVERS:                                                      │
│  ─────────────────────                                                       │
│                                                                              │
│  1. CONDITIONAL WAIVER ON PROGRESS PAYMENT                                   │
│     • Given with pay application                                             │
│     • Becomes effective WHEN payment clears                                 │
│     • Protects sub: no waiver if check bounces                              │
│                                                                              │
│  2. UNCONDITIONAL WAIVER ON PROGRESS PAYMENT                                 │
│     • Given AFTER payment received and cleared                              │
│     • Effective immediately upon signing                                    │
│     • Use only after confirming funds received                              │
│                                                                              │
│  3. CONDITIONAL WAIVER ON FINAL PAYMENT                                      │
│     • Given with final pay application                                       │
│     • Becomes effective when final payment clears                           │
│     • Covers entire contract amount                                          │
│                                                                              │
│  4. UNCONDITIONAL WAIVER ON FINAL PAYMENT                                    │
│     • Given AFTER final payment received                                     │
│     • Complete release of all lien rights                                   │
│     • Project closeout document                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Lien Waiver Flow for Subcontractors

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LIEN WAIVER WORKFLOW                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  AS GENERAL CONTRACTOR - RECEIVING FROM SUBS:                                │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  PROGRESS PAYMENTS:                                                          │
│                                                                              │
│       Sub submits                    GC reviews              GC pays sub    │
│       pay app                        and approves            by check/ACH    │
│          │                               │                        │         │
│          ▼                               ▼                        ▼         │
│   ┌─────────────┐               ┌─────────────────┐       ┌──────────────┐ │
│   │ Conditional │    →          │ GC holds until  │   →   │ Sub provides │ │
│   │ Waiver      │               │ waiver received │       │ Unconditional│ │
│   │ (current $) │               │                 │       │ Waiver for   │ │
│   └─────────────┘               └─────────────────┘       │ PRIOR payment│ │
│   Plus:                                                    └──────────────┘ │
│   Unconditional                                                             │
│   for PRIOR payment                                                         │
│                                                                              │
│  BEST PRACTICE TIMELINE:                                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Pay App #1:                                                                 │
│  • Sub provides: Conditional Waiver for Pay App #1 ($50,000)                │
│  • GC pays: $50,000                                                         │
│                                                                              │
│  Pay App #2:                                                                 │
│  • Sub provides: Conditional Waiver for Pay App #2 ($45,000)                │
│  •               Unconditional Waiver for Pay App #1 ($50,000)              │
│  • GC pays: $45,000                                                         │
│                                                                              │
│  Pay App #3:                                                                 │
│  • Sub provides: Conditional Waiver for Pay App #3 ($40,000)                │
│  •               Unconditional Waiver for Pay App #2 ($45,000)              │
│  • GC pays: $40,000                                                         │
│                                                                              │
│  Final Pay App:                                                              │
│  • Sub provides: Conditional Final Waiver ($15,000 + retention)             │
│  •               Unconditional Waiver for Pay App #3 ($40,000)              │
│  • GC pays: Final amount                                                    │
│  • Sub provides: Unconditional Final Waiver (after check clears)            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Tracking Lien Waivers in QBO

**Method 1: Bill Attachments**

```
For each subcontractor bill:
1. Receive lien waiver from sub
2. Scan to PDF
3. Open bill in QBO
4. Attach lien waiver document
5. Add note: "Conditional waiver attached for this payment"
```

**Method 2: Vendor Attachments**

```
For each vendor:
1. Compile all lien waivers received
2. Open Vendor record
3. Go to Attachments
4. Upload all waivers organized by date/project

Naming convention: LW-2024-001-P03-COND.pdf
(Lien Waiver-Job#-PayApp#-Type)
```

**Method 3: Custom Memo Field**

```
When recording sub payment in QBO:

Bill memo field:
"Pay App #3 - $45,000
Cond waiver received 03/15/24
Uncond waiver for PA#2 received 03/15/24"
```

### Lien Waiver Tracking Spreadsheet

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LIEN WAIVER LOG                                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Job: 2024-001 Smith Residence                                               │
│                                                                              │
│  Vendor           Pay App  Amount     Cond Rcvd   Uncond Rcvd   Check #     │
│  ────────────────────────────────────────────────────────────────────────── │
│  ABC Electric     PA #1    $15,000    03/01/24    03/15/24      4521        │
│  ABC Electric     PA #2    $12,500    03/15/24    04/01/24      4589        │
│  ABC Electric     PA #3    $10,000    04/01/24    PENDING       4621        │
│  XYZ Plumbing     PA #1    $22,000    03/05/24    03/20/24      4525        │
│  XYZ Plumbing     PA #2    $18,500    03/20/24    04/05/24      4598        │
│  123 HVAC         PA #1    $35,000    03/10/24    03/25/24      4532        │
│  Smith Lumber     Invoice  $8,450     N/A*        03/12/24      4518        │
│                                                                              │
│  * Material suppliers may provide unconditional with delivery               │
│                                                                              │
│  RETENTION WAIVERS: (Due at project closeout)                               │
│  ABC Electric     Retention  $3,750   Pending     Pending       -           │
│  XYZ Plumbing     Retention  $4,050   Pending     Pending       -           │
│  123 HVAC         Retention  $3,500   Pending     Pending       -           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Pay Application Processing

### Subcontractor Pay App Workflow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SUB PAY APP PROCESSING                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  STEP 1: RECEIVE PAY APPLICATION                                             │
│  ─────────────────────────────────                                           │
│  Sub submits:                                                                │
│  □ Pay application/invoice                                                   │
│  □ Schedule of values (if required)                                         │
│  □ Conditional lien waiver (current payment)                                │
│  □ Unconditional lien waiver (prior payment)                                │
│  □ Certified payroll (if applicable)                                        │
│                                                                              │
│  STEP 2: VERIFY DOCUMENTS                                                    │
│  ─────────────────────────                                                   │
│  □ All required documents received                                          │
│  □ Amounts match contract/approved changes                                  │
│  □ Work completion verified (PM sign-off)                                   │
│  □ Lien waivers complete and accurate                                       │
│  □ Insurance current                                                         │
│                                                                              │
│  STEP 3: ENTER BILL IN QBO                                                   │
│  ─────────────────────────                                                   │
│  □ Create bill from PO (if applicable)                                      │
│  □ Verify line items match pay app                                          │
│  □ Assign to correct job (Class)                                            │
│  □ Attach all documents to bill                                             │
│  □ Add memo with pay app details                                            │
│                                                                              │
│  STEP 4: CALCULATE RETENTION                                                 │
│  ────────────────────────────                                                │
│  If contract has retention:                                                  │
│  □ Calculate retention amount (typically 10%)                               │
│  □ Create retention payable entry                                           │
│  □ Net payment = Gross - Retention                                          │
│                                                                              │
│  STEP 5: APPROVE AND SCHEDULE PAYMENT                                        │
│  ────────────────────────────────────                                        │
│  □ Get approval per authority limits                                        │
│  □ Schedule payment per contract terms                                      │
│  □ Verify cash available                                                     │
│                                                                              │
│  STEP 6: PROCESS PAYMENT                                                     │
│  ───────────────────────                                                     │
│  □ Write check or schedule ACH                                              │
│  □ Record payment in QBO                                                    │
│  □ Mail/deliver check with remittance                                       │
│                                                                              │
│  STEP 7: FOLLOW UP                                                           │
│  ─────────────────                                                           │
│  □ Request unconditional waiver (after check clears)                        │
│  □ File all documents                                                        │
│  □ Update lien waiver log                                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Recording Sub Bills with Retention

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  BILL - XYZ Plumbing Services                             [Save] [Cancel]   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Vendor: XYZ Plumbing Services       Bill date: 03/15/2024                  │
│  Terms: Net 30                       Due date: 04/14/2024                   │
│  Ref #: INV-2024-0312               Memo: Pay App #2 - Smith Residence     │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │ Category Details                                                    │    │
│  ├─────────────────┬───────────────────────────────┬──────────────────┤    │
│  │ CATEGORY        │ DESCRIPTION                   │ AMOUNT           │    │
│  ├─────────────────┼───────────────────────────────┼──────────────────┤    │
│  │ 50200 Subcontr  │ Rough plumbing complete       │ $18,500.00       │    │
│  │                 │ Per Pay App #2                │                  │    │
│  │ Class: 2024-001 │                               │                  │    │
│  ├─────────────────┼───────────────────────────────┼──────────────────┤    │
│  │ 23100 Retention │ 10% Retention Held            │ ($1,850.00)      │    │
│  │ Payable         │ Pay App #2                    │                  │    │
│  │ Class: 2024-001 │                               │                  │    │
│  ├─────────────────┴───────────────────────────────┼──────────────────┤    │
│  │                              NET AMOUNT DUE:    │ $16,650.00       │    │
│  └──────────────────────────────────────────────────┴──────────────────┘    │
│                                                                              │
│  Attachments: [Pay App #2.pdf] [Cond Waiver.pdf] [Uncond PA#1.pdf]          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

RESULT:
• 50200 Subcontractor Costs: DEBIT $18,500 (full cost to job)
• 23100 Retention Payable: CREDIT $1,850 (liability for retention)
• 20000 Accounts Payable: CREDIT $16,650 (net amount owed now)
```

---

## Insurance Certificate Tracking

### Required Insurance Coverage

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TYPICAL INSURANCE REQUIREMENTS                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  GENERAL LIABILITY (GL):                                                     │
│  ─────────────────────                                                       │
│  Minimum Limits:                                                             │
│  • Each Occurrence: $1,000,000                                              │
│  • General Aggregate: $2,000,000                                            │
│  • Products/Completed Operations: $1,000,000                                │
│                                                                              │
│  Verify:                                                                     │
│  □ Your company listed as Additional Insured                                │
│  □ Policy covers construction operations                                    │
│  □ Current (not expired)                                                    │
│                                                                              │
│  WORKERS' COMPENSATION:                                                      │
│  ─────────────────────                                                       │
│  Minimum Limits:                                                             │
│  • Workers' Comp: Statutory (state-required limits)                         │
│  • Employers Liability: $500,000/$500,000/$500,000                          │
│                                                                              │
│  Verify:                                                                     │
│  □ Coverage includes all employees                                          │
│  □ Correct state(s) listed                                                  │
│  □ Classification codes appropriate for work                                │
│                                                                              │
│  Note: Some states allow exemptions for owners/small subs                   │
│  Get signed waiver if sub claims exemption                                  │
│                                                                              │
│  AUTO LIABILITY:                                                             │
│  ──────────────                                                              │
│  Minimum Limits:                                                             │
│  • Combined Single Limit: $1,000,000                                        │
│                                                                              │
│  Verify:                                                                     │
│  □ Covers all vehicles used on your projects                                │
│  □ Includes hired and non-owned auto coverage                               │
│                                                                              │
│  UMBRELLA/EXCESS (for larger subs):                                          │
│  ─────────────────────────────────                                           │
│  • Additional $1,000,000 - $5,000,000 over underlying policies              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Reading a Certificate of Insurance (COI)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ACORD 25 CERTIFICATE - KEY FIELDS                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PRODUCER (Insurance Agent):                                                 │
│  └── Who to contact for questions                                           │
│                                                                              │
│  INSURED (The Subcontractor):                                               │
│  └── Verify matches vendor name exactly                                     │
│                                                                              │
│  COVERAGES:                                                                  │
│  ─────────                                                                   │
│  Type of Insurance │ Policy Number │ Effective │ Expiration │ Limits        │
│  ──────────────────┼───────────────┼───────────┼────────────┼────────────── │
│  Commercial GL     │ GL-12345      │ 01/01/24  │ 01/01/25   │ $1M/$2M      │
│  Auto Liability    │ AU-67890      │ 01/01/24  │ 01/01/25   │ $1M CSL      │
│  Umbrella          │ UMB-11111     │ 01/01/24  │ 01/01/25   │ $2M          │
│  Workers Comp      │ WC-22222      │ 01/01/24  │ 01/01/25   │ Statutory    │
│                                                                              │
│  DESCRIPTION OF OPERATIONS:                                                  │
│  └── May list specific project or "All Operations"                          │
│  └── Look for: "Additional Insured: [Your Company Name]"                    │
│                                                                              │
│  CERTIFICATE HOLDER:                                                         │
│  └── Should be YOUR company name and address                                │
│  └── This is who gets notified of cancellation                              │
│                                                                              │
│  CANCELLATION:                                                               │
│  └── Notice period before policy cancelled (usually 30 days)                │
│                                                                              │
│  ⚠️ IMPORTANT:                                                              │
│  A certificate is EVIDENCE of insurance, not a guarantee.                   │
│  Policies can be cancelled mid-term. Request notification endorsement.      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Storing Certificates in QBO

```
For each subcontractor vendor:

1. Open Vendor Record
2. Go to Attachments
3. Upload documents:
   • COI-2024.pdf (current certificate)
   • COI-2023.pdf (prior year - keep for records)
   • WC-Exemption.pdf (if applicable)
   • License.pdf

4. Add expiration note in vendor Notes field:
   "GL: 01/01/25, WC: 01/01/25, Auto: 07/01/24"
```

---

## Best Practices and Common Mistakes

### Best Practices

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SUBCONTRACTOR MANAGEMENT BEST PRACTICES                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. COLLECT DOCUMENTS BEFORE FIRST PAYMENT                                   │
│     • W-9                                                                    │
│     • Insurance certificates                                                 │
│     • License (if required)                                                  │
│     • Signed subcontract                                                     │
│                                                                              │
│  2. VERIFY TAX ID BEFORE YEAR-END                                           │
│     • Use IRS TIN Matching program (free)                                   │
│     • Catches errors before 1099 filing                                     │
│     • Avoid B-Notices and penalties                                         │
│                                                                              │
│  3. NO PAY WITHOUT LIEN WAIVER                                               │
│     • Make it policy: "No waiver, no check"                                 │
│     • Train PMs and accounting staff                                        │
│     • Include requirement in subcontract                                    │
│                                                                              │
│  4. TRACK INSURANCE EXPIRATIONS PROACTIVELY                                  │
│     • Set calendar reminders 60 days before expiration                      │
│     • Send renewal requests automatically                                   │
│     • Stop new work with lapsed subs                                        │
│                                                                              │
│  5. KEEP SUBCONTRACTOR FILES ORGANIZED                                       │
│     • All documents attached to vendor in QBO                               │
│     • Or maintain organized digital folders                                 │
│     • Easy retrieval for audits                                             │
│                                                                              │
│  6. REVIEW 1099 LIST QUARTERLY                                               │
│     • Catch missing W-9s early                                              │
│     • Verify vendor setup (1099 tracking checkbox)                          │
│     • Less year-end stress                                                   │
│                                                                              │
│  7. DOCUMENT EVERYTHING                                                       │
│     • Attach correspondence to vendor/bills                                 │
│     • Keep records of verbal agreements                                     │
│     • Protect yourself from disputes                                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Mistakes

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COMMON MISTAKES TO AVOID                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ❌ MISTAKE 1: Paying without W-9 on file                                   │
│     Fix: Strict policy - W-9 before first payment                           │
│     Risk: Can't file 1099, IRS backup withholding                           │
│                                                                              │
│  ❌ MISTAKE 2: Not checking "Track payments for 1099"                       │
│     Fix: Verify checkbox on EVERY new vendor                                │
│     Risk: Vendor payments not included in 1099                              │
│                                                                              │
│  ❌ MISTAKE 3: Wrong Tax ID entered                                         │
│     Fix: Double-check against W-9, use TIN matching                         │
│     Risk: 1099 rejected, penalties for incorrect TIN                        │
│                                                                              │
│  ❌ MISTAKE 4: 1099 issued to corporation                                   │
│     Fix: Verify entity type on W-9                                          │
│     Risk: Embarrassment, sub may be annoyed                                 │
│                                                                              │
│  ❌ MISTAKE 5: Missing lien waivers                                         │
│     Fix: No payment without proper waivers                                  │
│     Risk: Liens on customer property, liability to owner                    │
│                                                                              │
│  ❌ MISTAKE 6: Expired insurance on working subs                            │
│     Fix: Monthly expiration review, strict enforcement                      │
│     Risk: Uninsured loss, your policy becomes primary                       │
│                                                                              │
│  ❌ MISTAKE 7: Paying ahead of waiver exchange                              │
│     Fix: Waiver received BEFORE or WITH payment                             │
│     Risk: No leverage to get waiver after payment                           │
│                                                                              │
│  ❌ MISTAKE 8: Not assigning sub costs to jobs                              │
│     Fix: Class/job on EVERY sub bill line                                   │
│     Risk: Inaccurate job costing, can't calculate profitability             │
│                                                                              │
│  ❌ MISTAKE 9: Missing 1099 filing deadline                                 │
│     Fix: Calendar reminders, prepare in early January                       │
│     Risk: $50-$280 penalty PER late form                                    │
│                                                                              │
│  ❌ MISTAKE 10: Verbal subcontracts only                                    │
│     Fix: Written agreement for ALL subs                                     │
│     Risk: Disputes over scope, price, terms                                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SUBCONTRACTOR QUICK REFERENCE                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  NEW SUBCONTRACTOR CHECKLIST:                                                │
│  □ W-9 received and verified                                                │
│  □ Vendor created in QBO                                                    │
│  □ Tax ID entered correctly                                                 │
│  □ "Track payments for 1099" checked                                        │
│  □ Insurance certificates on file                                           │
│  □ Additional insured endorsement                                           │
│  □ Signed subcontract                                                        │
│  □ All docs attached to vendor record                                       │
│                                                                              │
│  PAYMENT CHECKLIST:                                                          │
│  □ Pay application received                                                 │
│  □ Work verified complete                                                   │
│  □ Conditional lien waiver for current payment                              │
│  □ Unconditional lien waiver for prior payment                              │
│  □ Insurance still current                                                   │
│  □ Bill entered with correct job assignment                                 │
│  □ Retention calculated and recorded                                        │
│  □ Approval obtained per authority limits                                   │
│                                                                              │
│  1099 TIMELINE:                                                              │
│  • Throughout year: Collect W-9s, verify tracking                           │
│  • November: Review vendor list                                              │
│  • January 1-15: Run reports, prepare forms                                 │
│  • January 31: FILE AND FURNISH DEADLINE                                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With subcontractor management understood:
- [Purchase Orders](./01-purchase-orders.md) - PO workflows for subs
- [Recording Transactions](../basics/03-recording-transactions.md) - Complete AP workflows
- [Retention Tracking](../tutorials/06-retention-tracking.md) - Detailed retention guide

---

*[Back to Main Guide](../../README.md)*
