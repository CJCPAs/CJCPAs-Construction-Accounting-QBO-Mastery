# Time Tracking and Payroll Integration for Construction

## Overview

Time tracking is the bridge between field work and accurate job costing. This guide covers setting up time tracking in QuickBooks Online, integrating with payroll, and ensuring labor costs flow correctly to jobs.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Payroll and labor laws vary by state and locality. Consult with a qualified payroll specialist and employment attorney. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Why Time Tracking Matters](#why-time-tracking-matters)
2. [QBO Time Tracking Setup](#qbo-time-tracking-setup)
3. [Employee Time Entry](#employee-time-entry)
4. [Service Items for Labor](#service-items-for-labor)
5. [Payroll Integration](#payroll-integration)
6. [Job Costing from Timesheets](#job-costing-from-timesheets)
7. [Construction-Specific Considerations](#construction-specific-considerations)
8. [Third-Party Time Tracking Apps](#third-party-time-tracking-apps)
9. [Best Practices and Troubleshooting](#best-practices-and-troubleshooting)

---

## Why Time Tracking Matters

### The Labor Cost Problem

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LABOR COST CHALLENGE                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Labor is typically 30-50% of construction costs.                           │
│  Without accurate time tracking:                                             │
│                                                                              │
│  ❌ Can't calculate true job profitability                                  │
│  ❌ Can't bid future jobs accurately                                        │
│  ❌ Can't identify productivity issues                                      │
│  ❌ May violate wage and hour laws                                          │
│  ❌ Payroll costs hit overhead, not jobs                                    │
│                                                                              │
│  EXAMPLE: 10-Person Crew                                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Weekly payroll: $25,000                                                     │
│  Annual payroll: $1,300,000                                                  │
│                                                                              │
│  Without job tracking:                                                       │
│  • $1.3M shows as "Labor Expense"                                           │
│  • No visibility into cost per job                                          │
│  • Job profits/losses hidden                                                │
│                                                                              │
│  With job tracking:                                                          │
│  • Smith Residence: $85,000 labor (within budget ✅)                        │
│  • Johnson Remodel: $62,000 labor (over budget ❌)                          │
│  • Martinez Custom: $45,000 labor (on track ✅)                             │
│  • Immediately see problem jobs                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Time Tracking Flow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TIME TO JOB COST FLOW                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   FIELD                     OFFICE                    ACCOUNTING            │
│   ─────                     ──────                    ──────────            │
│                                                                              │
│   Employee works    →   Time reviewed/    →   Payroll         →  Job       │
│   on Job Site           approved               processed          Costing   │
│                                                                              │
│   ┌───────────┐        ┌───────────┐        ┌───────────┐     ┌─────────┐  │
│   │ Time      │   →    │ Supervisor│   →    │ Payroll   │  →  │ P&L by  │  │
│   │ Entry     │        │ Approval  │        │ Run       │     │ Job     │  │
│   │           │        │           │        │           │     │         │  │
│   │ • Hours   │        │ • Verify  │        │ • Gross   │     │ Labor   │  │
│   │ • Job     │        │   hours   │        │   wages   │     │ cost by │  │
│   │ • Task    │        │ • Correct │        │ • Taxes   │     │ job     │  │
│   │ • Notes   │        │   errors  │        │ • Net pay │     │         │  │
│   └───────────┘        └───────────┘        └───────────┘     └─────────┘  │
│                                                                              │
│   Data captured:                                                             │
│   • Who worked                                                               │
│   • Hours worked (regular + OT)                                              │
│   • Which job                                                                │
│   • What work type                                                           │
│   • Notes/details                                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## QBO Time Tracking Setup

### Enabling Time Tracking

**Step 1: Enable in Settings**

```
Navigation: ⚙️ Gear → Account and Settings → Advanced → Time tracking

Configure:
┌─────────────────────────────────────────────────────────────────────────────┐
│  TIME TRACKING SETTINGS                                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Add Service field to timesheets: ON ✅                                     │
│  └── Allows specifying labor type (Framing, Electrical, etc.)               │
│                                                                              │
│  Make Single-Time Activity Billable: ON                                      │
│  └── For Time & Materials billing                                            │
│                                                                              │
│  First day of work week: Monday                                              │
│  └── Matches typical construction schedule                                  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Step 2: Set Up Employees**

```
Navigation: Payroll → Employees (or Workers → Employees if no payroll)

For each employee, verify:
□ Name correct
□ Pay type: Hourly or Salary
□ Hourly rate set (if hourly)
□ Overtime settings correct
□ Job costing enabled
```

**Step 3: Create Service Items for Labor**

```
Navigation: ⚙️ Gear → Products and Services → New

Create service items for labor categories:
┌─────────────────────────────────────────────────────────────────────────────┐
│  LABOR SERVICE ITEMS                                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Name                │  Type     │  Rate     │  Income Account              │
│  ────────────────────┼───────────┼───────────┼─────────────────────────────│
│  Labor - General     │  Service  │  $45/hr   │  40100 Labor Revenue         │
│  Labor - Carpentry   │  Service  │  $55/hr   │  40100 Labor Revenue         │
│  Labor - Electrical  │  Service  │  $65/hr   │  40100 Labor Revenue         │
│  Labor - Plumbing    │  Service  │  $65/hr   │  40100 Labor Revenue         │
│  Labor - Supervision │  Service  │  $75/hr   │  40100 Labor Revenue         │
│                                                                              │
│  Note: Rates are BILLING rates (what you charge customer)                   │
│  Payroll tracks COST rate (what you pay employee)                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Employee Time Entry

### Time Entry in QBO

**Method 1: Single Time Activity**

```
Navigation: + New → Single Time Activity

┌─────────────────────────────────────────────────────────────────────────────┐
│  SINGLE TIME ACTIVITY                                         [Save] [X]    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Name: [Mike Johnson ▼]                                                      │
│  └── Select employee from dropdown                                          │
│                                                                              │
│  Date: [03/15/2024]                                                          │
│                                                                              │
│  Service: [Labor - Carpentry ▼]                                             │
│  └── What type of work performed                                            │
│                                                                              │
│  Customer: [Smith Family Trust ▼]                                           │
│  └── Which customer/job                                                     │
│                                                                              │
│  Project: [2024-001 Smith Residence ▼]                                      │
│  └── If using Projects feature                                              │
│                                                                              │
│  Billable: [✓] $55.00/hr                                                    │
│  └── Check if billing customer (T&M jobs)                                   │
│      Uncheck for fixed-price jobs (cost tracking only)                      │
│                                                                              │
│  Start/End Time: 7:00 AM - 3:30 PM                                          │
│  Break deducted: 30 min                                                      │
│  Duration: 8:00 hrs                                                          │
│                                                                              │
│  Description: Framed second floor exterior walls                            │
│                                                                              │
│  Class: [2024-001 Smith Residence ▼]                                        │
│  └── For job costing (in addition to Customer)                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Method 2: Weekly Timesheet**

```
Navigation: + New → Weekly Timesheet

┌─────────────────────────────────────────────────────────────────────────────┐
│  WEEKLY TIMESHEET - Mike Johnson                              [Save] [X]    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Name: [Mike Johnson ▼]        Week of: March 11 - 17, 2024                 │
│                                                                              │
│  ┌────────────────────────────────────────────────────────────────────┐     │
│  │ Details          │ Mon │ Tue │ Wed │ Thu │ Fri │ Sat │ Sun │ Total│     │
│  ├──────────────────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼──────┤     │
│  │ Customer: Smith  │     │     │     │     │     │     │     │      │     │
│  │ Service: Carpent │  8  │  8  │  8  │  8  │  4  │     │     │  36  │     │
│  │ Class: 2024-001  │     │     │     │     │     │     │     │      │     │
│  │ Billable: □      │     │     │     │     │     │     │     │      │     │
│  ├──────────────────┼─────┼─────┼─────┼─────┼─────┼─────┼─────┼──────┤     │
│  │ Customer: Johnson│     │     │     │     │     │     │     │      │     │
│  │ Service: Carpent │     │     │     │     │  4  │     │     │   4  │     │
│  │ Class: 2024-002  │     │     │     │     │     │     │     │      │     │
│  │ Billable: □      │     │     │     │     │     │     │     │      │     │
│  ├──────────────────┴─────┴─────┴─────┴─────┴─────┴─────┴─────┼──────┤     │
│  │                                           WEEKLY TOTAL:   │  40  │     │
│  └────────────────────────────────────────────────────────────┴──────┘     │
│                                                                              │
│  [+ Add row]                                                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Time Entry Best Practices for Field Workers

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FIELD TIME ENTRY OPTIONS                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  OPTION 1: PAPER TIMESHEETS (Traditional)                                   │
│  ───────────────────────────────────────                                     │
│  • Workers fill out paper timesheets daily                                  │
│  • Foreman collects and reviews                                             │
│  • Office enters into QBO weekly                                            │
│                                                                              │
│  Pros: Works without technology, familiar                                   │
│  Cons: Data entry burden, potential for errors, delayed                     │
│                                                                              │
│  OPTION 2: QBO WORKFORCE APP                                                 │
│  ────────────────────────────                                                │
│  • Employees use QuickBooks Workforce mobile app                            │
│  • Clock in/out from phone                                                   │
│  • Select customer/job from list                                            │
│  • GPS tracking available                                                    │
│                                                                              │
│  Pros: Direct entry, real-time data, GPS verification                       │
│  Cons: Requires smartphone, cell service, training                          │
│                                                                              │
│  OPTION 3: THIRD-PARTY APP (QuickBooks Time/TSheets)                        │
│  ──────────────────────────────────────────────────                          │
│  • Specialized time tracking app                                             │
│  • Advanced features: geofencing, photo clock-in                            │
│  • Syncs to QBO automatically                                               │
│                                                                              │
│  Pros: Best features, construction-friendly                                 │
│  Cons: Additional cost, another system to manage                            │
│                                                                              │
│  OPTION 4: INTEGRATED PROJECT SOFTWARE                                       │
│  ──────────────────────────────────────                                      │
│  • Procore, Buildertrend, CoConstruct                                       │
│  • Time tracking built into project management                              │
│  • Export/sync to QBO                                                        │
│                                                                              │
│  Pros: Single system for field, all data in one place                       │
│  Cons: Cost, complexity, may need customization                             │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Service Items for Labor

### Setting Up Labor Cost Accounts

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LABOR ACCOUNT STRUCTURE                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  COST OF GOODS SOLD (Job Costs):                                            │
│  ─────────────────────────────────                                           │
│  50400 - Direct Labor                                                        │
│  ├── 50410 - Field Labor - Wages                                            │
│  ├── 50420 - Field Labor - Payroll Taxes                                    │
│  ├── 50430 - Field Labor - Workers Comp                                     │
│  └── 50440 - Field Labor - Benefits                                         │
│                                                                              │
│  OPERATING EXPENSES (Overhead):                                              │
│  ─────────────────────────────────                                           │
│  62000 - Payroll Expenses                                                    │
│  ├── 62100 - Office Salaries                                                │
│  ├── 62200 - Office Payroll Taxes                                           │
│  └── 62300 - Office Benefits                                                │
│                                                                              │
│  WHY SEPARATE?                                                               │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • 50400 accounts are job costs (in COGS, affect gross profit)              │
│  • 62000 accounts are overhead (in OpEx, affect net profit)                 │
│  • Field labor should hit job costs                                          │
│  • Office staff should hit overhead                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Payroll Items to Expense Accounts

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PAYROLL ITEM MAPPING                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  FIELD EMPLOYEES (Job-coded):                                                │
│  ─────────────────────────────                                               │
│  Payroll Component        →  Account              →  Class                  │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Regular Hours            →  50410 Field Wages    →  [From timesheet]       │
│  Overtime Hours           →  50410 Field Wages    →  [From timesheet]       │
│  Employer FICA            →  50420 Field PR Tax   →  [From timesheet]       │
│  Employer Medicare        →  50420 Field PR Tax   →  [From timesheet]       │
│  State Unemployment       →  50420 Field PR Tax   →  [Allocated or direct]  │
│  Federal Unemployment     →  50420 Field PR Tax   →  [Allocated or direct]  │
│  Workers Comp             →  50430 Field WC       →  [From timesheet]       │
│  Health Insurance         →  50440 Field Benefits →  [Allocated]            │
│                                                                              │
│  OFFICE EMPLOYEES (Not job-coded):                                           │
│  ──────────────────────────────────                                          │
│  Payroll Component        →  Account              →  Class                  │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Salary/Wages             →  62100 Office Wages   →  OVERHEAD               │
│  Employer FICA            →  62200 Office PR Tax  →  OVERHEAD               │
│  etc.                     →  ...                  →  OVERHEAD               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Payroll Integration

### QBO Payroll Time Import

If using QuickBooks Payroll with time tracking:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PAYROLL TIME IMPORT PROCESS                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WEEKLY WORKFLOW:                                                            │
│                                                                              │
│  Day 1-5 (Mon-Fri): Employees enter time                                    │
│  ─────────────────────────────────────────                                   │
│  • Time entered via app, web, or paper → office entry                       │
│  • Each entry includes: Employee, Date, Hours, Job, Service                 │
│                                                                              │
│  Day 6 (Sat or Mon): Time review and approval                               │
│  ──────────────────────────────────────────                                  │
│  Navigation: Payroll → Time → Review time                                   │
│                                                                              │
│  Verify:                                                                     │
│  □ Total hours reasonable                                                   │
│  □ Jobs assigned correctly                                                  │
│  □ Overtime calculated correctly                                            │
│  □ No missing entries                                                       │
│                                                                              │
│  Make corrections as needed                                                  │
│                                                                              │
│  Day 7 (Mon): Run payroll                                                   │
│  ─────────────────────────                                                   │
│  Navigation: Payroll → Run payroll                                          │
│                                                                              │
│  1. Select pay period                                                        │
│  2. Time automatically imports                                               │
│  3. Review each employee:                                                    │
│     • Regular hours                                                          │
│     • Overtime hours                                                         │
│     • Job allocation                                                         │
│  4. Add any manual adjustments                                               │
│  5. Preview payroll                                                          │
│  6. Submit payroll                                                           │
│                                                                              │
│  Result: Hours flow to job costs via timesheet job assignments              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Job Costing Setup in QBO Payroll

**Enable Job Costing:**

```
Navigation: Payroll → Payroll Settings → Job Costing

Toggle: Track billable labor costs ON ✅

Configure:
┌─────────────────────────────────────────────────────────────────────────────┐
│  JOB COSTING OPTIONS                                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Track hours by customer: ON ✅                                             │
│  └── Required for job costing                                               │
│                                                                              │
│  Track hours by service: ON ✅                                              │
│  └── For labor type breakdown                                               │
│                                                                              │
│  Track hours by class: ON ✅                                                │
│  └── For class-based job costing                                            │
│                                                                              │
│  Labor cost rate includes:                                                   │
│  ☑️ Wages                                                                   │
│  ☑️ Payroll taxes                                                           │
│  ☑️ Employer contributions                                                  │
│  └── For "true" labor cost per job                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Burdened Labor Cost

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    UNDERSTANDING BURDENED LABOR COST                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TRUE LABOR COST = Wage + Burden                                            │
│                                                                              │
│  WAGE: What employee earns                                                   │
│  • Regular hourly rate: $25.00/hr                                           │
│  • Overtime rate: $37.50/hr (1.5x)                                          │
│                                                                              │
│  BURDEN: Additional employer costs                                           │
│  • FICA (Social Security + Medicare): 7.65%                                 │
│  • Federal Unemployment (FUTA): 0.6%                                        │
│  • State Unemployment (SUTA): varies (e.g., 2.7%)                           │
│  • Workers' Comp: varies (e.g., 5% for carpentry)                           │
│  • Health Insurance: varies (e.g., $500/month = $2.88/hr)                   │
│  • Other benefits: varies                                                    │
│                                                                              │
│  EXAMPLE CALCULATION:                                                        │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Mike Johnson - Carpenter                                                    │
│  Base Wage:                                    $25.00/hr                    │
│  FICA (7.65%):                                 $1.91                        │
│  FUTA (0.6%):                                  $0.15                        │
│  SUTA (2.7%):                                  $0.68                        │
│  Workers Comp (5%):                            $1.25                        │
│  Health Insurance ($500/173 hrs):              $2.89                        │
│  ────────────────────────────────────────────────────────                   │
│  BURDENED LABOR RATE:                          $31.88/hr                    │
│                                                                              │
│  This is the TRUE cost of Mike on a job.                                    │
│  Use burdened rate for job cost estimates and analysis.                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Job Costing from Timesheets

### How Time Becomes Job Costs

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TIME → JOB COST FLOW                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. TIME ENTRY                                                               │
│     ┌─────────────────────────────────────────────────────────────────┐     │
│     │ Employee: Mike Johnson                                          │     │
│     │ Date: 03/15/2024                                                │     │
│     │ Hours: 8                                                         │     │
│     │ Customer: Smith Family Trust                                    │     │
│     │ Class: 2024-001 Smith Residence                                 │     │
│     │ Service: Labor - Carpentry                                      │     │
│     └─────────────────────────────────────────────────────────────────┘     │
│                              │                                               │
│                              ▼                                               │
│  2. PAYROLL PROCESSES                                                        │
│     ┌─────────────────────────────────────────────────────────────────┐     │
│     │ Mike's paycheck:                                                │     │
│     │ 8 hrs × $25.00 = $200.00 gross                                 │     │
│     │                                                                  │     │
│     │ Employer costs:                                                  │     │
│     │ FICA: $15.30                                                    │     │
│     │ FUTA/SUTA: $6.60                                                │     │
│     │ Workers Comp: $10.00                                            │     │
│     │ Total burden: $31.90                                            │     │
│     └─────────────────────────────────────────────────────────────────┘     │
│                              │                                               │
│                              ▼                                               │
│  3. JOB COST RESULT                                                          │
│     ┌─────────────────────────────────────────────────────────────────┐     │
│     │ 50410 Field Labor - Wages                                       │     │
│     │   DEBIT: $200.00                                                │     │
│     │   Class: 2024-001 Smith Residence                               │     │
│     │                                                                  │     │
│     │ 50420 Field Labor - PR Tax                                      │     │
│     │   DEBIT: $21.90                                                 │     │
│     │   Class: 2024-001 Smith Residence                               │     │
│     │                                                                  │     │
│     │ 50430 Field Labor - WC                                          │     │
│     │   DEBIT: $10.00                                                 │     │
│     │   Class: 2024-001 Smith Residence                               │     │
│     └─────────────────────────────────────────────────────────────────┘     │
│                                                                              │
│  RESULT: $231.90 labor cost charged to Smith Residence                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Viewing Labor Costs by Job

**Report: Profit and Loss by Class**

```
Navigation: Reports → Profit and Loss by Class

Customize:
• Date range: Current month/quarter/year
• Display: Active classes only

Sample Output:
┌─────────────────────────────────────────────────────────────────────────────┐
│                     PROFIT AND LOSS BY CLASS                                 │
│                     January 1 - March 31, 2024                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│                        Smith      Johnson    Martinez    OVERHEAD    TOTAL  │
│                        Res.       Remodel    Custom                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Contract Revenue    $175,000    $95,000    $45,000           -   $315,000  │
│                                                                              │
│  Cost of Revenue                                                             │
│    Materials          $52,500    $28,500    $13,500           -    $94,500  │
│    Subcontractors     $35,000    $19,000    $9,000            -    $63,000  │
│    Field Labor        $38,500    $24,700    $11,200           -    $74,400  │
│      - Wages           31,500     20,200     9,200            -     60,900  │
│      - PR Taxes         4,850      3,100     1,400            -      9,350  │
│      - Workers Comp     2,150      1,400       600            -      4,150  │
│    Equipment           $5,000     $2,800    $1,300            -     $9,100  │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Gross Profit         $44,000    $20,000   $10,000           -    $74,000  │
│  Gross Margin %         25.1%      21.1%     22.2%            -      23.5%  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Report: Time Activities by Customer**

```
Navigation: Reports → Time Activities by Customer Detail

Shows hours worked by job with rates
```

---

## Construction-Specific Considerations

### Overtime Distribution

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    OVERTIME JOB ALLOCATION                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  SCENARIO:                                                                   │
│  Mike works 50 hours in a week:                                              │
│  • Mon-Thu: Smith Residence (32 hours)                                      │
│  • Fri: Johnson Remodel (10 hours)                                          │
│  • Sat: Martinez Custom (8 hours)                                           │
│                                                                              │
│  QUESTION: Which job gets charged overtime?                                  │
│                                                                              │
│  METHOD 1: CHRONOLOGICAL (Most Common)                                       │
│  ─────────────────────────────────────                                       │
│  Overtime charged to jobs worked after 40 hours:                            │
│  • Smith: 32 hours regular                                                   │
│  • Johnson: 8 hours regular + 2 hours OT                                    │
│  • Martinez: 8 hours OT                                                      │
│                                                                              │
│  METHOD 2: PRO-RATA                                                          │
│  ─────────────────                                                           │
│  Overtime spread proportionally:                                             │
│  Total hours: 50, OT hours: 10                                              │
│  OT % = 20%                                                                  │
│  • Smith: 32 hrs (25.6 reg + 6.4 OT)                                        │
│  • Johnson: 10 hrs (8 reg + 2 OT)                                           │
│  • Martinez: 8 hrs (6.4 reg + 1.6 OT)                                       │
│                                                                              │
│  METHOD 3: SPECIFIC JOB                                                      │
│  ──────────────────────                                                      │
│  Charge all OT to job that caused it                                        │
│  (e.g., if Saturday was rush request from Martinez)                         │
│                                                                              │
│  RECOMMENDATION: Use Method 1 (Chronological) for simplicity                │
│  QBO default behavior follows chronological method                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Certified Payroll Requirements

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CERTIFIED PAYROLL OVERVIEW                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT IS CERTIFIED PAYROLL?                                                  │
│  ─────────────────────────                                                   │
│  Weekly payroll report required on federal (Davis-Bacon) and                │
│  state (Prevailing Wage) public works projects.                             │
│                                                                              │
│  REQUIREMENTS:                                                               │
│  • Submit WH-347 form (or state equivalent) weekly                          │
│  • Report all workers and actual hours on project                           │
│  • Pay prevailing wage rates (set by DOL or state)                          │
│  • Sign under penalty of perjury                                            │
│                                                                              │
│  QBO AND CERTIFIED PAYROLL:                                                  │
│  ─────────────────────────────────────────────────────────────────────────  │
│  QBO does NOT generate certified payroll reports natively.                  │
│                                                                              │
│  Options:                                                                    │
│  1. Export time data from QBO, manually prepare WH-347                      │
│  2. Use third-party certified payroll software:                             │
│     • eBuildex                                                               │
│     • LCP Tracker                                                            │
│     • Elation Systems                                                        │
│  3. Use payroll service with certified payroll add-on                       │
│                                                                              │
│  TIME TRACKING REQUIREMENTS:                                                  │
│  • Track hours by specific project (not just customer)                      │
│  • Track hours by classification (Carpenter, Laborer, etc.)                 │
│  • Track regular vs overtime hours separately                               │
│  • Accurate daily records required                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Multi-Job Days

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    HANDLING MULTI-JOB DAYS                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  SCENARIO: Carpenter works at two job sites in one day                      │
│                                                                              │
│  Morning: Smith Residence (4 hours)                                          │
│  Afternoon: Johnson Remodel (4 hours)                                        │
│                                                                              │
│  OPTION 1: MULTIPLE TIME ENTRIES                                             │
│  ────────────────────────────────                                            │
│  Create separate time entry for each job:                                    │
│  Entry 1: Mike Johnson, Smith, 4 hrs, 7:00-11:00                            │
│  Entry 2: Mike Johnson, Johnson, 4 hrs, 12:00-4:00                          │
│                                                                              │
│  Best for: Accurate job costing                                              │
│                                                                              │
│  OPTION 2: SINGLE ENTRY WITH SPLIT                                           │
│  ─────────────────────────────────                                           │
│  Use weekly timesheet with multiple rows:                                    │
│  Row 1: Smith - 4 hrs on Monday                                              │
│  Row 2: Johnson - 4 hrs on Monday                                            │
│                                                                              │
│  CONSIDERATIONS:                                                             │
│  • Include travel time between jobs (charge to second job or overhead)      │
│  • Note any job-specific breaks or delays                                   │
│  • Ensure total hours reconcile                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Third-Party Time Tracking Apps

### QuickBooks Time (formerly TSheets)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QUICKBOOKS TIME OVERVIEW                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  FEATURES:                                                                   │
│  ─────────                                                                   │
│  ✅ Mobile app for iOS/Android                                              │
│  ✅ GPS tracking                                                            │
│  ✅ Geofencing (auto clock in/out at job site)                              │
│  ✅ Photo clock-in (facial recognition)                                     │
│  ✅ Job/task assignment                                                     │
│  ✅ Manager approvals                                                       │
│  ✅ Real-time job costing                                                   │
│  ✅ Overtime alerts                                                         │
│  ✅ Direct sync to QBO Payroll                                              │
│                                                                              │
│  PRICING (as of 2024):                                                       │
│  ─────────────────────                                                       │
│  • Premium: $10/month base + $8/user                                        │
│  • Elite: $20/month base + $10/user                                         │
│                                                                              │
│  SETUP STEPS:                                                                │
│  ─────────────                                                               │
│  1. Subscribe to QuickBooks Time                                            │
│  2. Connect to QBO (Apps → Find Apps → QuickBooks Time)                     │
│  3. Sync customers/jobs from QBO                                            │
│  4. Add employees and invite to mobile app                                  │
│  5. Configure job/task lists                                                │
│  6. Set approval workflow                                                    │
│  7. Map sync settings (time → payroll)                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Other Time Tracking Apps

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ALTERNATIVE TIME TRACKING APPS                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  CLOCKIFY                                                                    │
│  ─────────                                                                   │
│  • Free tier available                                                       │
│  • Web, desktop, and mobile apps                                            │
│  • QBO integration via Zapier or manual export                              │
│  • Good for: Smaller teams, budget-conscious                                │
│                                                                              │
│  BUSYBUSY                                                                    │
│  ─────────                                                                   │
│  • Construction-specific                                                     │
│  • GPS tracking, facial recognition                                          │
│  • Equipment tracking                                                        │
│  • Integrates with QBO                                                       │
│  • Good for: Construction-focused features                                  │
│                                                                              │
│  RHUMBIX / HCSS                                                              │
│  ──────────────                                                              │
│  • Heavy construction focused                                                │
│  • Certified payroll built-in                                               │
│  • Equipment/materials tracking                                              │
│  • Good for: Larger contractors, prevailing wage                            │
│                                                                              │
│  BUILDERTREND / PROCORE                                                      │
│  ─────────────────────                                                       │
│  • Project management platforms                                              │
│  • Time tracking as part of suite                                           │
│  • QBO integrations available                                               │
│  • Good for: Comprehensive project management                               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Best Practices and Troubleshooting

### Time Tracking Best Practices

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TIME TRACKING BEST PRACTICES                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. CAPTURE TIME DAILY                                                       │
│     • Enter time same day as work performed                                  │
│     • Don't wait until end of week (memory fades)                           │
│     • Real-time entry via mobile app is best                                │
│                                                                              │
│  2. REQUIRE JOB ASSIGNMENT                                                   │
│     • Every hour must have a job/customer                                   │
│     • Use "OVERHEAD" or "SHOP" class for non-job time                       │
│     • Never leave time unassigned                                            │
│                                                                              │
│  3. VERIFY BEFORE PAYROLL                                                    │
│     • Supervisors review time before processing                             │
│     • Check for reasonableness (40-50 hrs typical)                          │
│     • Verify job assignments match actual work                              │
│                                                                              │
│  4. USE CONSISTENT CATEGORIES                                                │
│     • Standard service items (Carpentry, Electrical, etc.)                  │
│     • Train employees on correct selections                                 │
│     • Don't create too many categories                                      │
│                                                                              │
│  5. TRACK NON-BILLABLE TIME                                                  │
│     • Travel, training, shop time                                            │
│     • Helps understand true labor utilization                               │
│     • Charge to OVERHEAD class                                              │
│                                                                              │
│  6. DOCUMENT OVERTIME                                                        │
│     • Note reason for overtime                                               │
│     • Approval before working OT                                            │
│     • Helps with job cost analysis                                          │
│                                                                              │
│  7. REGULAR REPORTS                                                          │
│     • Weekly: Hours by employee, hours by job                               │
│     • Monthly: Labor cost by job, overtime analysis                         │
│     • Quarterly: Labor as % of revenue by job type                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Problems and Solutions

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TROUBLESHOOTING                                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PROBLEM: Labor costs not showing on job reports                            │
│  ────────────────────────────────────────────                                │
│  Causes:                                                                     │
│  • Class not assigned on time entry                                          │
│  • Payroll expense accounts not mapped to COGS                              │
│  • Report filtering out labor accounts                                       │
│                                                                              │
│  Fix:                                                                        │
│  1. Check time entries have Class assigned                                  │
│  2. Verify payroll settings route to 50xxx accounts                         │
│  3. Edit report to include all expense accounts                             │
│                                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  PROBLEM: Time not importing to payroll                                     │
│  ─────────────────────────────────────────                                   │
│  Causes:                                                                     │
│  • Time entries not approved                                                 │
│  • Employee not set up for time tracking                                    │
│  • Pay period mismatch                                                       │
│                                                                              │
│  Fix:                                                                        │
│  1. Approve all time entries before payroll                                 │
│  2. Verify employee record has time tracking enabled                        │
│  3. Check pay period dates match time entry dates                           │
│                                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  PROBLEM: Overtime not calculating correctly                                │
│  ─────────────────────────────────────────────                               │
│  Causes:                                                                     │
│  • Overtime rules not configured                                             │
│  • Weekly hours spread across pay periods                                   │
│  • State OT rules different from federal                                    │
│                                                                              │
│  Fix:                                                                        │
│  1. Check payroll OT settings                                               │
│  2. Verify pay period alignment                                             │
│  3. Configure state-specific rules (e.g., CA daily OT)                      │
│                                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  PROBLEM: Hours don't match job site records                                │
│  ─────────────────────────────────────────────                               │
│  Causes:                                                                     │
│  • Time entry errors                                                         │
│  • Different people tracking time                                           │
│  • Breaks/lunch not handled consistently                                    │
│                                                                              │
│  Fix:                                                                        │
│  1. Implement single source of truth for time                               │
│  2. Train all employees on time entry                                       │
│  3. Standardize break/lunch handling                                        │
│  4. Daily reconciliation of field vs. system hours                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TIME TRACKING QUICK REFERENCE                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ENABLE TIME TRACKING:                                                       │
│  ⚙️ → Account and Settings → Advanced → Time tracking                       │
│                                                                              │
│  ENTER TIME:                                                                 │
│  + New → Single Time Activity (or Weekly Timesheet)                         │
│                                                                              │
│  REQUIRED FIELDS:                                                            │
│  • Employee name                                                             │
│  • Date and hours                                                            │
│  • Customer/Job                                                              │
│  • Class (for job costing)                                                  │
│  • Service (labor type)                                                     │
│                                                                              │
│  REVIEW TIME:                                                                │
│  Payroll → Time → Review time                                               │
│                                                                              │
│  KEY REPORTS:                                                                │
│  • Time Activities by Employee Detail                                       │
│  • Time Activities by Customer Detail                                       │
│  • Profit and Loss by Class (for labor costs)                               │
│                                                                              │
│  BEST PRACTICE: Require job assignment on EVERY time entry                  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With time tracking configured:
- [Job Costing Setup](../tutorials/03-job-costing-setup.md) - Complete job costing
- [Payroll Integration Details](../integrations/01-construction-integrations.md) - App connections
- [Reporting Guide](../reporting/01-essential-reports.md) - Labor cost analysis

---

*[Back to Main Guide](../../README.md)*
