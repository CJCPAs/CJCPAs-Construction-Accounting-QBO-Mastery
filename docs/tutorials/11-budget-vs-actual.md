# Budget vs. Actual Reporting for Construction

## Overview

Budget vs. Actual analysis is the core of construction project management. It answers the critical question: **"Are we making or losing money on this job?"**

This guide covers how to set up budgets, track actual costs, analyze variances, and take corrective action—all within QuickBooks Online.

---

## Why Budget vs. Actual Matters

### The Construction Profitability Challenge

```
WITHOUT BUDGET TRACKING:

Job awarded: $500,000
You think: "Great, we'll make money!"

...6 months later...

Final cost: $520,000
You discover: "We lost $20,000 😱"

BUT IT'S TOO LATE TO FIX!
```

```
WITH BUDGET TRACKING:

Job awarded: $500,000
Budget: $400,000 (20% margin)

Month 2: Budget $80,000, Actual $95,000 ⚠️
ALERT: 19% over budget

ACTION: Investigate, course-correct
Final cost: $420,000 (after fixing issues)
Profit: $80,000 ✓

CAUGHT EARLY, FIXED IN TIME!
```

### Key Benefits

| Benefit | Impact |
|---------|--------|
| **Early warning** | Catch problems while fixable |
| **Accountability** | PMs responsible for budgets |
| **Better estimating** | Learn from variances |
| **Cash flow planning** | Know costs ahead of time |
| **WIP accuracy** | Reliable cost-to-complete |
| **Bonding support** | Sureties love good tracking |

---

## The Construction Budget Structure

### Cost Code Hierarchy

```
PROJECT BUDGET STRUCTURE

CONTRACT VALUE                           $500,000
├── DIRECT COSTS (Budget: $400,000)
│   ├── 01 - LABOR                       $120,000 (30%)
│   │   ├── 01.1 Supervision              $30,000
│   │   ├── 01.2 Carpentry                $50,000
│   │   ├── 01.3 General Labor            $25,000
│   │   └── 01.4 Overtime Allowance       $15,000
│   │
│   ├── 02 - MATERIALS                   $140,000 (35%)
│   │   ├── 02.1 Lumber/Wood              $60,000
│   │   ├── 02.2 Concrete                 $35,000
│   │   ├── 02.3 Hardware                 $25,000
│   │   └── 02.4 Other Materials          $20,000
│   │
│   ├── 03 - SUBCONTRACTORS             $100,000 (25%)
│   │   ├── 03.1 Electrical               $35,000
│   │   ├── 03.2 Plumbing                 $30,000
│   │   ├── 03.3 HVAC                     $25,000
│   │   └── 03.4 Other Subs               $10,000
│   │
│   ├── 04 - EQUIPMENT                    $25,000 (6%)
│   │   ├── 04.1 Rental Equipment         $15,000
│   │   └── 04.2 Owned Equipment Charges  $10,000
│   │
│   └── 05 - OTHER DIRECT                 $15,000 (4%)
│       ├── 05.1 Permits/Fees              $5,000
│       ├── 05.2 Temporary Facilities      $5,000
│       └── 05.3 Miscellaneous             $5,000
│
└── GROSS PROFIT                        $100,000 (20%)
```

### Budget Timeline

```
BUDGET TIMING

  Pre-Bid         Award           Start        Monthly        Completion
     │              │               │             │              │
     ▼              ▼               ▼             ▼              ▼
┌─────────┐   ┌─────────┐   ┌─────────────┐   ┌───────────┐   ┌─────────┐
│ Initial │   │ Revised │   │ Production  │   │ Variance  │   │ Final   │
│Estimate │──▶│ Budget  │──▶│   Budget    │──▶│ Analysis  │──▶│Analysis │
└─────────┘   └─────────┘   └─────────────┘   └───────────┘   └─────────┘
     │              │               │               │              │
 Bid amount    Refine for      Break into       Compare to      Compare
 calculation   contract        monthly/phase    actual, fix     final to
               value           targets          problems        budget
```

---

## Setting Up Budgets in QBO

### QBO Budget Options

**Option 1: QBO Native Budgets (Limited)**
- Company-level budgets only
- Not project-specific
- Good for overhead budgeting

**Option 2: Projects Budget Feature (QBO Advanced)**
- Limited project budgeting
- Basic comparison capability
- Better than nothing

**Option 3: External Budget + QBO Actuals (Recommended)**
- Detailed budget in Excel
- Track actuals in QBO
- Compare in Excel or reporting tool
- Most flexibility

### Setting Up a QBO Company Budget

**HOW (for Overhead Budgeting):**

1. Go to **Settings ⚙️** → **Budgeting**
2. Click **Add Budget**
3. Configure:
   - **Fiscal Year:** Select year
   - **Interval:** Monthly (recommended)
   - **Pre-fill:** From prior year actuals (optional)
4. Enter budget amounts by account by month
5. Save

**Use For:**
- G&A expense budgets
- Revenue targets
- Cash flow planning

### Setting Up Job Budgets in Excel

Since QBO's project budgeting is limited, most contractors track job budgets externally.

**Job Budget Template:**

```
JOB BUDGET WORKSHEET
─────────────────────────────────────────────────────────────────────────────────
Project: Smith Residence Renovation
Contract Value: $500,000
Start Date: March 1, 2024
Est. Completion: August 31, 2024

COST CATEGORY                  BUDGET      ACTUAL      VARIANCE    % VAR
─────────────────────────────────────────────────────────────────────────────────
LABOR
  Supervision                  $30,000    $32,500      ($2,500)    -8.3%
  Carpentry                    $50,000    $48,200       $1,800      3.6%
  General Labor                $25,000    $27,800      ($2,800)   -11.2%
  Overtime                     $15,000    $12,000       $3,000     20.0%
─────────────────────────────────────────────────────────────────────────────────
  TOTAL LABOR                 $120,000   $120,500        ($500)    -0.4%
─────────────────────────────────────────────────────────────────────────────────

MATERIALS
  Lumber/Wood                  $60,000    $58,400       $1,600      2.7%
  Concrete                     $35,000    $38,200      ($3,200)    -9.1%
  Hardware                     $25,000    $24,100         $900      3.6%
  Other Materials              $20,000    $21,500      ($1,500)    -7.5%
─────────────────────────────────────────────────────────────────────────────────
  TOTAL MATERIALS             $140,000   $142,200      ($2,200)    -1.6%
─────────────────────────────────────────────────────────────────────────────────

SUBCONTRACTORS
  Electrical                   $35,000    $34,000       $1,000      2.9%
  Plumbing                     $30,000    $36,500      ($6,500)   -21.7% ⚠️
  HVAC                         $25,000    $25,000           $0      0.0%
  Other Subs                   $10,000     $8,500       $1,500     15.0%
─────────────────────────────────────────────────────────────────────────────────
  TOTAL SUBCONTRACTORS        $100,000   $104,000      ($4,000)    -4.0%
─────────────────────────────────────────────────────────────────────────────────

EQUIPMENT
  Rental Equipment             $15,000    $14,200         $800      5.3%
  Owned Equipment              $10,000     $9,500         $500      5.0%
─────────────────────────────────────────────────────────────────────────────────
  TOTAL EQUIPMENT              $25,000    $23,700       $1,300      5.2%
─────────────────────────────────────────────────────────────────────────────────

OTHER DIRECT
  Permits/Fees                  $5,000     $5,200        ($200)    -4.0%
  Temporary Facilities          $5,000     $4,800         $200      4.0%
  Miscellaneous                 $5,000     $6,100      ($1,100)   -22.0% ⚠️
─────────────────────────────────────────────────────────────────────────────────
  TOTAL OTHER DIRECT           $15,000    $16,100      ($1,100)    -7.3%
─────────────────────────────────────────────────────────────────────────────────

═════════════════════════════════════════════════════════════════════════════════
TOTAL DIRECT COSTS            $400,000   $406,500      ($6,500)    -1.6%
═════════════════════════════════════════════════════════════════════════════════

CONTRACT VALUE                $500,000
TOTAL DIRECT COSTS            $406,500
─────────────────────────────────────────────────────────────────────────────────
GROSS PROFIT                   $93,500   (Budget: $100,000)
GROSS MARGIN                    18.7%    (Budget: 20.0%)
─────────────────────────────────────────────────────────────────────────────────

STATUS: ⚠️ 1.3% below target margin - investigate plumbing and misc overruns
```

---

## Tracking Actuals in QBO

### Ensuring Accurate Job Costing

For budget vs. actual to work, every cost must be coded to the correct job and cost category.

**QBO Setup Requirements:**

1. **Customer/Project for each job**
2. **Consistent account structure** matching budget categories
3. **Every cost transaction includes:**
   - Customer/Project
   - Class (if using for cost type)
   - Correct expense/COGS account

### Getting Actuals from QBO

**Method 1: P&L by Customer Report**

1. Go to **Reports** → "Profit and Loss by Customer"
2. Set date range (project start to current date)
3. Filter to specific customer/project
4. Export to Excel

**Method 2: Transaction Detail by Account**

1. Go to **Reports** → "Transaction Detail by Account"
2. Filter by Customer/Project
3. Group by Account
4. Shows every transaction for analysis

**Method 3: Project Profitability Report (QBO Advanced)**

1. Go to **Reports** → "Project Profitability"
2. Select project
3. Shows income, costs, profit

### Mapping QBO Accounts to Budget Categories

**Example Mapping:**

| Budget Category | QBO Account(s) |
|-----------------|----------------|
| Labor - Supervision | 50100 Direct Labor - Supervision |
| Labor - Carpentry | 50110 Direct Labor - Carpenter |
| Labor - General | 50120 Direct Labor - Laborer |
| Materials - Lumber | 51100 Materials - Lumber |
| Materials - Concrete | 51200 Materials - Concrete |
| Subcontractors - Electrical | 52100 Subcontractors - Electrical |
| Subcontractors - Plumbing | 52200 Subcontractors - Plumbing |
| Equipment - Rental | 53100 Equipment Rental |
| Equipment - Owned | 53200 Equipment Charges |
| Other - Permits | 54100 Permits and Fees |

---

## Variance Analysis

### Understanding Variances

```
VARIANCE TYPES

FAVORABLE VARIANCE (Under Budget)
  Budget: $50,000
  Actual: $45,000
  Variance: $5,000 FAVORABLE

  Means: Spent less than planned
  Could indicate: Efficient work, lower prices, scope reduction

UNFAVORABLE VARIANCE (Over Budget)
  Budget: $50,000
  Actual: $58,000
  Variance: ($8,000) UNFAVORABLE

  Means: Spent more than planned
  Could indicate: Problems, scope creep, poor estimating, waste
```

### Variance Analysis Framework

For each significant variance, ask:

1. **What happened?** - Identify the cause
2. **Why did it happen?** - Root cause analysis
3. **Can it be fixed?** - Recovery options
4. **Will it happen again?** - Remaining risk
5. **What's the cost impact?** - Final profit effect

### Common Variance Causes

**Labor Variances:**

| Variance | Possible Causes |
|----------|-----------------|
| Over on hours | Rework, inefficiency, weather delays |
| Over on rate | Overtime, skill mix, wage increases |
| Under on hours | Better productivity, scope reduction |
| Under on rate | Better skill mix, less overtime |

**Material Variances:**

| Variance | Possible Causes |
|----------|-----------------|
| Over on quantity | Waste, theft, design changes |
| Over on price | Price increases, rush orders |
| Under on quantity | Better yield, value engineering |
| Under on price | Better buying, volume discounts |

**Subcontractor Variances:**

| Variance | Possible Causes |
|----------|-----------------|
| Over budget | Change orders, bid mistakes, added scope |
| Under budget | Negotiated savings, scope reduction |

---

## Budget vs. Actual Reporting

### Weekly Job Cost Report

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                    WEEKLY JOB COST REPORT                                        │
│                    Week Ending: November 24, 2024                                │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│  PROJECT: Smith Residence                                                        │
│  PM: John Smith                                                                  │
│  % Complete: 65%                                                                 │
│                                                                                  │
│  COST SUMMARY                                                                    │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │                    BUDGET     ACTUAL     VARIANCE    %      THIS WEEK    │   │
│  │                    TO DATE    TO DATE    TO DATE     VAR    COSTS        │   │
│  │  ──────────────────────────────────────────────────────────────────────  │   │
│  │  Labor            $78,000    $80,500    ($2,500)   -3.2%    $8,200       │   │
│  │  Materials        $91,000    $93,200    ($2,200)   -2.4%    $12,500      │   │
│  │  Subcontractors   $65,000    $69,000    ($4,000)   -6.2%    $15,000      │   │
│  │  Equipment        $16,250    $15,400       $850     5.2%    $1,800       │   │
│  │  Other             $9,750    $10,200      ($450)   -4.6%      $800       │   │
│  │  ──────────────────────────────────────────────────────────────────────  │   │
│  │  TOTAL COSTS     $260,000   $268,300    ($8,300)   -3.2%   $38,300       │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  PROJECTED FINAL                                                                 │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │  Original Budget:           $400,000                                     │   │
│  │  Current Forecast:          $412,769  (based on % complete)              │   │
│  │  Projected Over/(Under):    ($12,769)                                    │   │
│  │                                                                          │   │
│  │  Original Gross Profit:     $100,000 (20.0%)                             │   │
│  │  Projected Gross Profit:     $87,231 (17.4%)                             │   │
│  │  Profit Variance:           ($12,769)                                    │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  VARIANCE EXPLANATIONS                                                           │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │  1. Subcontractor Over ($4,000):                                         │   │
│  │     - Plumbing change order for relocated fixtures ($6,500)              │   │
│  │     - Offset by electrical savings ($2,500)                              │   │
│  │     - Status: Change order submitted to owner for approval               │   │
│  │                                                                          │   │
│  │  2. Labor Over ($2,500):                                                 │   │
│  │     - Weather delays week of 11/11 (2 days lost)                         │   │
│  │     - Overtime to catch up                                               │   │
│  │     - Status: Back on schedule, monitoring                               │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  ACTION ITEMS                                                                    │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │  □ Follow up on plumbing CO approval by 11/27                            │   │
│  │  □ Review remaining sub bids for potential savings                       │   │
│  │  □ Monitor labor productivity through project end                        │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  Prepared by: _________________ Date: ________                                   │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### Earned Value Analysis (EVA)

**Advanced budget tracking using earned value:**

```
EARNED VALUE METRICS

Budget at Completion (BAC):     $400,000 (original budget)
Planned Value (PV):             $260,000 (budget for work scheduled to date)
Earned Value (EV):              $260,000 (budget for work actually completed)
Actual Cost (AC):               $268,300 (actual costs incurred)

KEY METRICS:

Cost Variance (CV) = EV - AC
CV = $260,000 - $268,300 = ($8,300)
Interpretation: $8,300 over budget for work completed

Cost Performance Index (CPI) = EV / AC
CPI = $260,000 / $268,300 = 0.969
Interpretation: Getting $0.97 of work for every $1.00 spent

Schedule Variance (SV) = EV - PV
SV = $260,000 - $260,000 = $0
Interpretation: On schedule

Estimate at Completion (EAC) = BAC / CPI
EAC = $400,000 / 0.969 = $412,800
Interpretation: Projected final cost

Variance at Completion (VAC) = BAC - EAC
VAC = $400,000 - $412,800 = ($12,800)
Interpretation: Projected to be $12,800 over budget

```

### Visual Variance Report

```
BUDGET vs ACTUAL - VISUAL SUMMARY

Category      Budget     Actual      ◄─── Variance Bar ───►

Labor         $78,000    $80,500     ████████████████████░░  -3.2%
Materials     $91,000    $93,200     █████████████████████░  -2.4%
Subs          $65,000    $69,000     ███████████████████████ -6.2% ⚠️
Equipment     $16,250    $15,400     ██████████████████      +5.2%
Other          $9,750    $10,200     ████████████████████░░  -4.6%
              ─────────────────────────────────────────────────────
TOTAL        $260,000   $268,300     ████████████████████░░  -3.2%

Legend: █ = Actual spend as % of budget
        ░ = Over budget warning
        ⚠️ = Significant variance (>5%)
```

---

## Monthly Budget Review Process

### Budget Review Meeting Agenda

**Frequency:** Monthly (at minimum)
**Attendees:** Owner, PM, Estimator, Bookkeeper
**Duration:** 30-60 minutes per major project

**Agenda:**

1. **Financial Summary (5 min)**
   - Contract value (including approved COs)
   - Costs to date
   - % Complete
   - Billings to date

2. **Budget vs. Actual Review (15 min)**
   - Walk through each cost category
   - Highlight significant variances
   - Explain causes

3. **Projection Update (10 min)**
   - Estimated cost to complete
   - Projected final cost
   - Projected gross profit

4. **Risk Discussion (10 min)**
   - What could still go wrong?
   - Remaining scope uncertainties
   - Mitigation strategies

5. **Action Items (5 min)**
   - Who does what by when
   - Follow-up items from last meeting

### Monthly Job Cost Review Checklist

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                    MONTHLY JOB COST REVIEW                                       │
│                    Project: _______________  Month: _______                      │
├─────────────────────────────────────────────────────────────────────────────────┤
│                                                                                  │
│  PRE-MEETING PREP                                                                │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │ □ Pull P&L by Customer from QBO                                          │   │
│  │ □ Update budget vs. actual spreadsheet                                   │   │
│  │ □ Calculate % complete                                                   │   │
│  │ □ Get PM estimate of cost to complete                                    │   │
│  │ □ List all variances > 5%                                                │   │
│  │ □ Prepare variance explanations                                          │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  KEY METRICS                                                                     │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │ Contract Value (w/COs):    $_____________                                │   │
│  │ Original Budget:           $_____________                                │   │
│  │ Revised Budget:            $_____________                                │   │
│  │ Costs to Date:             $_____________                                │   │
│  │ % Complete:                _______%                                      │   │
│  │ Est. Cost to Complete:     $_____________                                │   │
│  │ Projected Final Cost:      $_____________                                │   │
│  │ Projected Gross Profit:    $_____________  (_____%)                      │   │
│  │                                                                          │   │
│  │ Status: □ On Track  □ Watch  □ Problem                                   │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  SIGNIFICANT VARIANCES (>5%)                                                     │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │ Category: _____________ Variance: $_________ (____%)                     │   │
│  │ Explanation: ___________________________________________________         │   │
│  │ Recovery Plan: _________________________________________________         │   │
│  │                                                                          │   │
│  │ Category: _____________ Variance: $_________ (____%)                     │   │
│  │ Explanation: ___________________________________________________         │   │
│  │ Recovery Plan: _________________________________________________         │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  ACTION ITEMS                                                                    │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │ □ ___________________________________ Owner: _______ Due: _______        │   │
│  │ □ ___________________________________ Owner: _______ Due: _______        │   │
│  │ □ ___________________________________ Owner: _______ Due: _______        │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
│                                                                                  │
│  Reviewed by: _________________ Date: ________                                   │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Taking Corrective Action

### When Variances Require Action

| Variance Level | Action Required |
|----------------|-----------------|
| **< 5%** | Monitor, no immediate action |
| **5-10%** | Investigate, develop recovery plan |
| **10-20%** | Immediate management attention |
| **> 20%** | Crisis mode, major intervention |

### Corrective Action Options

**For Labor Overruns:**
1. Reduce crew size if overstaffed
2. Work smarter (better sequencing)
3. Reduce overtime
4. Bring in more productive workers
5. Adjust remaining schedule

**For Material Overruns:**
1. Review remaining material orders
2. Negotiate better prices
3. Reduce waste
4. Value engineer remaining work
5. Submit change order if design issue

**For Subcontractor Overruns:**
1. Review remaining sub scopes
2. Get competitive bids for remaining work
3. Identify back-charges if appropriate
4. Submit change order if scope changed
5. Negotiate fixed prices for remaining work

### Recovery Plan Template

```
VARIANCE RECOVERY PLAN

Project: _______________
Issue: _______________
Current Variance: $_______
Target Recovery: $_______

RECOVERY ACTIONS:

Action 1: _________________________________________________
  Owner: ____________  Due: ____________
  Expected Savings: $_______

Action 2: _________________________________________________
  Owner: ____________  Due: ____________
  Expected Savings: $_______

Action 3: _________________________________________________
  Owner: ____________  Due: ____________
  Expected Savings: $_______

Total Expected Recovery: $_______
Remaining Variance After Recovery: $_______

Reviewed by: ____________  Date: ____________
```

---

## Budget vs. Actual Best Practices

### Do's

1. **Budget before starting** - Don't skip this step
2. **Update budgets for changes** - Approved COs change the baseline
3. **Review weekly** - Catch issues early
4. **Require explanations** - No unexplained variances
5. **Document lessons learned** - Improve future estimates
6. **Compare to similar jobs** - Historical benchmarking
7. **Include contingency** - But track it separately

### Don'ts

1. **Don't hide variances** - Problems don't age well
2. **Don't blame estimating** - Fix going forward
3. **Don't ignore small variances** - They add up
4. **Don't wait until job is done** - Too late to fix
5. **Don't skip the meeting** - Accountability matters
6. **Don't use "one-time" excuses repeatedly** - Find root causes

---

## Linking Budget to WIP Schedule

### How Budget Feeds WIP

```
BUDGET → WIP CONNECTION

Budget provides:
  • Total Estimated Cost (for % complete calculation)
  • Cost to Complete estimate

QBO Actuals provide:
  • Costs to Date

WIP calculation:
  % Complete = Costs to Date ÷ Total Estimated Cost
  Earned Revenue = Contract Value × % Complete
  Over/(Under) Billing = Billings to Date - Earned Revenue
```

### Monthly Budget-to-WIP Process

1. **Update budget** with PM input
2. **Pull actuals** from QBO
3. **Calculate variances**
4. **Revise cost-to-complete**
5. **Update Total Estimated Cost**
6. **Feed to WIP schedule**
7. **Calculate new % complete**
8. **Update earned revenue**

---

## Technology Tips

### Excel Budget Template

**Key Features:**
- Project info header
- Cost categories matching QBO accounts
- Budget column (from estimate)
- Actual column (from QBO export)
- Variance formulas
- % variance formulas
- Conditional formatting (red for >10% over)
- Summary section
- Charts/graphs

### Automating Budget vs. Actual

**QBO Export Automation:**
1. Run P&L by Customer
2. Export to Excel
3. Use VLOOKUP/INDEX-MATCH to pull into budget template
4. Refresh monthly

**Third-Party Tools:**
- Knowify (construction-specific)
- Buildertrend
- Procore
- Construction Partner
- Sage 100 Contractor

---

## Key Takeaways

1. **Every job needs a budget** - No exceptions
2. **Track at the category level** - Not just total cost
3. **Review weekly minimum** - Monthly is too late for construction
4. **Explain every variance** - Accountability drives performance
5. **Take action early** - Variances don't fix themselves
6. **Learn from every job** - Improve estimating over time
7. **Connect to WIP** - Budget accuracy = WIP accuracy

---

## Next Steps

- For WIP schedules → [WIP Schedules](./04-wip-schedules.md)
- For job costing setup → [Job Costing Setup](./03-job-costing-setup.md)
- For cash flow → [Cash Flow Forecasting](./10-cash-flow-forecasting.md)
- For monthly close → [Month-End Close Checklist](../checklists/11-month-end-close.md)

---

*[← Previous: Cash Flow Forecasting](./10-cash-flow-forecasting.md) | [Next: Troubleshooting →](../reference/13-troubleshooting-faq.md)*
