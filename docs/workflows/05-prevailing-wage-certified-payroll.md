# Prevailing Wage and Certified Payroll

## Overview

Government-funded construction projects often require contractors to pay "prevailing wages" - wage rates determined by the Department of Labor for specific trades in specific geographic areas. This chapter covers the accounting and compliance requirements for prevailing wage work in QuickBooks Online.

> **Disclaimer**: This guide is for informational purposes only. Prevailing wage laws are complex and vary by jurisdiction. Consult with a qualified attorney, CPA, or payroll specialist before bidding on or performing prevailing wage work. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Understanding Prevailing Wage](#understanding-prevailing-wage)
2. [Davis-Bacon Act Fundamentals](#davis-bacon-act-fundamentals)
3. [State Prevailing Wage Laws](#state-prevailing-wage-laws)
4. [Wage Determination Components](#wage-determination-components)
5. [Certified Payroll Requirements](#certified-payroll-requirements)
6. [WH-347 Form Walkthrough](#wh-347-form-walkthrough)
7. [QBO Setup for Prevailing Wage](#qbo-setup-for-prevailing-wage)
8. [Fringe Benefit Tracking](#fringe-benefit-tracking)
9. [Common Compliance Mistakes](#common-compliance-mistakes)
10. [Best Practices](#best-practices)

---

## Understanding Prevailing Wage

### What is Prevailing Wage?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PREVAILING WAGE EXPLAINED                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  DEFINITION:                                                                 │
│  The wage rate (hourly pay + fringe benefits) that must be paid to          │
│  workers on government-funded construction projects. Rates are set by       │
│  the Department of Labor based on wages paid in the geographic area.        │
│                                                                              │
│  PURPOSE:                                                                    │
│  • Prevent government contracts from driving down local wages               │
│  • Ensure fair competition among bidders                                    │
│  • Protect workers on public projects                                       │
│                                                                              │
│  WHEN IT APPLIES:                                                            │
│  • Federal projects over $2,000 (Davis-Bacon Act)                           │
│  • State/local projects (varies by state threshold)                         │
│  • Projects using federal funding (highways, schools, etc.)                 │
│  • Some private projects with government subsidies                          │
│                                                                              │
│  WHO MUST COMPLY:                                                            │
│  • Prime contractors                                                         │
│  • All subcontractors at any tier                                           │
│  • Owner's direct-hire workers (sometimes)                                  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Why Prevailing Wage Matters for Contractors

```
FINANCIAL IMPACT:

Standard Commercial Project:
  Electrician wage: $28/hour
  Burden (taxes, insurance): $8/hour
  Total labor cost: $36/hour

Prevailing Wage Project (same area):
  Electrician base wage: $42/hour
  Required fringe: $18/hour
  Burden on base: $12/hour
  Total labor cost: $72/hour

Difference: 100% higher labor costs!

BIDDING IMPLICATIONS:
• Must use prevailing wage rates in estimates
• Can't substitute cheaper labor
• Fringe costs add significantly
• Apprentice ratios may be mandated
```

---

## Davis-Bacon Act Fundamentals

### What is Davis-Bacon?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DAVIS-BACON ACT OVERVIEW                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ENACTED: 1931                                                               │
│                                                                              │
│  APPLIES TO:                                                                 │
│  • Federal construction contracts over $2,000                               │
│  • Contracts for construction, alteration, or repair                        │
│  • Public buildings or public works                                         │
│                                                                              │
│  REQUIREMENTS:                                                               │
│  1. Pay at least the prevailing wage rate for each classification           │
│  2. Pay required fringe benefits (or cash equivalent)                       │
│  3. Submit weekly certified payroll reports                                 │
│  4. Post wage determination at job site                                     │
│  5. Maintain payroll records for 3 years                                    │
│                                                                              │
│  RELATED ACTS:                                                               │
│  • Copeland Anti-Kickback Act (no kickbacks from wages)                     │
│  • Contract Work Hours Safety Standards Act (OT requirements)               │
│                                                                              │
│  ENFORCEMENT:                                                                │
│  • Department of Labor - Wage and Hour Division                             │
│  • Contracting agency                                                        │
│  • Can result in contract termination, debarment, back wages                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Davis-Bacon Thresholds and Coverage

```
COVERAGE DETERMINATION:

Question 1: Is it a federal contract?
├── Yes → Continue
└── No → May still have state prevailing wage

Question 2: Is it over $2,000?
├── Yes → Continue
└── No → Davis-Bacon doesn't apply (but state may)

Question 3: Is it construction, alteration, or repair?
├── Yes → Davis-Bacon applies
└── No → Service Contract Act may apply instead

Question 4: Is it a public building or public work?
├── Yes → Davis-Bacon applies
└── No → Check if federal funding triggers "Related Acts"

COMMON FEDERALLY-FUNDED PROJECTS:
• Highway construction (FHWA funding)
• Airport improvements (FAA funding)
• Public housing (HUD funding)
• Water/sewer projects (EPA funding)
• School construction (federal grants)
• Hospital construction (HHS funding)
```

---

## State Prevailing Wage Laws

### State Variations

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    STATE PREVAILING WAGE LAWS                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  STATES WITH PREVAILING WAGE LAWS (as of 2024):                             │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Alaska, Arkansas, California, Colorado, Connecticut, Delaware,             │
│  Hawaii, Illinois, Indiana, Kentucky, Maine, Maryland, Massachusetts,       │
│  Michigan, Minnesota, Missouri, Montana, Nebraska, Nevada, New Jersey,      │
│  New Mexico, New York, Ohio, Oregon, Pennsylvania, Rhode Island,            │
│  Tennessee, Texas, Vermont, Washington, West Virginia, Wisconsin, Wyoming   │
│                                                                              │
│  STATES WITHOUT PREVAILING WAGE (or repealed):                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Alabama, Arizona, Florida, Georgia, Idaho, Iowa, Kansas, Louisiana,        │
│  Mississippi, New Hampshire, North Carolina, North Dakota, Oklahoma,        │
│  South Carolina, South Dakota, Utah, Virginia                               │
│                                                                              │
│  ⚠️ IMPORTANT: Laws change! Verify current status for your state.          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

KEY STATE VARIATIONS:

THRESHOLD AMOUNTS:
• California: $1,000+
• New York: $0 (all public work)
• Texas: $2,000+ (follows Davis-Bacon)
• Illinois: $0 (all public work)

DETERMINATION METHOD:
• Some use union rates
• Some survey actual wages
• Some adopt federal rates
• Some use hybrid approaches

COVERAGE SCOPE:
• Some include maintenance
• Some exclude certain project types
• Some have local (city/county) requirements
```

### Multi-Jurisdiction Compliance

```
SCENARIO: Highway project crossing state lines

Project Location: Kansas City metro (Missouri and Kansas)

Missouri portion:
• State prevailing wage applies
• Missouri rates for Missouri work

Kansas portion:
• No state prevailing wage
• But federal funding = Davis-Bacon applies
• Federal rates for Kansas work

COMPLIANCE REQUIREMENT:
Must track hours by state AND apply correct wage determination!
```

---

## Wage Determination Components

### Reading a Wage Determination

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SAMPLE WAGE DETERMINATION                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  General Decision Number: TX20240001                                        │
│  Superseded General Decision Number: TX20230001                             │
│  State: Texas                                                                │
│  Construction Type: Building                                                 │
│  County: Dallas                                                              │
│  Modification Number: 3                                                      │
│  Publication Date: 01/05/2024                                               │
│                                                                              │
│  CLASSIFICATION                    │ BASIC HOURLY │ FRINGE      │ TOTAL    │
│  ─────────────────────────────────┼──────────────┼─────────────┼──────────│
│  ELECTRICIAN                       │ $38.45       │ $15.23      │ $53.68   │
│  PLUMBER/PIPEFITTER               │ $36.80       │ $14.95      │ $51.75   │
│  CARPENTER                        │ $28.50       │ $11.20      │ $39.70   │
│  LABORER: Common/General          │ $18.25       │ $ 7.45      │ $25.70   │
│  LABORER: Mason Tender            │ $19.50       │ $ 8.10      │ $27.60   │
│  IRONWORKER: Structural           │ $32.40       │ $13.50      │ $45.90   │
│  CEMENT MASON/FINISHER            │ $26.75       │ $10.80      │ $37.55   │
│  OPERATOR: Backhoe/Excavator      │ $30.25       │ $12.15      │ $42.40   │
│  OPERATOR: Crane                  │ $34.60       │ $14.20      │ $48.80   │
│  SHEET METAL WORKER               │ $35.20       │ $14.50      │ $49.70   │
│  HVAC MECHANIC                    │ $34.85       │ $14.30      │ $49.15   │
│  PAINTER                          │ $24.50       │ $ 9.80      │ $34.30   │
│  ROOFER                           │ $25.80       │ $10.35      │ $36.15   │
│  TRUCK DRIVER                     │ $22.40       │ $ 9.00      │ $31.40   │
│                                                                              │
│  APPRENTICE RATES: (See separate schedule below)                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Understanding Fringe Benefits

```
FRINGE BENEFIT COMPONENTS:

The "fringe" portion can include:
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  BONA FIDE FRINGE BENEFITS:                                                 │
│  • Health insurance premiums (medical, dental, vision)                      │
│  • Retirement/pension contributions                                         │
│  • Life insurance                                                            │
│  • Disability insurance                                                      │
│  • Vacation pay                                                              │
│  • Holiday pay                                                               │
│  • Apprenticeship training fund contributions                               │
│                                                                              │
│  NOT CONSIDERED FRINGE:                                                      │
│  • Employer FICA taxes                                                       │
│  • Workers' compensation insurance                                          │
│  • Unemployment insurance                                                    │
│  • Tools or equipment                                                        │
│  • Travel expenses (unless per diem)                                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

FRINGE PAYMENT OPTIONS:

Option 1: Pay to Benefit Plans
  Required fringe: $15.23/hour
  Pay to union health fund: $8.50/hour
  Pay to union pension: $4.25/hour
  Pay to training fund: $1.00/hour
  Total to plans: $13.75/hour
  Cash difference to worker: $1.48/hour

Option 2: All Cash
  Required fringe: $15.23/hour
  No benefit plans provided
  Add $15.23 to base hourly rate
  Worker receives: $38.45 + $15.23 = $53.68/hour gross

Option 3: Hybrid
  Some benefits + cash for remainder
```

### Worker Classifications

```
CLASSIFICATION CHALLENGES:

Common Classification Issues:

1. WORKING FOREMAN
   Does foreman do manual work?
   • More than 20% manual = pay prevailing wage
   • Supervision only = may be exempt

2. MULTI-TRADE WORKERS
   Worker does electrical AND plumbing
   • Track hours by classification
   • Pay higher rate for all hours (conservative)
   • Or split hours accurately by task

3. HELPER vs. LABORER vs. TRADESPERSON
   • Helper: Assists tradesperson, limited scope
   • Laborer: General construction work
   • Tradesperson: Skilled trade work

   When in doubt, use higher classification!

4. APPRENTICE RATIOS
   • May only use apprentices at specified ratios
   • Apprentice must be registered
   • Apprentice rates are % of journeyman

   Example: 1 apprentice per 3 journeymen
   4 journeymen + 2 apprentices = VIOLATION (ratio is 2:1, not 3:1)
```

---

## Certified Payroll Requirements

### What is Certified Payroll?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CERTIFIED PAYROLL REQUIREMENTS                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  DEFINITION:                                                                 │
│  A weekly payroll report submitted to the contracting agency certifying     │
│  that workers on the project were paid prevailing wages.                    │
│                                                                              │
│  SUBMISSION REQUIREMENTS:                                                    │
│  • Submit weekly (within 7 days of pay date)                                │
│  • Include all workers on the project that week                             │
│  • Cover each day worked on the project                                     │
│  • Signed certification statement                                           │
│                                                                              │
│  REQUIRED INFORMATION:                                                       │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Worker name and last 4 of SSN                                            │
│  • Worker address                                                            │
│  • Work classification                                                       │
│  • Hours worked each day                                                     │
│  • Total hours (straight time and overtime)                                 │
│  • Rate of pay (base + fringe breakdown)                                    │
│  • Gross wages                                                               │
│  • Deductions (itemized)                                                     │
│  • Net wages                                                                 │
│                                                                              │
│  RETENTION:                                                                  │
│  • Keep copies for 3 years after project completion                         │
│  • Must be available for DOL inspection                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Weekly Submission Process

```
CERTIFIED PAYROLL WORKFLOW:

Week Ending: Saturday
Payroll Processed: Following Tuesday
Certified Payroll Due: Following Friday (7 days)

┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  MONDAY-SATURDAY: Work performed on project                                 │
│         ↓                                                                    │
│  SUNDAY: Week ends, collect timesheets                                      │
│         ↓                                                                    │
│  MONDAY-TUESDAY: Process payroll                                            │
│         ↓                                                                    │
│  TUESDAY: Payday (or per your schedule)                                     │
│         ↓                                                                    │
│  TUESDAY-WEDNESDAY: Prepare WH-347                                          │
│         ↓                                                                    │
│  THURSDAY: Review and sign certification                                    │
│         ↓                                                                    │
│  FRIDAY: Submit to contracting agency                                       │
│         ↓                                                                    │
│  ONGOING: Retain copy in project file                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## WH-347 Form Walkthrough

### Form Structure

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    WH-347 PAYROLL FORM                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  HEADER SECTION:                                                             │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Name and address of Contractor: ABC Construction, LLC                      │
│                                  123 Builder Lane                            │
│                                  Dallas, TX 75201                            │
│                                                                              │
│  Payroll No: 15          For Week Ending: 03/23/2024                        │
│  Project and Location: City Hall Renovation, 500 Main St, Dallas TX         │
│  Project or Contract No: 2024-PW-0045                                       │
│                                                                              │
│  PAYROLL DATA (Columns):                                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│  (1) Name, Address, SSN (last 4)                                            │
│  (2) Work Classification                                                     │
│  (3) OT/Hours worked (S M T W T F S)                                        │
│  (4) Total Hours (ST / OT)                                                  │
│  (5) Rate of Pay (Base / Fringe)                                            │
│  (6) Gross Amount Earned                                                     │
│  (7) Deductions                                                              │
│  (8) Net Wages Paid                                                          │
│                                                                              │
│  STATEMENT OF COMPLIANCE (Reverse side):                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Certification that:                                                         │
│  • Information is correct and complete                                      │
│  • Wages paid are not less than prevailing rates                            │
│  • Classifications are accurate                                              │
│  • No deductions not permitted by law                                       │
│  • Apprentices are registered (if applicable)                               │
│                                                                              │
│  Signature: ____________________  Date: __________                          │
│  Title: ____________________                                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Sample Completed Entry

```
SAMPLE WH-347 LINE ITEM:

┌─────────────────────────────────────────────────────────────────────────────┐
│ (1) John Smith                                                               │
│     456 Worker Ave, Dallas TX 75202                                         │
│     xxx-xx-1234                                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│ (2) Classification: ELECTRICIAN                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│ (3) Hours:  S  M  T   W   T   F   S                                         │
│      OT:    0  0  0   0   2   0   4                                         │
│      ST:    0  8  8   8   8   8   4                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│ (4) Total Hours: 44 ST / 6 OT                                               │
├─────────────────────────────────────────────────────────────────────────────┤
│ (5) Rate of Pay:                                                             │
│     Basic: $38.45/hr                                                         │
│     Fringe: $15.23/hr (paid to: Health $8.50, Pension $4.25, Cash $2.48)   │
├─────────────────────────────────────────────────────────────────────────────┤
│ (6) Gross Amount Earned:                                                     │
│     ST: 44 hrs × $38.45 = $1,691.80                                         │
│     OT: 6 hrs × $57.68 (1.5x base) = $346.08                                │
│     Fringe (cash): 50 hrs × $2.48 = $124.00                                 │
│     Total Gross: $2,161.88                                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│ (7) Deductions:                                                              │
│     Federal Tax: $324.28                                                     │
│     State Tax: $86.48                                                        │
│     FICA: $165.38                                                            │
│     Union Dues: $25.00                                                       │
│     Total Deductions: $601.14                                               │
├─────────────────────────────────────────────────────────────────────────────┤
│ (8) Net Wages Paid: $1,560.74                                               │
│     Check #: 4521  Date: 03/26/2024                                         │
└─────────────────────────────────────────────────────────────────────────────┘

FRINGE BENEFIT RECONCILIATION:
Required Fringe: $15.23/hr × 50 hrs = $761.50
Paid to Health Fund: $8.50 × 50 = $425.00
Paid to Pension Fund: $4.25 × 50 = $212.50
Cash to Worker: $2.48 × 50 = $124.00
Total Fringe Provided: $761.50 ✓
```

---

## QBO Setup for Prevailing Wage

### QBO Limitations

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QBO PREVAILING WAGE LIMITATIONS                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ⚠️ IMPORTANT: QBO Payroll has significant limitations for prevailing      │
│  wage work. Consider these workarounds or supplemental solutions.           │
│                                                                              │
│  LIMITATIONS:                                                                │
│  ─────────────────────────────────────────────────────────────────────────  │
│  ✗ Cannot track multiple pay rates per employee by project                 │
│  ✗ Cannot automatically calculate fringe benefit requirements               │
│  ✗ No built-in certified payroll (WH-347) generation                       │
│  ✗ Limited classification tracking                                          │
│  ✗ No apprentice ratio monitoring                                           │
│  ✗ Cannot split hours by wage determination                                 │
│                                                                              │
│  WORKAROUND OPTIONS:                                                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Option 1: Dedicated Prevailing Wage Payroll Software                       │
│    • LCPtracker, eMars, Points North                                        │
│    • Handles certified payroll natively                                     │
│    • Export totals to QBO via journal entry                                 │
│                                                                              │
│  Option 2: Manual Tracking + QBO                                            │
│    • Spreadsheet for certified payroll                                      │
│    • Process payroll in QBO at higher rate                                  │
│    • Manual WH-347 preparation                                              │
│                                                                              │
│  Option 3: Payroll Service Bureau                                           │
│    • Use service specializing in construction                               │
│    • They handle certified payroll                                          │
│    • Import totals to QBO                                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Setting Up Pay Items in QBO

```
IF USING QBO PAYROLL FOR PREVAILING WAGE:

Step 1: Create Pay Types for Each Rate
────────────────────────────────────────
Navigation: Payroll → Payroll Settings → Pay Types

Create separate pay types:
• Regular Pay - Standard (your normal rate)
• Regular Pay - Prevailing Wage (PW project rate)
• Overtime - Standard
• Overtime - Prevailing Wage
• Fringe Benefit - Cash (for fringe paid as wages)

Step 2: Create Earnings Codes
─────────────────────────────
For each wage determination classification you use:
• PW - Electrician
• PW - Carpenter
• PW - Laborer
• PW - Operator
• etc.

Step 3: Employee Setup
──────────────────────
For employees working prevailing wage projects:
• Add multiple pay rates
• Assign to appropriate classifications
• Note: May need to adjust per project

Step 4: Time Tracking
─────────────────────
Track time separately by:
• Project (Class in QBO)
• Classification
• Prevailing wage vs. non-prevailing wage
```

### Chart of Accounts Additions

```
ADD THESE ACCOUNTS FOR PREVAILING WAGE TRACKING:

COGS (Direct Costs):
50150  ↳ Labor - Prevailing Wage
50151    ↳ PW - Base Wages
50152    ↳ PW - Fringe Cash
50153    ↳ PW - Fringe Benefits Paid
50160  ↳ Payroll Taxes - Prevailing Wage
50170  ↳ Workers Comp - Prevailing Wage

LIABILITY (for fringe due to funds):
23500  Fringe Benefits Payable
23510  ↳ Union Health Fund Payable
23520  ↳ Union Pension Payable
23530  ↳ Training Fund Payable

This allows you to:
• See true cost of prevailing wage labor
• Track fringe obligations separately
• Compare PW vs. non-PW job costs
```

### Recording Fringe Benefit Payments

```
JOURNAL ENTRY: Fringe Benefits to Union Funds

When paying union/trust funds for fringe benefits:

Date: Monthly (or per fund requirements)
Memo: Fringe benefit payment - Project XYZ - March 2024

Account                              Debit      Credit
────────────────────────────────────────────────────────────────
23510 Union Health Fund Payable                 $4,250.00
23520 Union Pension Payable                     $2,125.00
23530 Training Fund Payable                       $500.00
  10000 Checking - Operating         $6,875.00
────────────────────────────────────────────────────────────────

ORIGINAL ENTRY (when payroll processed):

Account                              Debit      Credit
────────────────────────────────────────────────────────────────
50153 PW - Fringe Benefits Paid     $6,875.00
  23510 Union Health Fund Payable                $4,250.00
  23520 Union Pension Payable                    $2,125.00
  23530 Training Fund Payable                      $500.00
────────────────────────────────────────────────────────────────
Customer/Class: [Assign to PW Project]
```

---

## Fringe Benefit Tracking

### Fringe Calculation Worksheet

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FRINGE BENEFIT CALCULATION                                │
│                    Week Ending: 03/23/2024                                   │
│                    Project: City Hall Renovation                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  REQUIRED FRINGE (from wage determination):                                 │
│                                                                              │
│  Classification     │ Hours │ Rate/Hr │ Required Fringe                     │
│  ───────────────────┼───────┼─────────┼─────────────────                    │
│  Electrician        │  150  │ $15.23  │ $2,284.50                           │
│  Carpenter          │   80  │ $11.20  │   $896.00                           │
│  Laborer            │  200  │ $ 7.45  │ $1,490.00                           │
│  Operator           │   60  │ $12.15  │   $729.00                           │
│  ───────────────────┴───────┴─────────┼─────────────────                    │
│  TOTAL FRINGE REQUIRED:               │ $5,399.50                           │
│                                                                              │
│  FRINGE PROVIDED:                                                            │
│                                                                              │
│  Benefit Type            │ Amount     │ Qualifies? │ Notes                  │
│  ────────────────────────┼────────────┼────────────┼────────────────────    │
│  Health Insurance        │ $2,800.00  │ Yes        │ Employer contribution  │
│  401(k) Match            │   $850.00  │ Yes        │ 3% match               │
│  Paid Vacation (accrued) │   $425.00  │ Yes        │ Per policy             │
│  Paid Holidays (accrued) │   $175.00  │ Yes        │ Per policy             │
│  ────────────────────────┼────────────┼────────────┼────────────────────    │
│  Total Bona Fide Fringe  │ $4,250.00  │            │                        │
│                                                                              │
│  FRINGE SHORTFALL:                                                          │
│  Required:     $5,399.50                                                    │
│  Provided:     $4,250.00                                                    │
│  ─────────────────────────                                                  │
│  Cash Owed:    $1,149.50  ← Must add to worker paychecks                   │
│                                                                              │
│  DISTRIBUTION OF CASH FRINGE:                                               │
│  Electrician: 150 hrs × ($15.23 - $9.64*) = $838.50                        │
│  Carpenter:    80 hrs × ($11.20 - $8.25*) = $236.00                        │
│  Laborer:     200 hrs × ($ 7.45 - $7.45*) = $0.00 (fully covered)          │
│  Operator:     60 hrs × ($12.15 - $9.90*) = $75.00                         │
│  ────────────────────────────────────────────────                           │
│  *Prorated share of bona fide benefits provided                             │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Annualization of Benefits

```
ANNUALIZING BENEFITS FOR HOURLY FRINGE CREDIT:

Health Insurance Example:
Annual premium paid by employer: $12,000
Expected annual hours: 2,080
Hourly credit: $12,000 ÷ 2,080 = $5.77/hour

Vacation Example:
Vacation policy: 2 weeks paid
Hourly rate: $38.45
Annual value: 80 hours × $38.45 = $3,076
Expected annual hours: 2,080
Hourly credit: $3,076 ÷ 2,080 = $1.48/hour

Holiday Example:
Paid holidays: 7 days
Hourly rate: $38.45
Annual value: 56 hours × $38.45 = $2,153
Expected annual hours: 2,080
Hourly credit: $2,153 ÷ 2,080 = $1.04/hour

TOTAL HOURLY FRINGE CREDIT: $5.77 + $1.48 + $1.04 = $8.29/hour

If required fringe is $15.23:
Cash fringe owed: $15.23 - $8.29 = $6.94/hour additional
```

---

## Common Compliance Mistakes

### Top 10 Prevailing Wage Violations

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COMMON PREVAILING WAGE VIOLATIONS                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. WRONG CLASSIFICATION                                                     │
│     Problem: Paying laborer rate for skilled trade work                     │
│     Fix: Classify by work performed, not job title                          │
│                                                                              │
│  2. MISSING FRINGE BENEFITS                                                  │
│     Problem: Paying base rate only, forgetting fringe                       │
│     Fix: Track fringe separately, verify weekly                             │
│                                                                              │
│  3. OVERTIME CALCULATION ERRORS                                              │
│     Problem: Not applying 1.5x to base rate correctly                       │
│     Fix: OT = 1.5 × base rate; fringe stays at 1x                          │
│                                                                              │
│  4. LATE CERTIFIED PAYROLL                                                   │
│     Problem: Submitting WH-347 late or incomplete                           │
│     Fix: Calendar submission deadlines, prepare promptly                    │
│                                                                              │
│  5. APPRENTICE RATIO VIOLATIONS                                              │
│     Problem: Too many apprentices for journeymen on site                    │
│     Fix: Track ratios daily, adjust staffing                                │
│                                                                              │
│  6. UNREGISTERED APPRENTICES                                                 │
│     Problem: Paying apprentice rates to non-registered workers              │
│     Fix: Verify registration before using apprentice rate                   │
│                                                                              │
│  7. IMPROPER DEDUCTIONS                                                      │
│     Problem: Deducting for tools, damages, etc.                             │
│     Fix: Only legally permitted deductions (taxes, benefits)                │
│                                                                              │
│  8. SPLIT CLASSIFICATION ERRORS                                              │
│     Problem: Not tracking hours by classification when worker               │
│              performs multiple types of work                                │
│     Fix: Detailed time tracking by task/classification                      │
│                                                                              │
│  9. USING WRONG WAGE DETERMINATION                                           │
│     Problem: Using outdated or wrong geographic area rates                  │
│     Fix: Verify WD at bid, confirm at project start                        │
│                                                                              │
│  10. SUBCONTRACTOR NON-COMPLIANCE                                            │
│      Problem: Sub doesn't submit certified payroll or underpays             │
│      Fix: Prime is responsible! Collect/verify sub CPRs weekly              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Penalty Consequences

```
POTENTIAL PENALTIES:

BACK WAGES:
• Must pay all underpaid wages to workers
• Plus interest from date wages were due
• Can go back 3 years

LIQUIDATED DAMAGES:
• Up to $27 per day per violation (CWHSSA)
• Applies to overtime violations

WITHHOLDING:
• Contracting agency can withhold contract payments
• Funds held until compliance verified

DEBARMENT:
• Contractor banned from federal contracts
• Typically 3 years
• Devastating for government contractors

CRIMINAL PENALTIES:
• Willful violations can be prosecuted
• Falsifying certified payroll = federal crime
• Up to $10,000 fine and/or imprisonment

EXAMPLE SCENARIO:
────────────────
Underpaid 10 workers by $5/hour for 6 months
• 10 workers × $5/hour × 40 hours × 26 weeks = $52,000 back wages
• Interest and penalties could add 25-50%
• Plus legal fees, audit costs, potential debarment
• Total exposure: $75,000+ (and loss of federal work)
```

---

## Best Practices

### Compliance Checklist

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PREVAILING WAGE COMPLIANCE CHECKLIST                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PRE-BID:                                                                    │
│  □ Obtain correct wage determination for project location                   │
│  □ Identify all classifications needed                                      │
│  □ Calculate fully-burdened labor costs (base + fringe + taxes + WC)       │
│  □ Include certified payroll admin costs in bid                            │
│                                                                              │
│  PROJECT START:                                                              │
│  □ Verify wage determination is still current                               │
│  □ Post wage determination at job site                                      │
│  □ Train field supervisors on classification requirements                   │
│  □ Set up project-specific payroll tracking                                 │
│  □ Confirm subcontractor compliance procedures                              │
│                                                                              │
│  WEEKLY:                                                                     │
│  □ Collect accurate timesheets by classification                           │
│  □ Process payroll with correct rates                                       │
│  □ Calculate and pay fringe benefits (or cash equivalent)                  │
│  □ Prepare WH-347 certified payroll                                        │
│  □ Collect subcontractor certified payrolls                                □
│  □ Submit to contracting agency by deadline                                □
│  □ File copies in project records                                          │
│                                                                              │
│  MONTHLY:                                                                    │
│  □ Reconcile fringe benefit payments to funds                              │
│  □ Verify apprentice ratios maintained                                      │
│  □ Review for any classification issues                                     │
│  □ Confirm all subcontractor CPRs received                                 │
│                                                                              │
│  PROJECT CLOSE:                                                              │
│  □ Final certified payroll submitted                                        │
│  □ All fringe benefits paid/reconciled                                     │
│  □ Subcontractor compliance verified                                        │
│  □ Records organized for retention (3 years minimum)                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Recommended Third-Party Tools

```
CERTIFIED PAYROLL SOFTWARE OPTIONS:

┌──────────────────┬───────────────────────────────────────────────────────┐
│ Product          │ Features                                              │
├──────────────────┼───────────────────────────────────────────────────────┤
│ LCPtracker       │ • Cloud-based certified payroll                       │
│                  │ • WH-347 generation                                   │
│                  │ • Subcontractor management                            │
│                  │ • Agency submission portals                           │
├──────────────────┼───────────────────────────────────────────────────────┤
│ Points North     │ • Full prevailing wage compliance                     │
│                  │ • Fringe benefit tracking                             │
│                  │ • Apprentice management                               │
│                  │ • Mobile time entry                                   │
├──────────────────┼───────────────────────────────────────────────────────┤
│ eMars            │ • Certified payroll reporting                         │
│                  │ • Multi-state compliance                              │
│                  │ • DIR (California) integration                        │
│                  │ • EEO reporting                                       │
├──────────────────┼───────────────────────────────────────────────────────┤
│ Elation Systems  │ • Prevailing wage calculations                        │
│                  │ • Fringe benefit administration                       │
│                  │ • Union reporting                                     │
│                  │ • Integration with payroll systems                    │
└──────────────────┴───────────────────────────────────────────────────────┘

INTEGRATION WITH QBO:
Most of these systems can export journal entry summaries that you import
to QBO for your general ledger. This gives you:
• Specialized PW compliance in the dedicated system
• Clean financial records in QBO
• Best of both worlds
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PREVAILING WAGE QUICK REFERENCE                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TOTAL HOURLY COST = Base Rate + Fringe + Employer Taxes + WC              │
│                                                                              │
│  OVERTIME CALCULATION:                                                       │
│  OT Rate = (Base Rate × 1.5) + Fringe (at 1x) + Taxes on OT wages          │
│                                                                              │
│  CERTIFIED PAYROLL DUE: Within 7 days of pay date                          │
│                                                                              │
│  RECORD RETENTION: 3 years after project completion                        │
│                                                                              │
│  KEY FORMS:                                                                  │
│  • WH-347: Certified Payroll form                                          │
│  • WH-348: Statement of Compliance (or reverse of WH-347)                  │
│  • SF-1444: Request for Authorization of Additional Classification          │
│                                                                              │
│  WAGE DETERMINATION LOOKUP:                                                  │
│  sam.gov → Wage Determinations → Search by state/county/type               │
│                                                                              │
│  APPRENTICE REQUIREMENTS:                                                    │
│  • Must be registered with DOL or state agency                             │
│  • Must follow approved apprentice schedule                                 │
│  • Must maintain proper ratios                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With prevailing wage compliance understood:
- [Time Tracking & Payroll](./03-time-tracking-payroll.md) - Labor costing workflows
- [Job Costing Setup](../tutorials/03-job-costing-setup.md) - Tracking costs by project
- [Subcontractor Management](./02-subcontractor-1099-lien-waivers.md) - Sub compliance

---

*[Back to Main Guide](../../README.md)*
