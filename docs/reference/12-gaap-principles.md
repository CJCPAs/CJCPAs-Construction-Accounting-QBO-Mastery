# GAAP Principles Reference for Construction Accounting

## Overview

This chapter explains the Generally Accepted Accounting Principles (GAAP) that govern construction accounting. For each principle, we provide:
- The technical standard
- Plain English explanation
- How it applies to construction
- Practical implications

---

## The Foundation: ASC 606 Revenue Recognition

### What is ASC 606?

ASC 606 (Accounting Standards Codification Topic 606) is the GAAP standard for recognizing revenue from contracts with customers. It replaced the previous construction-specific guidance in 2018.

### The Five-Step Model

```
ASC 606: FIVE STEPS TO REVENUE RECOGNITION

Step 1: IDENTIFY THE CONTRACT
        ▼
Step 2: IDENTIFY PERFORMANCE OBLIGATIONS
        ▼
Step 3: DETERMINE TRANSACTION PRICE
        ▼
Step 4: ALLOCATE PRICE TO PERFORMANCE OBLIGATIONS
        ▼
Step 5: RECOGNIZE REVENUE WHEN OBLIGATIONS SATISFIED
```

### Step 1: Identify the Contract

**Standard**: A contract exists when both parties have approved it, rights and payment terms are identifiable, the contract has commercial substance, and collection is probable.

**For Construction**:
- Written contracts (most common)
- Purchase orders
- Work orders
- Change orders (once approved)

**Practical Application**:
No contract = No revenue recognition (even if work is performed)

### Step 2: Identify Performance Obligations

**Standard**: A performance obligation is a promise to transfer a good or service that is distinct or a series of distinct goods/services.

**For Construction**:
Most construction contracts have a **single performance obligation** because:
- The outputs are highly interdependent
- The contractor provides significant integration services
- The owner couldn't hire separate contractors for each component

**Example**:
```
Contract: Build a commercial building
- Foundation, structure, mechanical, electrical, finishes

Even though these could be done separately, they're ONE performance 
obligation because:
- They're integrated into a single deliverable
- The contractor coordinates all components
- Value comes from the integrated whole
```

### Step 3: Determine Transaction Price

**Standard**: Transaction price is the amount of consideration expected to be received in exchange for transferring goods/services.

**For Construction**:
- Original contract amount
- **Plus**: Approved change orders
- **Plus**: Incentive payments if probable
- **Minus**: Liquidated damages if probable
- **Excluding**: Disputed amounts until resolved

**Variable Consideration**:
```
Original Contract:      $1,000,000
Approved COs:             $50,000
Incentive (if probable):  $25,000
─────────────────────────────────
Transaction Price:     $1,075,000
```

### Step 4: Allocate to Performance Obligations

**Standard**: If multiple obligations, allocate transaction price based on standalone selling prices.

**For Construction**:
With a single performance obligation (typical), no allocation is needed. The entire transaction price applies to that obligation.

### Step 5: Recognize Revenue

**Standard**: Recognize revenue when (or as) each performance obligation is satisfied—either over time or at a point in time.

**For Construction**:
Construction contracts almost always meet criteria for **over time** recognition because:
- The asset is created on customer's property
- Customer controls the work in progress
- No alternative use for the work

---

## Percentage-of-Completion Method

### The Core Concept

> **GAAP Principle**: When revenue is recognized over time, progress toward completion must be measured to determine how much revenue to recognize.

### Input vs. Output Methods

| Method | Measures | Example | Best For |
|--------|----------|---------|----------|
| **Input (Cost-to-Cost)** | Costs incurred vs. total costs | $400K spent ÷ $1M total = 40% | Most construction |
| **Output (Units)** | Units delivered vs. total units | 40 units ÷ 100 units = 40% | Repetitive production |

### Cost-to-Cost Formula

```
% Complete = Costs Incurred to Date ÷ Total Estimated Costs

Earned Revenue = Contract Price × % Complete

Earned Revenue This Period = Total Earned Revenue - Previously Recognized Revenue
```

### Why Cost-to-Cost is Preferred

1. **Objective**: Costs are documented with invoices
2. **Auditable**: Third parties can verify
3. **Consistent**: Applied the same way across projects
4. **Comprehensive**: Captures all work (including subs)

### Costs That Count

**Include in % Complete**:
- Direct labor
- Materials installed
- Subcontractor work
- Equipment used
- Other direct costs

**Exclude from % Complete**:
- Materials stored but not installed (may use separately)
- Costs unrelated to progress
- Abnormal costs (waste, rework beyond normal)
- Advance payments to subs

---

## The Matching Principle

### The Core Concept

> **GAAP Principle**: Expenses should be recognized in the same accounting period as the revenues they help generate.

### Application to Construction

```
CORRECT APPLICATION (MATCHING):

Month 1: Incur $100,000 costs, 10% complete
         Recognize: $120,000 revenue (10% of $1.2M contract)
                   $100,000 costs
                   $20,000 gross profit

Month 2: Incur $100,000 costs, 20% complete
         Recognize: $120,000 revenue (additional 10%)
                   $100,000 costs
                   $20,000 gross profit

WRONG APPLICATION (NO MATCHING):

Month 1: Incur $100,000 costs
         Bill $0 (waiting for milestone)
         Report: $100,000 loss

Month 2: Incur $100,000 costs
         Bill $300,000
         Report: $200,000 profit

(Actual results are identical, but without matching, 
Month 1 looks disastrous and Month 2 looks amazing)
```

---

## Over/Under Billing: The GAAP Perspective

### Billings in Excess of Costs (Over-Billing)

**GAAP Definition**: When cumulative billings exceed cumulative revenue recognized, the difference is a contract liability.

**Why It's a Liability**:
You've received payment for work not yet performed. You owe the customer that work.

**Balance Sheet Presentation**:
- Shown in Current Liabilities
- Often called "Billings in Excess of Costs and Estimated Earnings on Uncompleted Contracts"

### Costs in Excess of Billings (Under-Billing)

**GAAP Definition**: When cumulative revenue recognized exceeds cumulative billings, the difference is a contract asset.

**Why It's an Asset**:
You've performed work you haven't yet billed for. You have a right to payment.

**Balance Sheet Presentation**:
- Shown in Current Assets
- Often called "Costs and Estimated Earnings in Excess of Billings on Uncompleted Contracts"

### Key GAAP Requirements

1. **Cannot Net**: Over and under-billing from different contracts cannot be netted. Each contract must be evaluated separately.

2. **Must Disclose**: Financial statements must include information about:
   - Revenue recognized
   - Method used to measure progress
   - Significant judgments made

---

## Loss Contracts

### Recognition of Losses

> **GAAP Principle**: When current estimates indicate a loss on a contract, the entire loss must be recognized immediately—not spread over the contract period.

### Why Immediate Recognition?

**Conservative Accounting**: GAAP prefers recognizing losses sooner (conservatism). Waiting to recognize a loss would overstate profitability.

### Example

```
CONTRACT SITUATION:
Contract Price:          $1,000,000
Original Est. Cost:        $900,000
Original Est. Profit:      $100,000

At 50% Complete, new estimate:
Revised Est. Cost:       $1,100,000
Revised Est. Profit:      ($100,000) LOSS

REQUIRED ACCOUNTING:
Recognize entire $100,000 loss NOW, even though:
- Only 50% of work is complete
- The loss hasn't been "incurred" yet in traditional sense

Journal Entry:
Dr. Loss on Contract              $100,000
    Cr. Estimated Loss on Contract (Liability)  $100,000
```

### Ongoing Treatment

Once a loss is recognized:
- Future revenue recognition continues normally
- Loss provision is drawn down as work progresses
- If estimate improves, recovery of loss is recognized

---

## Change Orders Under GAAP

### Types of Modifications

| Type | Contract Price Change | Revenue Recognition |
|------|----------------------|---------------------|
| **Approved CO** | Yes, documented | Include in transaction price |
| **Pending CO (probable)** | Estimated | May include if probable and estimable |
| **Disputed CO** | Unknown | Exclude until resolved |
| **Unpriced CO** | TBD | Include estimated amount if probable |

### Variable Consideration Rules

For pending change orders to be included in revenue:

> **GAAP Constraint**: Include variable consideration only to the extent that it is probable that a significant revenue reversal will not occur.

**In Practice**:
- Strong documentation? May include
- Oral promise only? Don't include
- Similar COs always approved? May include
- First time situation? Don't include

---

## Contract Costs

### Which Costs to Capitalize

**Pre-Contract Costs (Bid Costs)**:
- Generally expensed when incurred
- Exception: Costs to obtain a contract (like sales commissions) may be capitalized if recoverable

**Contract Fulfillment Costs**:
- Direct materials, labor, subs → COGS
- Indirect costs allocable to contract → COGS
- Costs that don't relate to future performance → Expense

### Uninstalled Materials

**GAAP Treatment**:
Uninstalled materials should generally be excluded from the % complete calculation UNLESS:
- They're unique to the project (can't use elsewhere)
- Control has transferred to customer
- Revenue can be recognized for the materials

**Example**:
```
Scenario A: Standard materials stored on site
- Cost: $50,000
- Treatment: Exclude from % complete until installed
- Or: Recognize separate revenue equal to cost (0% margin)

Scenario B: Custom-fabricated equipment
- Cost: $200,000
- Treatment: Include in % complete (customer-specific, no alternative use)
```

---

## Retainage Under GAAP

### Classification

**Retainage Receivable**:
- Qualifies as accounts receivable
- Collection is probable (assuming normal contract completion)
- Unconditional right to payment exists

**Current vs. Non-Current**:
- Retention due within 12 months: Current Asset
- Retention due beyond 12 months: Long-term Asset
- (Most construction retention is current)

### Impairment

If collection becomes questionable:
- Evaluate for impairment
- Record allowance if necessary
- Disclose significant retention aging issues

---

## Disclosures Required by GAAP

### ASC 606 Disclosure Requirements

For significant contracts, disclose:

1. **Revenue Recognized**
   - Revenue by category (type of contract, geography, etc.)
   - Significant judgments in determining timing

2. **Contract Balances**
   - Contract assets (under-billing)
   - Contract liabilities (over-billing)
   - Changes from prior period

3. **Performance Obligations**
   - Remaining performance obligations
   - Expected timing of satisfaction

4. **Significant Judgments**
   - Methods to measure progress
   - Significant payment terms
   - Variable consideration estimates

---

## GAAP vs. Tax Accounting

### Common Differences

| Item | GAAP | Tax (Small Contractor) | Tax (Large Contractor) |
|------|------|------------------------|------------------------|
| **Revenue Method** | % Complete | Completed Contract OK | % Complete required |
| **Threshold** | All contracts | < $26M avg revenue | > $26M avg revenue |
| **Long-term** | Any duration | > 1 year may differ | > 1 year |
| **Over-billing** | Deferred (liability) | May be income | Deferred |
| **Under-billing** | Accrued (asset) | May not be income | Accrued |

### Implications

- Keep GAAP books for bonding, banking, and management
- Tax return may differ (CPA handles reconciliation)
- Don't adjust GAAP books to match tax return

---

## Summary: Key GAAP Concepts

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    GAAP CONSTRUCTION ACCOUNTING SUMMARY                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. REVENUE RECOGNITION (ASC 606)                                           │
│     • Five-step model applies                                               │
│     • Most construction = single performance obligation                     │
│     • Recognize revenue over time (as work progresses)                      │
│                                                                              │
│  2. MEASURING PROGRESS                                                       │
│     • Cost-to-cost is most common                                           │
│     • % Complete = Costs Incurred ÷ Total Estimated Costs                   │
│     • Earned Revenue = Contract × % Complete                                │
│                                                                              │
│  3. OVER/UNDER BILLING                                                       │
│     • Over-billing (billed > earned) = Liability                            │
│     • Under-billing (earned > billed) = Asset                               │
│     • Cannot net across contracts                                           │
│                                                                              │
│  4. MATCHING PRINCIPLE                                                       │
│     • Match costs to revenue in same period                                 │
│     • Don't wait for billing to recognize revenue                           │
│                                                                              │
│  5. LOSSES                                                                   │
│     • Recognize entire estimated loss immediately                           │
│     • Don't wait until loss is "realized"                                   │
│                                                                              │
│  6. CHANGE ORDERS                                                            │
│     • Approved COs = Add to contract price                                  │
│     • Pending COs = Include only if probable                                │
│     • Disputed COs = Exclude until resolved                                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick Reference: Journal Entries

### Revenue Recognition (Normal Progress)

```
Dr. Accounts Receivable (Billings)
    Cr. Contract Revenue

Dr. Contract Costs (COGS)
    Cr. Accounts Payable / Cash / etc.
```

### WIP Adjustment (Under-Billing)

```
Dr. Costs in Excess of Billings
    Cr. Contract Revenue
```

### WIP Adjustment (Over-Billing)

```
Dr. Contract Revenue
    Cr. Billings in Excess of Costs
```

### Loss Recognition

```
Dr. Loss on Contracts
    Cr. Estimated Loss Liability
```

---

*[← Previous: Month-End Close Checklist](../checklists/11-month-end-close.md) | [Back to Introduction →](../01-introduction.md)*
