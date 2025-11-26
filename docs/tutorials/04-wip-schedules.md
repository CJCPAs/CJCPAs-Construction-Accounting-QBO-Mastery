# WIP Schedules & Percentage-of-Completion Accounting

## Overview

Work-in-Progress (WIP) schedules are the heartbeat of construction financial management. They tell you how much revenue you've actually earned (regardless of billing), whether you're over or under-billed, and provide the data your bonding company needs.

This chapter provides a complete tutorial on WIP accounting, percentage-of-completion logic, and over/under billing mechanics.

---

## The Critical Question WIP Answers

> **"How much have I actually EARNED on each job?"**

This seems simple, but it's not:
- You might have billed $200,000 but only earned $150,000 (over-billed)
- You might have billed $100,000 but earned $150,000 (under-billed)
- Your bank balance doesn't tell you either

WIP schedules provide the true answer.

---

## Understanding Percentage of Completion (POC)

### The GAAP Foundation

> **ASC 606 / ASC 340-10**: Revenue from long-term contracts should be recognized over time when the entity's performance creates or enhances an asset that the customer controls, or when the entity's performance creates an asset with no alternative use and the entity has an enforceable right to payment.

**Translation for Contractors**: If you're building something for a customer and they're obligated to pay you as you go, you recognize revenue as you perform the work—not when you bill and not when you receive cash.

### The Two Methods of POC

#### Method 1: Cost-to-Cost (Most Common)

```
% Complete = Costs Incurred to Date ÷ Total Estimated Costs
```

**Example:**
- Total Estimated Cost: $800,000
- Costs Incurred to Date: $320,000
- **% Complete: $320,000 ÷ $800,000 = 40%**

**WHY Cost-to-Cost?**
- Costs are objective and measurable
- Auditable with invoices and time records
- Most accepted by sureties and CPAs

#### Method 2: Units of Work (Alternative)

```
% Complete = Units Completed ÷ Total Units
```

**Example (Road Construction):**
- Total Linear Feet: 10,000
- Feet Completed: 4,000
- **% Complete: 4,000 ÷ 10,000 = 40%**

**WHY Use Units of Work?**
- Some projects have measurable units (miles, linear feet, apartments)
- Can be more accurate for repetitive work
- May differ from cost % (if some units cost more than others)

### Calculating Earned Revenue

```
Earned Revenue = Contract Price × % Complete
```

**Full Example:**
```
Contract Price:        $1,000,000
Total Estimated Cost:    $800,000
Costs Incurred:          $320,000
Billings to Date:        $380,000

% Complete = $320,000 ÷ $800,000 = 40%
Earned Revenue = $1,000,000 × 40% = $400,000
Gross Profit Earned = $400,000 - $320,000 = $80,000
```

---

## Over/Under Billing: The Heart of WIP

### What is Over-Billing?

> **Over-Billing**: When you've billed more than you've earned based on percentage of completion.

**Calculation:**
```
Billings to Date > Earned Revenue = OVER-BILLED

Over-Billing Amount = Billings to Date - Earned Revenue
```

**Example:**
```
Earned Revenue:        $400,000
Billings to Date:      $450,000
Over-Billing:          $50,000 ← You've billed $50K more than you've earned
```

**WHY This Matters:**

1. **It's a Liability**: You owe the customer $50,000 worth of work
2. **Balance Sheet Impact**: Shows as "Billings in Excess of Costs" (liability)
3. **Cash Flow Positive**: You have the customer's money before doing the work
4. **Bonding Concern**: Heavy over-billing can indicate front-loading or cash problems

### What is Under-Billing?

> **Under-Billing**: When you've earned more than you've billed based on percentage of completion.

**Calculation:**
```
Earned Revenue > Billings to Date = UNDER-BILLED

Under-Billing Amount = Earned Revenue - Billings to Date
```

**Example:**
```
Earned Revenue:        $400,000
Billings to Date:      $350,000
Under-Billing:         $50,000 ← You've earned $50K more than you've billed
```

**WHY This Matters:**

1. **It's an Asset**: The customer owes you $50,000 (even if not invoiced yet)
2. **Balance Sheet Impact**: Shows as "Costs in Excess of Billings" (asset)
3. **Cash Flow Negative**: You're financing the customer's project
4. **Collection Risk**: If you don't bill it, you may never collect it

### The Over/Under Billing Spectrum

```
                           Under-Billed                    Over-Billed
                                │                              │
    ────────────────────────────┼──────────────────────────────┼────────────────────────
                                │                              │
    ASSET (Good for net worth)  │                              │  LIABILITY
    BAD for cash flow           │   PERFECTLY BILLED           │  GOOD for cash flow
    Financing customer's job    │   (Rare!)                    │  Customer financing you
    Risk: May not collect       │                              │  Risk: May have to give back
                                │                              │
```

### Balance Sheet Presentation

**Correct GAAP Presentation:**

```
BALANCE SHEET (Construction Company)

CURRENT ASSETS
  Cash                                    $xxx,xxx
  Accounts Receivable                     $xxx,xxx
  Costs in Excess of Billings            $xxx,xxx  ← Under-Billing
    (on uncompleted contracts)
  
CURRENT LIABILITIES
  Accounts Payable                        $xxx,xxx
  Billings in Excess of Costs            $xxx,xxx  ← Over-Billing
    (on uncompleted contracts)
```

**WHY Separate Lines?**
- Can't net over and under-billing from different jobs
- Each project's status must be analyzed separately
- Some jobs over-billed, some under-billed—both show on B/S

---

## Building a WIP Schedule: Step-by-Step

### WIP Schedule Components

Every WIP schedule contains these columns:

| Column | Source | Purpose |
|--------|--------|---------|
| **Contract Price** | Original contract + approved COs | Total revenue potential |
| **Est. Cost to Complete** | Budget - Costs to Date | Remaining cost forecast |
| **Total Est. Cost** | Costs to Date + Est. to Complete | Full project cost forecast |
| **Est. Gross Profit** | Contract - Total Est. Cost | Expected total profit |
| **Costs to Date** | QBO job cost reports | Actual costs incurred |
| **% Complete** | Costs to Date ÷ Total Est. Cost | Progress measure |
| **Earned Revenue** | Contract × % Complete | GAAP revenue |
| **Billings to Date** | QBO customer balance | Amounts invoiced |
| **Over/(Under) Billing** | Billings - Earned Revenue | Billing position |

### Step 1: Gather Data from QBO

**HOW to Extract Job Cost Data:**

1. Go to **Reports** → "Profit and Loss by Customer"
2. Set date range: From project start to current date
3. Filter to specific project
4. Export to Excel

**Data You Need:**
- Total Income (Billings to Date)
- Total Cost of Goods Sold (Costs to Date)

**HOW to Get Contract Values:**

Since QBO doesn't have native contract tracking:
- Option A: Maintain contract register in Excel
- Option B: Create custom field in QBO for contract value
- Option C: Use Estimates as contracts (partial solution)

### Step 2: Build the WIP Schedule in Excel

**HOW to Create a WIP Template:**

Create a spreadsheet with these columns (download template in Templates section):

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                            WIP SCHEDULE - [DATE]                                                          │
├───────┬───────────────┬──────────┬─────────────┬──────────────┬───────────┬──────────┬─────────┬─────────┬────────────────┤
│ Job # │ Contract      │ Est Cost │ Total Est   │ Est Gross    │ Costs to  │ %        │ Earned  │ Billings│ Over/(Under)   │
│       │ Price         │ Complete │ Cost        │ Profit       │ Date      │ Complete │ Revenue │ to Date │ Billing        │
├───────┼───────────────┼──────────┼─────────────┼──────────────┼───────────┼──────────┼─────────┼─────────┼────────────────┤
│ A     │ $1,000,000    │ $480,000 │ $800,000    │ $200,000     │ $320,000  │ 40%      │ $400,000│ $380,000│ ($20,000)      │
│ B     │ $500,000      │ $200,000 │ $400,000    │ $100,000     │ $200,000  │ 50%      │ $250,000│ $280,000│ $30,000        │
│ C     │ $750,000      │ $450,000 │ $600,000    │ $150,000     │ $150,000  │ 25%      │ $187,500│ $150,000│ ($37,500)      │
├───────┼───────────────┼──────────┼─────────────┼──────────────┼───────────┼──────────┼─────────┼─────────┼────────────────┤
│ TOTAL │ $2,250,000    │$1,130,000│ $1,800,000  │ $450,000     │ $670,000  │ --       │ $837,500│ $810,000│ ($27,500)      │
└───────┴───────────────┴──────────┴─────────────┴──────────────┴───────────┴──────────┴─────────┴─────────┴────────────────┘

Summary:
  Total Under-Billing (Asset):     $57,500  [Jobs A + C]
  Total Over-Billing (Liability):  $30,000  [Job B]
  Net Under-Billing (Asset):       $27,500
```

### Step 3: Key Formulas

```excel
# Percentage Complete
=Costs_to_Date / Total_Est_Cost

# Earned Revenue
=Contract_Price * Percent_Complete

# Over/(Under) Billing
=Billings_to_Date - Earned_Revenue
  Positive = Over-Billed (liability)
  Negative = Under-Billed (asset)

# Estimated Gross Profit
=Contract_Price - Total_Est_Cost

# Gross Profit Earned
=Earned_Revenue - Costs_to_Date
```

### Step 4: Reconcile to QBO

**CRITICAL**: Your WIP schedule must reconcile to QBO

**Reconciliation Checklist:**
- [ ] Total Costs to Date = Total COGS per QBO for active projects
- [ ] Total Billings to Date = Total AR + Collections for active projects
- [ ] Any differences are explained and documented

---

## Setting Up WIP Tracking in QBO

### Creating WIP Balance Sheet Accounts

**HOW:**

Go to **Settings ⚙️** → **Chart of Accounts** → **New**

| Account # | Name | Type | Detail Type | Description |
|-----------|------|------|-------------|-------------|
| 12500 | Costs in Excess of Billings | Other Current Assets | Other Current Assets | Under-billing on contracts |
| 12510 | ↳ CIE - Project A | Other Current Assets | Other Current Assets | Under-billing detail |
| 24500 | Billings in Excess of Costs | Other Current Liabilities | Other Current Liabilities | Over-billing on contracts |
| 24510 | ↳ BIE - Project B | Other Current Liabilities | Other Current Liabilities | Over-billing detail |

### Monthly WIP Adjustment Journal Entry

At month-end, after completing your WIP schedule, you'll make an adjusting entry:

**Scenario: Your WIP shows net under-billing increased from $20,000 to $27,500**

```
Date: [Month End]
Memo: WIP Adjustment per WIP Schedule dated [date]

Account                           Debit        Credit
─────────────────────────────────────────────────────
Costs in Excess of Billings      $7,500
  Contract Revenue                            $7,500
─────────────────────────────────────────────────────
To recognize revenue earned in excess of billings
```

**Scenario: Your WIP shows net over-billing increased from $10,000 to $30,000**

```
Date: [Month End]
Memo: WIP Adjustment per WIP Schedule dated [date]

Account                           Debit        Credit
─────────────────────────────────────────────────────
Contract Revenue                 $20,000
  Billings in Excess of Costs                $20,000
─────────────────────────────────────────────────────
To defer revenue billed but not yet earned
```

---

## The WHY Behind WIP: GAAP Deep Dive

### Revenue Recognition Principles

> **ASC 606-10-25-27**: An entity shall recognize revenue when (or as) the entity satisfies a performance obligation by transferring a promised good or service (an asset) to a customer.

**For Construction:**
- The "asset" is the building/structure being constructed
- "Transfer" occurs as work is performed (on customer's property)
- Revenue is recognized "over time" not "at a point in time"

### Why Percentage-of-Completion, Not Completed Contract?

**Completed Contract Method:**
- Recognize ALL revenue and costs when project is 100% complete
- Results in extreme swings in reported income
- Not allowed under GAAP for most construction contracts

**Percentage-of-Completion Method:**
- Recognize revenue proportionally as work is performed
- Provides smooth, accurate income recognition
- Required by GAAP for qualifying contracts

**Visual Comparison:**

```
Project: $1,000,000 contract, $800,000 cost, 2-year duration

COMPLETED CONTRACT:
Year 1: Revenue $0, Cost $0, Profit $0
Year 2: Revenue $1M, Cost $800K, Profit $200K
(Wildly distorts year-over-year performance)

PERCENTAGE OF COMPLETION:
Year 1 (50% complete): Revenue $500K, Cost $400K, Profit $100K
Year 2 (100% complete): Revenue $500K, Cost $400K, Profit $100K
(Accurately reflects work performed each year)
```

### The Matching Principle in Action

> **GAAP Matching Principle**: Expenses should be recognized in the same period as the revenues they help generate.

**WIP ensures matching:**
- Revenue recognized = Work performed
- Costs recognized = Costs of work performed
- Over/under billing adjustment maintains proper matching

---

## WIP Reports for Bonding Companies

### Why Sureties Want WIP Schedules

Your bonding company provides payment and performance bonds. They're guaranteeing your work.

**They Need to Know:**
1. **Are jobs profitable?** (Est. Gross Profit column)
2. **Are cost estimates reliable?** (Actual vs. Estimated)
3. **Is cash flow healthy?** (Over/under billing pattern)
4. **Any trouble jobs?** (Negative gross profit jobs)

### Standard Surety WIP Format

Most bonding companies want this format:

```
┌─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                    SCHEDULE OF CONTRACTS IN PROGRESS                                                            │
│                                        As of [Date]                                                                             │
├─────────┬──────────┬──────────────────┬─────────────┬──────────────┬─────────────┬───────────┬──────────┬─────────┬────────────┤
│ Job     │ Contract │ Original         │ Approved    │ Revised      │ Total       │ Est. Cost │ Total    │ Billings│ Over/(Under)│
│ Name    │ Date     │ Contract         │ Change      │ Contract     │ Est.        │ to        │ Est.     │ to      │ Billing     │
│         │          │ Amount           │ Orders      │ Amount       │ Cost        │ Complete  │ G.P.     │ Date    │             │
├─────────┼──────────┼──────────────────┼─────────────┼──────────────┼─────────────┼───────────┼──────────┼─────────┼────────────┤
│Smith    │ 1/15/24  │ $950,000         │ $50,000     │ $1,000,000   │ $800,000    │ $480,000  │ $200,000 │ $380,000│ ($20,000)   │
│ABC Corp │ 2/1/24   │ $500,000         │ $0          │ $500,000     │ $400,000    │ $200,000  │ $100,000 │ $280,000│ $30,000     │
│Johnson  │ 3/10/24  │ $750,000         │ $0          │ $750,000     │ $600,000    │ $450,000  │ $150,000 │ $150,000│ ($37,500)   │
├─────────┴──────────┴──────────────────┴─────────────┴──────────────┴─────────────┴───────────┴──────────┴─────────┴────────────┤
│ TOTALS              $2,200,000         $50,000       $2,250,000    $1,800,000   $1,130,000   $450,000  $810,000   ($27,500)    │
└─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘

FADE SCHEDULE (Jobs completed in past 12 months):
┌─────────┬──────────┬──────────────────┬──────────────┬────────────┐
│ Job     │ Contract │ Original Est.    │ Actual       │ Variance   │
│ Name    │ Date     │ Gross Profit     │ Gross Profit │            │
├─────────┼──────────┼──────────────────┼──────────────┼────────────┤
│ Prior 1 │ 6/15/23  │ $80,000          │ $75,000      │ ($5,000)   │
│ Prior 2 │ 8/1/23   │ $45,000          │ $52,000      │ $7,000     │
└─────────┴──────────┴──────────────────┴──────────────┴────────────┘
```

**WHY the Fade Schedule:**
Sureties want to know if your estimates are reliable. The fade schedule shows how your actual profits compared to estimates on completed jobs.

### Red Flags Sureties Watch For

| Red Flag | What It Means | Your Action |
|----------|---------------|-------------|
| Heavy over-billing across all jobs | Cash flow problems, front-loading | Investigate billing timing |
| Negative gross profit on any job | Losing money, poor estimating | Explain circumstances |
| Costs exceeding estimates frequently | Estimating problems | Review estimating process |
| Large under-billing | Financing customers, collection issues | Bill more frequently |
| Incomplete data | Poor financial systems | Clean up records |

---

## Practical WIP Workflow

### Monthly WIP Process

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                      MONTHLY WIP PROCESS                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Week 1: Data Gathering                                                      │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │ 1. Close books for prior month (complete AP/AR entry)                  │ │
│  │ 2. Run P&L by Customer report from QBO                                 │ │
│  │ 3. Update contract values in WIP spreadsheet                           │ │
│  │ 4. Meet with PMs to update cost-to-complete estimates                  │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                          │                                                   │
│                          ▼                                                   │
│  Week 2: WIP Preparation                                                     │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │ 5. Populate WIP schedule with current data                             │ │
│  │ 6. Calculate % complete for each job                                   │ │
│  │ 7. Calculate earned revenue per job                                    │ │
│  │ 8. Determine over/under billing per job                                │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                          │                                                   │
│                          ▼                                                   │
│  Week 2: Analysis & Adjustment                                               │
│  ┌────────────────────────────────────────────────────────────────────────┐ │
│  │ 9. Review for reasonableness                                           │ │
│  │ 10. Calculate WIP adjustment needed                                    │ │
│  │ 11. Post WIP journal entry in QBO                                      │ │
│  │ 12. Verify B/S shows correct CIE/BIE balances                          │ │
│  └────────────────────────────────────────────────────────────────────────┘ │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### The Cost-to-Complete Meeting

**WHY This Meeting Is Critical:**

Your WIP is only as good as your cost-to-complete estimate. If PMs don't update estimates:
- Percentage complete will be wrong
- Earned revenue will be wrong
- Over/under billing will be wrong
- Financial statements will be misleading

**Meeting Agenda:**

1. **For each active project:**
   - Review costs incurred to date
   - Discuss remaining work scope
   - Update estimated cost to complete
   - Identify any problem areas
   - Document change orders pending approval

2. **Questions to ask:**
   - "What's left to do on this job?"
   - "Any surprises we haven't captured in costs?"
   - "Is the original estimate still valid?"
   - "Any change orders we need to account for?"

---

## Common WIP Mistakes

### Mistake 1: Stale Estimates

**Problem**: Cost-to-complete not updated monthly
**Impact**: % complete is wrong, earned revenue is wrong
**Solution**: Monthly PM review meetings (non-negotiable)

### Mistake 2: Ignoring Change Orders

**Problem**: Contract price not updated for approved COs
**Impact**: Earned revenue understated
**Solution**: Add approved COs to contract price immediately

### Mistake 3: Including Completed Jobs

**Problem**: Finished jobs on WIP schedule
**Impact**: Distorts over/under billing totals
**Solution**: Move completed jobs to Fade schedule

### Mistake 4: Not Reconciling to QBO

**Problem**: WIP costs don't match QBO
**Impact**: Two sets of books, audit nightmare
**Solution**: Monthly reconciliation process

### Mistake 5: One-Sided WIP Entries

**Problem**: Adjusting CIE without affecting revenue (or vice versa)
**Impact**: Out-of-balance entries, incorrect financials
**Solution**: Every WIP entry has two sides

---

## WIP and Taxes: Important Note

### Book vs. Tax Treatment

Your WIP represents **GAAP (book) accounting**. Tax treatment may differ:

| Method | GAAP | Tax (Small Contractor) | Tax (Large Contractor) |
|--------|------|------------------------|------------------------|
| Revenue Recognition | % Completion | Completed Contract OK | % Completion Required |
| Threshold | All contracts | Revenue < $26M | Revenue > $26M |
| Over-billing | Deferred (liability) | May be income | Deferred |
| Under-billing | Accrued (asset) | May not be income | Accrued |

**WHY This Matters:**
- You may have two sets of revenue numbers (book vs. tax)
- Your CPA handles the tax reconciliation
- Your WIP schedule is still needed for GAAP statements

---

## Next Steps

Now that you understand WIP and earned revenue, the next logical step is **billing** that earned revenue. In [Progress Billing & Applications for Payment](./05-progress-billing.md), you'll learn:
- Creating progress billing invoices
- AIA G702/G703 forms
- Schedule of Values
- Billing to match earned revenue

---

*[← Previous: Job Costing Setup](./03-job-costing-setup.md) | [Next: Progress Billing →](./05-progress-billing.md)*
