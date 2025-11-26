# Retention Tracking in QuickBooks Online

## Overview

Retention (also called retainage) is a percentage of each payment withheld by the customer until project completion. Tracking retention properly is critical because:
- It represents real money you've earned but not received
- It affects your true accounts receivable balance  
- It impacts bonding capacity calculations
- It requires careful timing on both AR and AP sides

This chapter provides a complete system for tracking retention in QBO.

---

## Understanding Retention

### What is Retention?

> **Definition**: Retention is a contractually agreed-upon percentage (typically 5-10%) of each progress payment withheld by the payer until certain conditions are met (usually substantial completion and punch list resolution).

### WHY Retention Exists

**Owner's Perspective:**
- Ensures contractor completes punch list items
- Provides financial leverage for warranty issues
- Protects against contractor abandonment

**Contractor's Perspective:**
- Represents earned but uncollected revenue
- Creates cash flow timing challenges
- Must be tracked for accurate AR aging

### Retention Flows Both Ways

As a contractor, you have:
1. **Retention Receivable (AR)**: Money your customers owe you
2. **Retention Payable (AP)**: Money you owe your subcontractors

```
OWNER
  │
  │ Pays 90% of your invoice
  │ Holds 10% retention
  ▼
YOU (General Contractor)
  │
  │ Pay 90% of sub invoices
  │ Hold 10% retention
  ▼
SUBCONTRACTOR
```

---

## Setting Up Retention Accounts in QBO

### Create Retention Receivable Account

**HOW:**
1. Go to **Settings ⚙️** → **Chart of Accounts**
2. Click **New**
3. Fill in:
   - **Account Type**: Accounts Receivable
   - **Detail Type**: Accounts Receivable (A/R)
   - **Name**: Retention Receivable
   - **Number**: 12000 (or follow your numbering)
4. Save

**WHY a Separate AR Account:**
Standard Accounts Receivable shows invoiced amounts. Retention Receivable segregates the withheld portion, giving you:
- Clear visibility of retention outstanding
- Accurate aging of billable AR vs. retention
- Proper reporting for bonding purposes

### Create Retention Payable Account

**HOW:**
1. Go to **Settings ⚙️** → **Chart of Accounts**
2. Click **New**
3. Fill in:
   - **Account Type**: Accounts Payable
   - **Detail Type**: Accounts Payable (A/P)
   - **Name**: Retention Payable
   - **Number**: 22000 (or follow your numbering)
4. Save

**WHY a Separate AP Account:**
Same reasoning as AR—segregates retention owed to subs from regular AP.

### Alternative: Use Sub-Accounts

Some prefer sub-accounts under main AR/AP:

```
1200 Accounts Receivable
  └── 1210 Trade Receivables
  └── 1220 Retention Receivable

2100 Accounts Payable  
  └── 2110 Trade Payables
  └── 2120 Retention Payable
```

**Pros**: Keeps AR/AP together in standard accounts
**Cons**: Some reports don't separate sub-accounts well

---

## Creating Retention Products/Services

### Retention Receivable Service Item

**HOW:**
1. Go to **Settings ⚙️** → **Products and Services**
2. Click **New** → **Service**
3. Fill in:
   - **Name**: Retention Withheld
   - **Description**: Contract retention withheld per terms
   - Check "I sell this product/service to my customers"
   - **Income Account**: Select your Retention Receivable account
   - Leave rate blank
4. Save

### Retention Payable Service Item

**HOW:**
1. Go to **Settings ⚙️** → **Products and Services**
2. Click **New** → **Service**  
3. Fill in:
   - **Name**: Subcontractor Retention
   - **Description**: Retention withheld from subcontractor
   - Check "I purchase this product/service from a vendor"
   - **Expense Account**: Select your Retention Payable account
   - Leave rate blank
4. Save

---

## Recording Retention on Customer Invoices

### Method 1: Negative Line Item (Recommended)

This method shows the full invoice amount and then deducts retention.

**HOW to Invoice with Retention:**

1. Create invoice for total work completed
2. Add all SOV line items at their current period values
3. Add final line item:
   - **Product/Service**: Retention Withheld
   - **Amount**: NEGATIVE (e.g., -$10,000)
   - **Note**: "10% retention per contract"
4. Save

**Example Invoice:**
```
┌─────────────────────────────────────────────────────────────────────┐
│ INVOICE #1003                                                       │
│ Customer: ABC Development - Office Project                          │
│ Date: March 1, 2024                                                 │
├─────────────────────────────────────────────────────────────────────┤
│ Progress Billing #3 - February 2024                                 │
├─────────────────────────────────────────────────────────────────────┤
│ PRODUCT/SERVICE              │ AMOUNT                               │
│ ─────────────────────────────┼─────────────────────────────────────│
│ General Conditions           │ $15,000.00                           │
│ Structural Steel             │ $45,000.00                           │
│ Exterior Framing             │ $25,000.00                           │
│ Interior Framing             │ $15,000.00                           │
│ ─────────────────────────────┼─────────────────────────────────────│
│ SUBTOTAL                     │ $100,000.00                          │
│ Retention Withheld (10%)     │ ($10,000.00)                         │
│ ─────────────────────────────┼─────────────────────────────────────│
│ AMOUNT DUE                   │ $90,000.00                           │
└─────────────────────────────────────────────────────────────────────┘
```

**What This Creates in QBO:**
- Debit: Accounts Receivable $90,000
- Debit: Retention Receivable $10,000
- Credit: Contract Revenue $100,000

**WHY This Method Works:**
- Customer sees full value of work completed
- Invoice amount matches what they'll actually pay
- Retention automatically tracked in separate AR account
- Revenue fully recognized (GAAP compliant)

### Method 2: Separate Retention Invoice

Some prefer completely separate tracking:

1. Invoice #1003A: Main invoice for $90,000 (net of retention)
2. Invoice #1003B: Retention invoice for $10,000 (due at completion)

**Pros**: Very clear separation
**Cons**: More invoices to manage, can confuse customers

---

## Recording Retention on Subcontractor Bills

### When Receiving a Sub's Invoice

**HOW to Record Bill with Retention:**

1. Go to **+ New** → **Bill**
2. Fill in vendor, date, etc.
3. In **Item details** section:
   - **Product/Service**: Sub - [Trade] (e.g., Sub - Electrical)
   - **Amount**: Full invoice amount (e.g., $50,000)
   - **Customer**: Assign to project
4. Add second line:
   - **Product/Service**: Subcontractor Retention
   - **Amount**: NEGATIVE (e.g., -$5,000)
5. Save

**Example Bill Entry:**
```
┌─────────────────────────────────────────────────────────────────────┐
│ BILL                                                                │
│ Vendor: Smith Electrical Inc.                                       │
│ Date: February 28, 2024                                             │
│ Bill #: SE-2024-015                                                 │
├─────────────────────────────────────────────────────────────────────┤
│ PRODUCT/SERVICE              │ AMOUNT      │ CUSTOMER                │
│ ─────────────────────────────┼─────────────┼────────────────────────│
│ Sub - Electrical             │ $50,000.00  │ ABC Office Project      │
│ Subcontractor Retention -10% │ ($5,000.00) │ ABC Office Project      │
│ ─────────────────────────────┼─────────────┼────────────────────────│
│ AMOUNT DUE                   │ $45,000.00  │                         │
└─────────────────────────────────────────────────────────────────────┘
```

**What This Creates in QBO:**
- Debit: Subcontractor Expense $50,000
- Credit: Accounts Payable $45,000
- Credit: Retention Payable $5,000

---

## Tracking Retention by Project

### WHY Project-Level Retention Tracking Matters

At project completion, you need to know:
- Exactly how much retention is due from this customer
- Exactly how much retention you owe to each sub on this project

### Report: Retention Receivable by Project

**HOW to Create:**

1. Go to **Reports** → **Balance Sheet Detail**
2. Filter: Account = Retention Receivable
3. Group by: Customer
4. This shows retention outstanding by customer/project

**Alternative: Custom Report**
1. Go to **Reports** → **Transaction List by Customer**
2. Filter: Account = Retention Receivable
3. This provides transaction-level detail

### Report: Retention Payable by Project

**HOW to Create:**

1. Go to **Reports** → **A/P Aging Detail**
2. Filter: Account = Retention Payable
3. Group by: Vendor
4. This shows retention owed to each sub

**WHY Transaction-Level Detail Matters:**
At completion, you'll release retention by vendor/project. Having clear records prevents:
- Releasing wrong amount
- Missing vendors
- Double payments

---

## Billing for Retention Release

### When to Bill Retention

Retention is typically released upon:
- Substantial completion
- Punch list completion
- Final inspection approval
- Lien waiver submission
- Owner/architect certification

### HOW to Bill for Retention Release

**Step 1: Verify Retention Amount**
Run retention receivable report for the project to confirm balance.

**Step 2: Create Retention Release Invoice**

1. Go to **+ New** → **Invoice**
2. Select Customer/Project
3. Add line item:
   - **Product/Service**: Retention Release (create if needed)
   - **Description**: "Release of retention per contract completion"
   - **Amount**: Full retention balance
4. Save

**IMPORTANT: Income Account Setup**
Create "Retention Release" product with same income account as "Retention Withheld" but use the POSITIVE amount. This debits AR and credits Retention Receivable.

**Alternative Method: Journal Entry**

If the retention product setup is confusing, use a journal entry:

```
Date: [Project completion date]
Memo: Retention release - ABC Office Project

Account                        Debit        Credit
────────────────────────────────────────────────────
Accounts Receivable           $25,000
  Retention Receivable                     $25,000
────────────────────────────────────────────────────
To reclassify retention to standard A/R upon project completion
```

Then invoice normally from A/R.

---

## Releasing Retention to Subcontractors

### When to Release Sub Retention

You typically release sub retention when:
- You receive your retention from owner
- Sub completes all punch list items
- Sub provides final lien waiver
- Warranty period begins (varies by contract)

### HOW to Release Sub Retention

**Step 1: Verify Retention Owed**
Run retention payable report for the project by vendor.

**Step 2: Create Retention Release Bill**

1. Go to **+ New** → **Bill**
2. Select Vendor (subcontractor)
3. Add line item:
   - **Product/Service**: Create "Retention Release - Sub"
   - **Description**: "Release of retention per subcontract completion"
   - **Amount**: Full retention balance
   - **Account**: Retention Payable (to reduce the liability)
4. Save and pay normally

**Alternative: Journal Entry to Reclassify**

```
Date: [Retention release date]
Memo: Retention release to Smith Electrical - ABC Project

Account                        Debit        Credit
────────────────────────────────────────────────────
Retention Payable             $5,000
  Accounts Payable                         $5,000
────────────────────────────────────────────────────
To reclassify retention to standard A/P for payment
```

---

## Retention Matching: The Cash Flow Reality

### The Timing Problem

```
Timeline:
───────────────────────────────────────────────────────────────────────────
Month 1    Month 2    Month 3    Month 4    Month 5    Month 6
  │          │          │          │          │          │
  ▼          ▼          ▼          ▼          ▼          ▼
Invoice    Invoice    Invoice    Invoice    Complete   Receive
#1         #2         #3         #4         Project    Retention
$10K ret   $10K ret   $10K ret   $10K ret              $40K
  │          │          │          │                     │
  │          │          │          │                     │
  ▼          ▼          ▼          ▼                     │
Pay sub    Pay sub    Pay sub    Pay sub              Pay sub
$5K ret    $5K ret    $5K ret    $5K ret              retention
                                                       $20K
───────────────────────────────────────────────────────────────────────────

RETENTION CASH FLOW:
Your retention receivable grows each month: $10K → $20K → $30K → $40K
Your retention payable grows each month:    $5K → $10K → $15K → $20K
Net cash tied up in retention:              $5K → $10K → $15K → $20K
```

### WHY Retention Matching Matters for Cash Flow

If your retention receivable rate doesn't match your retention payable rate:

```
PROBLEM SCENARIO:
Customer retention: 10% = $100,000 held back
Your sub retention:  5% = $50,000 you hold back
Net cash impact:        = $50,000 you're financing!

IDEAL SCENARIO:
Customer retention: 10% = $100,000 held back
Your sub retention: 10% = $100,000 you hold back
Net cash impact:        = $0 (pass-through)
```

**Contract Negotiation Tip**: Match your sub retention terms to your customer retention terms.

---

## Retention Aging Analysis

### WHY Aging Matters

Old retention is a warning sign:
- Project may be stalled
- Punch list issues unresolved
- Collection problems developing

### Creating a Retention Aging Report

**QBO Doesn't Have Native Retention Aging, So Build in Excel:**

**Step 1: Export Data**
1. Run **Balance Sheet Detail** filtered to Retention Receivable
2. Export to Excel

**Step 2: Create Aging Buckets**

```
┌─────────────────────────────────────────────────────────────────────────────────────────┐
│                        RETENTION RECEIVABLE AGING                                        │
│                        As of: March 31, 2024                                            │
├─────────────────────────────┬───────────┬──────────┬──────────┬──────────┬──────────────┤
│ Customer / Project          │ Current   │ 31-60    │ 61-90    │ Over 90  │ Total        │
├─────────────────────────────┼───────────┼──────────┼──────────┼──────────┼──────────────┤
│ ABC Development - Office    │ $10,000   │ $10,000  │ $5,000   │ $0       │ $25,000      │
│ Smith Residence             │ $0        │ $0       │ $3,500   │ $12,000  │ $15,500  ⚠️ │
│ Johnson Commercial          │ $8,000    │ $4,000   │ $0       │ $0       │ $12,000      │
├─────────────────────────────┼───────────┼──────────┼──────────┼──────────┼──────────────┤
│ TOTAL                       │ $18,000   │ $14,000  │ $8,500   │ $12,000  │ $52,500      │
│ % of Total                  │ 34%       │ 27%      │ 16%      │ 23%      │ 100%         │
└─────────────────────────────┴───────────┴──────────┴──────────┴──────────┴──────────────┘

Action Items:
⚠️ Smith Residence: $12,000 over 90 days - Follow up on completion status
```

### Retention Over 90 Days: Warning Signs

| Scenario | Likely Cause | Action |
|----------|--------------|--------|
| Project complete, retention not billed | Billing oversight | Bill immediately |
| Project complete, retention billed but not paid | Collection issue | Follow up aggressively |
| Project not complete, retention aging | Punch list issues | Complete punch list |
| Project disputed | Contract dispute | Legal/management attention |

---

## Retention on Your Balance Sheet

### Proper GAAP Presentation

```
BALANCE SHEET
As of March 31, 2024

ASSETS
Current Assets:
  Cash                                    $xxx,xxx
  Accounts Receivable                     $185,000
  Retention Receivable                     $52,500
  Costs in Excess of Billings              $xx,xxx
  ───────────────────────────────────────────────────
  Total Current Assets                    $xxx,xxx

LIABILITIES  
Current Liabilities:
  Accounts Payable                        $xxx,xxx
  Retention Payable                        $28,000
  Billings in Excess of Costs              $xx,xxx
  ───────────────────────────────────────────────────
  Total Current Liabilities               $xxx,xxx
```

### WHY Separate Lines Matter for Bonding

Bonding companies analyze your working capital:
- **Retention Receivable**: Generally excluded from "quick" working capital calculations (can't be collected immediately)
- **Retention Payable**: Also excluded from immediate liability calculations

Net effect: Bonding companies want to see both numbers to assess:
1. How much capital is tied up in retention
2. Whether retention terms are matched
3. If old retention indicates problem projects

---

## Common Retention Mistakes

### Mistake 1: Retention Not Tracked Separately

**Problem**: Retention buried in standard AR/AP
**Impact**: Can't identify true receivable vs. retention, bad reporting
**Solution**: Use separate retention accounts

### Mistake 2: Retention Rates Not Matched

**Problem**: Customer holds 10%, you only hold 5% from subs
**Impact**: Cash flow drag, financing sub work
**Solution**: Match retention terms in subcontracts

### Mistake 3: Old Retention Not Followed Up

**Problem**: Retention over 90 days not addressed
**Impact**: Collection problems, may indicate project issues
**Solution**: Monthly retention aging review

### Mistake 4: Releasing Sub Retention Before Receiving Yours

**Problem**: Pay sub retention before customer pays you
**Impact**: Cash flow problems, no leverage for sub performance
**Solution**: Policy: Release sub retention only after receiving customer retention

### Mistake 5: Not Getting Lien Waivers for Retention

**Problem**: Release retention without final lien waiver
**Impact**: Lien exposure, payment disputes
**Solution**: Require unconditional final waiver before releasing retention

---

## Retention Tracking Checklist

### Setup:
- [ ] Retention Receivable account created
- [ ] Retention Payable account created
- [ ] Retention products/services created
- [ ] Staff trained on retention entry

### Monthly:
- [ ] All customer invoices include retention line
- [ ] All sub bills include retention line
- [ ] Retention aging report reviewed
- [ ] Old retention items investigated

### Project Completion:
- [ ] Final retention receivable balance verified
- [ ] Retention release invoice created
- [ ] Final lien waivers collected
- [ ] Sub retention releases processed with final waivers
- [ ] Retention accounts zeroed for completed projects

---

## Next Steps

With retention tracking in place, the next important system is allocating equipment costs to jobs. In [Equipment Allocation](./07-equipment-allocation.md), you'll learn:
- Tracking owned vs. rented equipment
- Internal equipment charge rates
- Equipment cost allocation methods
- Equipment profitability analysis

---

*[← Previous: Progress Billing](./05-progress-billing.md) | [Next: Equipment Allocation →](./07-equipment-allocation.md)*
