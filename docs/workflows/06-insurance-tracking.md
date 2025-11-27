# Insurance Tracking & Compliance for Construction

## Overview

Construction companies face complex insurance requirements. You need coverage for your operations, AND you must verify coverage from every subcontractor. This guide covers both sides of construction insurance management in QuickBooks Online.

---

## Types of Construction Insurance

### Insurance Coverage Matrix

```
CONSTRUCTION INSURANCE TYPES

┌─────────────────────────────────────────────────────────────────────────────────┐
│                                                                                  │
│  YOUR COMPANY'S INSURANCE                                                        │
│  ┌───────────────────────────────────────────────────────────────────────────┐  │
│  │ GENERAL LIABILITY (GL)                                                    │  │
│  │ • Bodily injury / property damage                                         │  │
│  │ • Products / completed operations                                         │  │
│  │ • Personal / advertising injury                                           │  │
│  │ • Typical: $1M per occurrence / $2M aggregate                             │  │
│  └───────────────────────────────────────────────────────────────────────────┘  │
│  ┌───────────────────────────────────────────────────────────────────────────┐  │
│  │ WORKERS' COMPENSATION (WC)                                                │  │
│  │ • Employee injury coverage                                                │  │
│  │ • State-mandated (most states)                                            │  │
│  │ • Rates vary by classification                                            │  │
│  │ • Experience modification factor (EMR)                                    │  │
│  └───────────────────────────────────────────────────────────────────────────┘  │
│  ┌───────────────────────────────────────────────────────────────────────────┐  │
│  │ COMMERCIAL AUTO                                                           │  │
│  │ • Company vehicles                                                        │  │
│  │ • Hired & non-owned auto                                                  │  │
│  │ • Typical: $1M combined single limit                                      │  │
│  └───────────────────────────────────────────────────────────────────────────┘  │
│  ┌───────────────────────────────────────────────────────────────────────────┐  │
│  │ UMBRELLA / EXCESS LIABILITY                                               │  │
│  │ • Additional limits above GL/Auto/WC                                      │  │
│  │ • Typical: $1M - $10M+ depending on project requirements                  │  │
│  └───────────────────────────────────────────────────────────────────────────┘  │
│  ┌───────────────────────────────────────────────────────────────────────────┐  │
│  │ PROFESSIONAL LIABILITY (E&O) - Design-Build                               │  │
│  │ • Errors & omissions in design                                            │  │
│  │ • Required for design-build                                               │  │
│  └───────────────────────────────────────────────────────────────────────────┘  │
│  ┌───────────────────────────────────────────────────────────────────────────┐  │
│  │ BUILDER'S RISK                                                            │  │
│  │ • Property coverage during construction                                   │  │
│  │ • May be provided by owner or contractor                                  │  │
│  └───────────────────────────────────────────────────────────────────────────┘  │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Minimum Coverage Requirements

| Coverage Type | Typical Minimum | Commercial Projects | Large Projects |
|---------------|-----------------|--------------------|--------------------|
| **General Liability** | $1M/$2M | $1M/$2M | $2M/$4M |
| **Workers' Comp** | Statutory | Statutory | Statutory |
| **Employers Liability** | $500K | $1M | $1M |
| **Auto Liability** | $1M CSL | $1M CSL | $1M CSL |
| **Umbrella** | $1M | $2M-$5M | $5M-$10M+ |
| **Professional (D-B)** | N/A | $1M | $2M+ |

---

## Tracking Your Company's Insurance

### Insurance Calendar Setup

**Create a Master Insurance Calendar:**

```
INSURANCE RENEWAL & PAYMENT CALENDAR

Policy              Carrier          Policy #       Renewal    Premium    Payment
────────────────────────────────────────────────────────────────────────────────────
General Liability   ABC Insurance    GL-2024-001    3/1/2025   $45,000    Monthly
Workers' Comp       State Fund       WC-2024-002    7/1/2025   $85,000    Quarterly
Commercial Auto     DEF Insurance    CA-2024-003    5/1/2025   $18,000    Semi-Annual
Umbrella            ABC Insurance    UMB-2024-004   3/1/2025   $12,000    Annual
Builder's Risk      GHI Insurance    BR-2024-005    Per Project Varies   Per Project
────────────────────────────────────────────────────────────────────────────────────

KEY DATES:
□ 60 days before renewal - Review coverage needs
□ 30 days before renewal - Receive renewal quote
□ 15 days before renewal - Bind coverage
□ After renewal - Update certificate of insurance
```

### Insurance Expense Tracking in QBO

**Chart of Accounts:**
```
64000 Insurance Expense
├── 64100 General Liability Insurance
├── 64200 Workers' Compensation Insurance
├── 64300 Commercial Auto Insurance
├── 64400 Umbrella Insurance
├── 64500 Builder's Risk Insurance
├── 64600 Professional Liability Insurance
├── 64700 Health Insurance (Employee)
└── 64800 Other Insurance
```

**For Project-Specific Insurance:**
- Track to the project using Customer/Class
- Builder's risk often billed to specific job

### Workers' Compensation by Class Code

Track WC premium by classification for audit preparation:

```
WC CLASSIFICATION TRACKING

Class Code    Description              Rate      Payroll        Premium
────────────────────────────────────────────────────────────────────────────
5403          Carpentry                $8.50     $450,000       $38,250
5221          Concrete Work            $12.00    $200,000       $24,000
8810          Clerical                 $0.35     $150,000       $525
5606          Contractor - Exec/Super  $5.00     $250,000       $12,500
────────────────────────────────────────────────────────────────────────────
TOTAL ESTIMATED PREMIUM                                         $75,275

Experience Modification Rate (EMR): 0.92
MODIFIED PREMIUM: $75,275 × 0.92 = $69,253
```

---

## Subcontractor Insurance Compliance

### Certificate of Insurance (COI) Requirements

**What Must Be On a Valid COI:**

```
CERTIFICATE OF INSURANCE - REQUIRED ELEMENTS

┌─────────────────────────────────────────────────────────────────────────────────┐
│  □ NAMED INSURED                                                                │
│    • Subcontractor's legal name                                                 │
│    • Must match W-9 and contract exactly                                        │
│                                                                                  │
│  □ POLICY INFORMATION                                                           │
│    • Insurance company name (carrier)                                           │
│    • Policy number                                                              │
│    • Policy effective dates                                                     │
│    • Coverage type and limits                                                   │
│                                                                                  │
│  □ COVERAGE LIMITS                                                              │
│    • General Liability limits (per occurrence / aggregate)                      │
│    • Workers' Comp (statutory + employers liability)                            │
│    • Auto liability limits                                                      │
│    • Umbrella limits (if required)                                              │
│                                                                                  │
│  □ ADDITIONAL INSURED STATUS                                                    │
│    • Your company listed as Additional Insured                                  │
│    • Project/location may be specified                                          │
│    • "Additional Insured as required by written contract"                       │
│                                                                                  │
│  □ WAIVER OF SUBROGATION                                                        │
│    • Waiver in favor of your company                                            │
│    • Prevents carrier from suing you after paying claim                         │
│                                                                                  │
│  □ CERTIFICATE HOLDER                                                           │
│    • Your company name and address                                              │
│    • Where cancellation notice is sent                                          │
│                                                                                  │
│  □ CANCELLATION NOTICE                                                          │
│    • 30-day notice of cancellation                                              │
│    • Some policies say "endeavor to" (weaker)                                   │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Subcontractor Insurance Tracking System

**Track These Items for Each Subcontractor:**

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                    SUBCONTRACTOR INSURANCE TRACKER                               │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│  SUBCONTRACTOR: ABC Electric, Inc.                                               │
│  CONTACT: John Smith | (555) 123-4567 | john@abcelectric.com                     │
│                                                                                  │
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                      GENERAL LIABILITY                                  │    │
│  │  Carrier: XYZ Insurance Company                                         │    │
│  │  Policy #: GL-12345-2024                                                │    │
│  │  Effective: 1/1/2024 - 1/1/2025                                         │    │
│  │  Limits: $1,000,000 per occurrence / $2,000,000 aggregate               │    │
│  │  Additional Insured: ☑ Yes  ☐ No                                        │    │
│  │  Waiver of Subrogation: ☑ Yes  ☐ No                                     │    │
│  │  Status: ☑ Current  ☐ Expiring Soon  ☐ Expired                          │    │
│  │  COI on File: ☑ Yes  Date Received: 1/15/2024                           │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
│                                                                                  │
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                      WORKERS' COMPENSATION                              │    │
│  │  Carrier: State Compensation Fund                                       │    │
│  │  Policy #: WC-67890-2024                                                │    │
│  │  Effective: 7/1/2024 - 7/1/2025                                         │    │
│  │  Limits: Statutory / $1,000,000 EL                                      │    │
│  │  Waiver of Subrogation: ☑ Yes  ☐ No                                     │    │
│  │  Status: ☑ Current  ☐ Expiring Soon  ☐ Expired                          │    │
│  │  COI on File: ☑ Yes  Date Received: 7/10/2024                           │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
│                                                                                  │
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                      AUTO LIABILITY                                     │    │
│  │  Carrier: XYZ Insurance Company                                         │    │
│  │  Policy #: CA-11111-2024                                                │    │
│  │  Effective: 1/1/2024 - 1/1/2025                                         │    │
│  │  Limits: $1,000,000 Combined Single Limit                               │    │
│  │  Additional Insured: ☑ Yes  ☐ No                                        │    │
│  │  Status: ☑ Current  ☐ Expiring Soon  ☐ Expired                          │    │
│  │  COI on File: ☑ Yes  Date Received: 1/15/2024                           │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
│                                                                                  │
│  EXPIRATION ALERTS:                                                              │
│  ☑ GL expires in 45 days - Request renewal COI                                   │
│                                                                                  │
│  COMPLIANCE STATUS: ☑ COMPLIANT  ☐ NON-COMPLIANT                                 │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Insurance Compliance Workflow

```
SUBCONTRACTOR INSURANCE COMPLIANCE PROCESS

Step 1: Before Subcontract Award
├── Request COI with specific requirements
├── Verify coverage meets project requirements
├── Check Additional Insured and Waiver endorsements
└── File COI if compliant; reject if not

Step 2: During Project
├── Track expiration dates
├── Request renewal COIs 30 days before expiration
├── Hold payment if coverage lapses
└── Maintain current COI on file

Step 3: Expiration Management
├── Run weekly expiration report
├── Send renewal request emails automatically (if possible)
├── Follow up on non-responses
└── Escalate to management if coverage lapses

Step 4: Non-Compliance Actions
├── First notice: Request updated COI
├── Second notice: Warning - payment will be held
├── Third notice: Payment held until compliant
└── Last resort: Default subcontractor (if required by contract)
```

---

## QBO Setup for Insurance Tracking

### Using Custom Fields for Insurance

**In QBO Vendor Records:**

While QBO doesn't have built-in insurance tracking, you can:

1. **Add notes to vendor records:**
   - Open Vendor → Notes section
   - Track key dates and status

2. **Use vendor sub-types:**
   - Create "Compliant Subs" and "Non-Compliant Subs" categories
   - Filter payment runs by compliance status

3. **Create recurring reminders:**
   - Use QBO Tasks or external calendar
   - 30-day advance notice for expirations

### Tracking Insurance Costs

**Project-Specific Insurance:**
```
When you purchase project-specific insurance:

Bill Entry:
  Vendor: GHI Insurance Company
  Account: 64500 Builder's Risk Insurance
  Amount: $15,000
  Customer/Project: Office Building Project
  Memo: Builder's Risk policy for project duration
```

**Allocated Insurance:**
```
To allocate insurance to projects via journal entry:

Debit: 50600 Job Cost - Insurance (Job A)    $2,500
Debit: 50600 Job Cost - Insurance (Job B)    $1,800
Debit: 50600 Job Cost - Insurance (Job C)    $1,200
Credit: 64100 General Liability Insurance             $5,500
```

---

## Insurance Audits

### Workers' Compensation Audit

**Annual WC Audit Process:**

1. **Auditor Request:**
   - Payroll by classification code
   - 941 quarterly reports
   - State unemployment reports
   - Subcontractor payments (for uninsured subs)

2. **Prepare Documentation:**
   - Run payroll reports by employee
   - Verify classifications are correct
   - Identify any misclassified employees
   - Gather subcontractor COIs (to exclude from your premium)

3. **Audit Adjustments:**
   - Premium increase if payroll exceeded estimate
   - Premium decrease if payroll was lower
   - Reclassification adjustments

**QBO Reports for WC Audit:**
- Payroll Summary by Employee
- Payroll Detail by Date Range
- Vendor payments (subcontractors) - 1099 report

### General Liability Audit

**GL Audit Basis:**
- May be based on revenue (gross receipts)
- May be based on payroll
- May be based on subcontractor cost

**Prepare:**
- P&L showing gross revenue
- Subcontractor cost detail
- Payroll summary if applicable

---

## OCIP/CCIP Programs

### What Are Wrap-Up Programs?

```
WRAP-UP INSURANCE PROGRAMS

OCIP (Owner-Controlled Insurance Program)
├── Owner provides GL and WC for entire project
├── All contractors "wrap into" owner's program
├── Contractor credits insurance cost from bid
└── Reduces coverage gaps, centralizes claims

CCIP (Contractor-Controlled Insurance Program)
├── GC provides GL and WC for entire project
├── Subcontractors wrap into GC's program
├── Sub credits insurance cost from bid
└── GC controls coverage and claims

BENEFITS:
• Volume purchasing power
• Uniform coverage (no gaps)
• Centralized claims management
• Eliminates certificate tracking (mostly)

CHALLENGES:
• Complex administration
• Insurance credit calculations
• Enrollment requirements
• Claim coordination
```

### OCIP/CCIP Accounting

**When You Deduct Insurance from Sub:**
```
Original Subcontract: $100,000
Less: Insurance Credit (3%): ($3,000)
Net Subcontract Value: $97,000
```

**QBO Treatment:**
- Bill subcontractor for full amount
- Record insurance credit as reduction or separate line

---

## Common Insurance Problems

### Problem 1: Sub's COI Expires Mid-Project

**Risk:** You may be liable if sub is uninsured during work
**Solution:**
1. Hold all payments until renewed COI received
2. Contact sub's insurance agent directly
3. Have backup sub available if needed

### Problem 2: Sub Doesn't Carry Required Coverage

**Risk:** Claim with no sub coverage falls to you
**Solution:**
1. Verify limits BEFORE awarding subcontract
2. Don't accept lower limits without owner approval
3. Consider requiring umbrella if GL is light

### Problem 3: Your Coverage Lapses

**Risk:** Immediate contract default possible
**Solution:**
1. Set reminders 60 days before renewal
2. Maintain relationship with insurance broker
3. Budget for premium payments

### Problem 4: Claim Affects Renewal

**Risk:** Premium increase, possible non-renewal
**Solution:**
1. Strong safety program reduces claims
2. Work with broker on claims management
3. Shop coverage if premium jumps significantly

---

## Insurance Compliance Checklist

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                    MONTHLY INSURANCE COMPLIANCE REVIEW                           │
│                    Month: _______________                                        │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│  YOUR COMPANY'S INSURANCE                                                        │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │ □ All policies current (no lapses)                                       │   │
│  │ □ Certificates available for customers/GCs                               │   │
│  │ □ No policies expiring in next 30 days                                   │   │
│  │     OR renewal in process for: _______________________                   │   │
│  │ □ Premium payments current                                               │   │
│  │ □ No pending claims affecting coverage                                   │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  SUBCONTRACTOR COMPLIANCE                                                        │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │ □ All active subs have current COIs                                      │   │
│  │ □ Expiring COIs identified and requests sent:                            │   │
│  │     Sub: _________________ Expires: ________ Status: ________            │   │
│  │     Sub: _________________ Expires: ________ Status: ________            │   │
│  │ □ Non-compliant subs on payment hold:                                    │   │
│  │     Sub: _________________ Issue: _______________________                │   │
│  │ □ New subs this month have COIs on file:                                 │   │
│  │     □ _________________ COI: ☑ W-9: ☑ Agreement: ☑                       │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  Completed by: _________________ Date: ________                                  │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Key Takeaways

1. **Insurance is non-negotiable** - Don't let coverage lapse
2. **Verify before you pay** - No current COI = no payment
3. **Track expirations proactively** - 30-day advance warning
4. **Additional insured matters** - Protects you from sub's claims
5. **Audit preparation** - Track payroll by WC class code
6. **Document everything** - Keep all COIs on file
7. **Know your limits** - Meet project requirements

---

## Next Steps

- For subcontractor compliance → [Subcontractor Management](./02-subcontractor-1099-lien-waivers.md)
- For vendor setup → [Vendor Setup & AP](../basics/04-vendor-setup-ap.md)
- For audit prep → [Audit Preparation Guide](../compliance/03-audit-preparation.md)

---

*[← Previous: Prevailing Wage](./05-prevailing-wage-certified-payroll.md) | [Next: Material Management →](./07-material-management.md)*
