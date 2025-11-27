# Invoice Tie-Out & Pay App Reconciliation

## Overview

This chapter provides detailed procedures for tying out your invoices to pay applications, reconciling AR balances, and ensuring your billing matches your work in progress. These skills are essential for accurate financial reporting and avoiding disputes.

---

## Understanding the Invoice-to-Pay App Connection

### What is a Pay App?

A **Pay Application** (Pay App) is a formal request for payment, typically using AIA forms (G702/G703), that documents:
- Work completed to date
- Materials stored
- Previous payments received
- Retention held
- Current amount due

### The Relationship

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                    INVOICE vs PAY APP RELATIONSHIP                                   │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  PAY APPLICATION (AIA G702/G703)              QBO INVOICE                           │
│  ────────────────────────────                 ─────────────────────                  │
│                                                                                      │
│  Application for Payment #3                   Invoice #1045                          │
│  Period: 03/01/24 - 03/31/24                 Date: 04/01/24                          │
│                                                                                      │
│  ┌─────────────────────────────┐             ┌─────────────────────────────┐        │
│  │ Total Completed: $620,000   │ ═══════════▶│ Amount: Matches pay app     │        │
│  │ Retention: ($62,000)        │             │ Retention: ($62,000)        │        │
│  │ Previous Payments: $378,000 │             │ Previously Invoiced         │        │
│  │ Current Due: $180,000       │             │ Current Invoice: $180,000   │        │
│  └─────────────────────────────┘             └─────────────────────────────┘        │
│                                                                                      │
│  The QBO invoice should EXACTLY match the pay app submitted to the customer         │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

---

## Step-by-Step: Creating Invoice from Pay App

### Step 1: Complete Your Pay Application

Before creating the QBO invoice, prepare your pay app:
- G702 Application and Certificate for Payment
- G703 Continuation Sheet (Schedule of Values)
- Supporting documentation

### Step 2: Verify Pay App Math

Double-check these calculations:

```
PAY APP VERIFICATION CHECKLIST:

1. Contract Verification
   Original Contract:                    $____________
   + Approved Change Orders:             $____________
   = Current Contract Sum:               $____________

2. Work Completed Verification  
   Previous Completed (Column D):        $____________
   + This Period (Column E):             $____________
   + Stored Materials (Column F):        $____________
   = Total Completed (Column G):         $____________

3. Retention Verification
   Completed Work × Retention %:         $____________
   + Stored Materials × Retention %:     $____________
   = Total Retention:                    $____________

4. Current Payment Calculation
   Total Completed & Stored:             $____________
   - Total Retention:                    $____________
   = Total Earned Less Retention:        $____________
   - Previous Certificates:              $____________
   = CURRENT PAYMENT DUE:                $____________
```

### Step 3: Create Matching QBO Invoice

**HOW:**

1. Go to **+ New** → **Invoice**

2. **Header Information:**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                  INVOICE                                             │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Customer: [ABC Development LLC ▼]                                                   │
│  Project:  [2024-001-ABC-OfficeBuildout ▼]                                          │
│                                                                                      │
│  Invoice date: [04/01/2024]  ◄── Date of pay app submission                         │
│  Due date:     [05/01/2024]  ◄── Per contract terms (usually Net 30)                │
│  Terms:        [Net 30 ▼]                                                           │
│                                                                                      │
│  Invoice no.:  [1045]                                                                │
│  P.O. number:  [Leave blank or enter GC PO#]                                        │
│                                                                                      │
│  Message on invoice:                                                                 │
│  [Application for Payment #3 - Work through 03/31/2024                              │
│   See attached AIA G702/G703 for detail]                                            │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Line Items - Two Methods:**

**Method A: Single Line Item (Simpler)**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  # │ PRODUCT/SERVICE     │ DESCRIPTION                      │ AMOUNT               │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  1 │ Progress Billing    │ Pay App #3 - Work thru 03/31/24  │ $200,000.00         │
│  2 │ Retention Held      │ 10% retention per contract        │ ($20,000.00)        │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│                                              TOTAL DUE:       │ $180,000.00         │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**Method B: Match G703 Lines (More Detail)**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  # │ PRODUCT/SERVICE     │ DESCRIPTION                      │ AMOUNT               │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  1 │ General Conditions  │ Item 1 - This period             │ $15,000.00          │
│  2 │ Structural Steel    │ Item 4 - This period             │ $90,000.00          │
│  3 │ Ext. Framing        │ Item 5 - This period             │ $58,000.00          │
│  4 │ Interior Framing    │ Item 9 - This period             │ $25,000.00          │
│  5 │ Mechanical Rough    │ Item 12 - This period            │ $12,000.00          │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│      SUBTOTAL                                                │ $200,000.00         │
│  6 │ Retention Held      │ 10% per contract                  │ ($20,000.00)        │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│                                              TOTAL DUE:       │ $180,000.00         │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

4. **Attach Documentation:**
   - G702 Application for Payment
   - G703 Continuation Sheet
   - Lien waivers (conditional)
   - Any backup documentation

5. **Save and Review**

### Step 4: Verify Invoice Matches Pay App

**CRITICAL VERIFICATION:**
```
Pay App Shows:                          QBO Invoice Shows:
──────────────                          ─────────────────
Current Payment Due: $180,000.00   =    Invoice Total: $180,000.00  ✓

Work This Period: $200,000.00      =    Subtotal: $200,000.00  ✓

Retention: $20,000.00              =    Retention Line: ($20,000.00)  ✓
```

---

## Reconciling Invoices to Contract

### The Master Reconciliation

At any point, your total invoices should tie to your contract progress:

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                    CONTRACT TO INVOICE RECONCILIATION                                │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  PROJECT: 2024-001-ABC-OfficeBuildout                                               │
│  DATE: 04/01/2024                                                                    │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  CONTRACT STATUS                                                                     │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Original Contract:                              $1,500,000.00                       │
│  Approved Change Orders:                            $50,000.00                       │
│  Current Contract Value:                         $1,550,000.00                       │
│                                                                                      │
│  BILLING STATUS                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Total Completed & Stored (per G702):              $620,000.00                       │
│  Total Retention Held:                             ($62,000.00)                      │
│  Total Earned Less Retention:                      $558,000.00                       │
│                                                                                      │
│  QBO INVOICE STATUS                                                                  │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Invoice #1043 (Pay App #1):                       $180,000.00                       │
│  Invoice #1044 (Pay App #2):                       $198,000.00                       │
│  Invoice #1045 (Pay App #3):                       $180,000.00                       │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Total Invoiced (Net of Retention):                $558,000.00  ✓ MATCHES           │
│                                                                                      │
│  RETENTION TRACKING                                                                  │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Retention per Pay Apps:                            $62,000.00                       │
│  Retention per QBO Retention Receivable:            $62,000.00  ✓ MATCHES           │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Running the QBO Reconciliation Report

**HOW:**

1. Go to **Reports** → "Customer Balance Detail"
2. Filter for your project customer
3. Review all transactions

```
CUSTOMER BALANCE DETAIL
Customer: ABC Development - Office Buildout

Date        Type      Num     Amount      Balance
──────────────────────────────────────────────────────
02/01/24    Invoice   1043    $180,000    $180,000
02/28/24    Payment           ($180,000)  $0
03/01/24    Invoice   1044    $198,000    $198,000
03/28/24    Payment           ($198,000)  $0
04/01/24    Invoice   1045    $180,000    $180,000
──────────────────────────────────────────────────────
                              BALANCE:    $180,000
```

---

## Retention Reconciliation

### Tracking Retention Separately

**WHY SEPARATE RETENTION:**
- Retention isn't due until project completion
- Different aging than regular AR
- Need to track for final billing
- Bonding company requires breakdown

### Retention Tie-Out Process

**Step 1: Calculate Expected Retention**
```
From Pay App Records:
Pay App #1: Work $200,000 × 10% = $20,000 retention
Pay App #2: Work $220,000 × 10% = $22,000 retention
Pay App #3: Work $200,000 × 10% = $20,000 retention
────────────────────────────────────────────────────
TOTAL EXPECTED RETENTION:          $62,000
```

**Step 2: Run QBO Retention Report**
1. Go to **Reports** → "Balance Sheet Detail"
2. Filter: Account = Retention Receivable
3. Filter: Customer = Your project

```
BALANCE SHEET DETAIL - RETENTION RECEIVABLE
Customer: ABC Development - Office Buildout

Date        Type      Num     Memo                    Amount      Balance
──────────────────────────────────────────────────────────────────────────────
02/01/24    Invoice   1043    10% retention           $20,000     $20,000
03/01/24    Invoice   1044    10% retention           $22,000     $42,000
04/01/24    Invoice   1045    10% retention           $20,000     $62,000
──────────────────────────────────────────────────────────────────────────────
                              BALANCE:                             $62,000  ✓
```

**Step 3: Verify Match**
```
Expected Retention (from pay apps):    $62,000
QBO Retention Receivable:              $62,000
Difference:                            $0  ✓ RECONCILED
```

---

## AR Aging Analysis

### Understanding AR Categories

For construction companies, AR has distinct categories:

```
AR BREAKDOWN:
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                      │
│  TRADE RECEIVABLES (Regular AR)                                                      │
│  ─────────────────────────────                                                       │
│  Invoices with payment terms                                                         │
│  Expected collection: Within 30-60 days                                              │
│  Action: Follow up on overdue                                                        │
│                                                                                      │
│  RETENTION RECEIVABLE                                                                │
│  ───────────────────                                                                 │
│  Retention withheld until completion                                                 │
│  Expected collection: At project end                                                 │
│  Action: Track, bill at completion                                                   │
│                                                                                      │
│  UNBILLED REVENUE (Under-billing)                                                    │
│  ─────────────────────────────────                                                   │
│  Work performed but not yet billed                                                   │
│  Not in AR until invoiced                                                            │
│  Action: Bill promptly                                                               │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Running AR Aging Report

**HOW:**
1. Go to **Reports** → "A/R Aging Summary"
2. Review by customer/project

```
A/R AGING SUMMARY
As of 04/15/2024

Customer                    CURRENT   1-30     31-60    61-90    91+      TOTAL
──────────────────────────────────────────────────────────────────────────────────────
ABC Development             $180,000  $0       $0       $0       $0       $180,000
Smith Residence             $15,300   $0       $0       $0       $0       $15,300
Johnson Commercial          $0        $25,000  $0       $0       $0       $25,000  ⚠️
XYZ Corp                    $0        $0       $12,500  $0       $0       $12,500  ⚠️
──────────────────────────────────────────────────────────────────────────────────────
TOTAL                       $195,300  $25,000  $12,500  $0       $0       $232,800
```

### Following Up on Overdue Invoices

**COLLECTION WORKFLOW:**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                        AR COLLECTION WORKFLOW                                        │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  DAY 1 (Invoice Sent)                                                                │
│  ├── Send invoice with pay app                                                      │
│  └── Confirm receipt                                                                │
│                                                                                      │
│  DAY 25 (5 days before due)                                                         │
│  ├── Send friendly reminder                                                         │
│  └── Verify no issues with pay app                                                  │
│                                                                                      │
│  DAY 35 (5 days overdue)                                                            │
│  ├── Phone call to AP contact                                                       │
│  └── Document conversation                                                          │
│                                                                                      │
│  DAY 45 (15 days overdue)                                                           │
│  ├── Escalate to project manager                                                    │
│  ├── Send formal demand letter                                                      │
│  └── Consider stopping work                                                         │
│                                                                                      │
│  DAY 60+ (30+ days overdue)                                                         │
│  ├── Escalate to management                                                         │
│  ├── Review lien rights                                                             │
│  └── Consider legal action                                                          │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

---

## Tying AR to WIP Schedule

### The AR-WIP Connection

Your AR should reconcile to your WIP schedule:

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                       AR TO WIP RECONCILIATION                                       │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  FROM WIP SCHEDULE:                                                                  │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Total Billings to Date (all projects):              $2,450,000                      │
│  Less: Collections to Date:                         ($2,100,000)                     │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Expected AR Balance:                                  $350,000                      │
│                                                                                      │
│  FROM QBO:                                                                           │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Accounts Receivable (Trade):                          $232,800                      │
│  Retention Receivable:                                 $117,200                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  Total QBO Receivable:                                 $350,000  ✓                   │
│                                                                                      │
│  DIFFERENCE:                                           $0.00  RECONCILED             │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Common Reconciliation Issues

| Issue | Cause | Resolution |
|-------|-------|------------|
| AR higher than WIP | Invoice entered but not on WIP | Add to WIP or delete duplicate invoice |
| AR lower than WIP | Billing not entered in QBO | Enter missing invoice |
| Retention doesn't match | Wrong retention % or calculation error | Review each pay app |
| Collections different | Payment not applied or misapplied | Review payment applications |

---

## Monthly Invoice Tie-Out Checklist

### Before Month-End Close

**FOR EACH ACTIVE PROJECT:**

- [ ] **Verify Pay App Submitted**
  - Pay app sent to customer
  - Copy retained in files
  - G702/G703 completed correctly

- [ ] **Verify QBO Invoice Created**
  - Invoice matches pay app amount
  - Retention recorded correctly
  - Attached to correct project

- [ ] **Verify AR Balance**
  - Run customer balance report
  - Compare to expected balance
  - Investigate differences

- [ ] **Verify Retention Balance**
  - Run retention receivable report
  - Compare to cumulative retention per pay apps
  - Investigate differences

### Monthly Summary Report

Create a monthly summary for management:

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                    MONTHLY BILLING SUMMARY - MARCH 2024                              │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Project               Contract    Billed MTD   Billed YTD   % Billed   AR Balance  │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  ABC Office Buildout   $1,550,000  $180,000     $558,000     36%        $180,000    │
│  Smith Residence         $150,000   $15,300     $120,000     80%         $15,300    │
│  Johnson Commercial      $500,000   $25,000     $175,000     35%         $25,000    │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  TOTALS                $2,200,000  $220,300     $853,000     39%        $220,300    │
│                                                                                      │
│  RETENTION SUMMARY                                                                   │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  Total Retention Held:                                                $117,200      │
│  Expected Release (jobs completing this quarter):                      $45,000      │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

---

## Troubleshooting Invoice Issues

### Issue: Invoice Doesn't Match Pay App

**SYMPTOMS:**
- Invoice total different from pay app
- Customer questions billing

**RESOLUTION:**
1. Pull both documents side by side
2. Identify line item differences
3. Correct QBO invoice OR
4. Issue corrected pay app
5. Document changes

### Issue: Duplicate Invoices

**SYMPTOMS:**
- AR overstated
- Customer received two invoices

**RESOLUTION:**
1. Identify duplicate
2. Void or delete duplicate invoice
3. Notify customer if already sent
4. Review process to prevent recurrence

### Issue: Missing Retention

**SYMPTOMS:**
- Retention receivable doesn't match expected
- Invoice shows different retention amount

**RESOLUTION:**
1. Review each invoice for retention line
2. Add missing retention entries
3. Adjust retention receivable as needed

### Issue: Payment Applied to Wrong Invoice

**SYMPTOMS:**
- Old invoice shows paid, new invoice open
- AR aging incorrect

**RESOLUTION:**
1. Find the payment transaction
2. Edit and reapply to correct invoice
3. Verify AR aging corrected

---

## Best Practices Summary

### Daily Practices

- [ ] Review AR aging for overdue items
- [ ] Follow up on past-due amounts
- [ ] Apply payments same day received

### Weekly Practices

- [ ] Review all active projects for billing status
- [ ] Verify pay apps prepared and submitted
- [ ] Match QBO invoices to pay apps

### Monthly Practices

- [ ] Complete AR-to-WIP reconciliation
- [ ] Prepare billing summary report
- [ ] Review retention balances
- [ ] Investigate and resolve all differences

---

*[← Previous: Vendor Setup & AP](./04-vendor-setup-ap.md) | [Back to Introduction →](../01-introduction.md)*
