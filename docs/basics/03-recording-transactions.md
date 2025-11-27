# Recording Transactions in QuickBooks Online

## Overview

This chapter provides detailed, step-by-step instructions for recording every type of transaction you'll encounter in construction bookkeeping. We'll cover the complete workflow from receipt to reconciliation.

---

## The Transaction Workflow

### Understanding the Complete Cycle

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                        CONSTRUCTION TRANSACTION CYCLE                                │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│   PURCHASE CYCLE                           SALES CYCLE                               │
│   ──────────────                           ──────────────                            │
│                                                                                      │
│   1. Receive goods/services                1. Perform work                           │
│         ↓                                       ↓                                    │
│   2. Receive vendor invoice                2. Create invoice/pay app                 │
│         ↓                                       ↓                                    │
│   3. Enter bill in QBO                     3. Send to customer                       │
│         ↓                                       ↓                                    │
│   4. Pay bill when due                     4. Receive payment                        │
│         ↓                                       ↓                                    │
│   5. Match to bank feed                    5. Match to bank feed                     │
│         ↓                                       ↓                                    │
│   6. Reconcile at month-end                6. Reconcile at month-end                 │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

---

## Part 1: Recording Expenses

### Method 1: Enter a Bill (For Invoices You'll Pay Later)

**USE FOR:**
- Subcontractor invoices
- Material supplier invoices
- Equipment rental invoices
- Any invoice with payment terms (Net 15, Net 30, etc.)

**WHY USE BILLS:**
- Tracks what you owe (Accounts Payable)
- Shows aging of payables
- Enables payment scheduling
- Matches to pay apps from subs

**STEP-BY-STEP:**

1. **Navigate to Bills**
   - Go to **+ New** → **Bill**
   
2. **Fill in Header Information**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                   BILL                                               │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Vendor: [ABC Electrical Subcontractor ▼]                                           │
│                                                                                      │
│  Mailing address:                    Terms: [Net 30 ▼]                              │
│  123 Main Street                     Bill date: [03/15/2024]                        │
│  Anytown, ST 12345                   Due date: [04/14/2024] (auto-calculates)       │
│                                                                                      │
│  Bill no.: [INV-2024-0156]  ◄── Vendor's invoice number                             │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Add Line Items (CRITICAL for Job Costing)**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  ITEM DETAILS (Use for job costing)                                                  │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  #  │ PRODUCT/SERVICE          │ DESCRIPTION           │ QTY │ RATE    │ AMOUNT     │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  1  │ [Sub - Electrical    ▼]  │ [Rough-in electrical] │ 1   │ $8,500  │ $8,500.00  │
│                                                                                      │
│  Customer: [2024-015-Johnson-Kitchen ▼]  ◄── ALWAYS assign to job!                  │
│  ☑ Billable  (if you'll invoice customer for this)                                  │
│                                                                                      │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  2  │ [Retention Payable   ▼]  │ [10% retention held ] │ 1   │ -$850   │ -$850.00   │
│                                                                                      │
│  Customer: [2024-015-Johnson-Kitchen ▼]                                              │
│  ☐ Billable                                                                          │
│                                                                                      │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                   BILL TOTAL:        $7,650.00       │
│                                                   (Invoice - Retention)              │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

4. **Attach Documentation**
   - Click **Attachments**
   - Upload vendor invoice PDF
   - Upload any lien waivers

5. **Save**
   - Click **Save and close** (or **Save and new** for more bills)

### Method 2: Record an Expense (For Immediate Payments)

**USE FOR:**
- Debit card purchases
- Cash purchases (petty cash)
- Reimbursements
- Small purchases already paid

**WHY USE EXPENSE:**
- Faster than Bill + Payment
- Good for one-time immediate purchases
- Links directly to bank feed

**STEP-BY-STEP:**

1. **Navigate to Expense**
   - Go to **+ New** → **Expense**

2. **Fill in Payment Information**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                  EXPENSE                                             │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Payee: [Home Depot ▼]                                                              │
│                                                                                      │
│  Payment account: [Checking - Operating ▼]  ◄── Account money came from             │
│  Payment date: [03/15/2024]                                                          │
│  Payment method: [Debit Card ▼]                                                      │
│  Ref no.: [Check #1234 or Card ****5678]                                            │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Add Line Items**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  ITEM DETAILS                                                                        │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  #  │ PRODUCT/SERVICE          │ DESCRIPTION           │ AMOUNT    │ CUSTOMER       │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  1  │ [Materials - Lumber  ▼]  │ [2x4 framing lumber ] │ $456.78   │ [Johnson Kit ▼]│
│  2  │ [Materials - Hardware▼]  │ [Fasteners, nails   ] │ $123.45   │ [Johnson Kit ▼]│
│                                                                                      │
│  ☑ Billable  (check for each line you'll invoice)                                   │
│                                                                                      │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                   TOTAL:             $580.23         │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

4. **Attach Receipt**
   - Click **Attachments**
   - Upload photo of receipt

5. **Save**

### Method 3: Write a Check

**USE FOR:**
- Handwritten checks
- Printed checks from QBO
- When you need a check record specifically

**STEP-BY-STEP:**

1. **Navigate to Check**
   - Go to **+ New** → **Check**

2. **Fill in Check Details**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                   CHECK                                              │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Payee: [ABC Materials Supply ▼]                                                    │
│                                                                                      │
│  Bank account: [Checking - Operating ▼]                                             │
│  Payment date: [03/15/2024]                                                          │
│  Check no.: [1234]  ◄── Enter actual check number                                   │
│                                                                                      │
│  Print later: ☐  (check if printing from QBO)                                       │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Add Line Items** (same as Bill)

4. **Save and/or Print**

---

## Part 2: Recording Income

### Method 1: Create an Invoice (Standard Billing)

**USE FOR:**
- T&M (Time & Materials) billing
- Service invoices
- Simple progress billing
- Change order billing

**STEP-BY-STEP:**

1. **Navigate to Invoice**
   - Go to **+ New** → **Invoice**

2. **Fill in Header Information**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                  INVOICE                                             │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Customer: [Smith Residence ▼]                                                       │
│                                                                                      │
│  Project: [2024-015-Johnson-Kitchen ▼]  ◄── CRITICAL: Select project                │
│                                                                                      │
│  Invoice date: [03/31/2024]                                                          │
│  Due date: [04/30/2024]                                                              │
│  Terms: [Net 30 ▼]                                                                  │
│                                                                                      │
│  Invoice no.: [1045]  (auto-generated or manual)                                    │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Add Line Items**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  PRODUCT/SERVICE                                                                     │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  #  │ PRODUCT/SERVICE       │ DESCRIPTION              │ QTY   │ RATE    │ AMOUNT   │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  1  │ [Labor - General  ▼]  │ [Framing labor 3/1-3/15] │ 80 hrs│ $75.00  │ $6,000   │
│  2  │ [Materials         ▼] │ [Lumber per attached    ]│ 1     │ $2,500  │ $2,500   │
│  3  │ [Sub - Electrical  ▼] │ [Rough-in per invoice   ]│ 1     │ $8,500  │ $8,500   │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│                                                       SUBTOTAL:         $17,000      │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│  4  │ [Retention Held    ▼] │ [10% retention          ]│ 1     │ -$1,700 │ -$1,700  │
│  ─────────────────────────────────────────────────────────────────────────────────  │
│                                                       TOTAL DUE:        $15,300      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

4. **Add Billable Expenses (if any)**
   - If you marked expenses as Billable, they appear in sidebar
   - Click to add them to invoice

```
┌───────────────────────────────────────┐
│  BILLABLE EXPENSES                    │
├───────────────────────────────────────┤
│  ☑ Home Depot 3/12     $580.23        │
│  ☑ Lowe's 3/14         $234.56        │
│                                       │
│  [Add to invoice]                     │
└───────────────────────────────────────┘
```

5. **Customize and Review**
   - Click **Customize** to adjust layout
   - Review all line items
   - Verify math

6. **Save and Send**
   - **Save and close**: Save draft
   - **Save and send**: Email to customer
   - **Print or preview**: Create PDF

### Method 2: Receive Payment

**USE FOR:**
- Recording customer payments against invoices
- Applying payments to specific invoices
- Partial payments

**STEP-BY-STEP:**

1. **Navigate to Receive Payment**
   - Go to **+ New** → **Receive Payment**

2. **Fill in Payment Details**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                              RECEIVE PAYMENT                                         │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Customer: [Smith Residence ▼]                                                       │
│                                                                                      │
│  Payment date: [04/10/2024]                                                          │
│  Payment method: [Check ▼]                                                          │
│  Reference no.: [Check #5678]                                                        │
│                                                                                      │
│  Deposit to: [Undeposited Funds ▼]  or  [Checking ▼]                                │
│                                                                                      │
│  Amount received: [$15,300.00]                                                       │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Apply to Outstanding Invoices**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  OUTSTANDING TRANSACTIONS                                                            │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  ☑  Invoice #1045  03/31/24  Due 04/30/24  $15,300.00  Payment: [$15,300.00]       │
│  ☐  Invoice #1032  02/28/24  Due 03/30/24   $8,500.00  Payment: [$0.00]            │
│                                                                                      │
│  Amount to apply: $15,300.00                                                         │
│  Amount to credit: $0.00                                                             │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

4. **Save**

### Method 3: Bank Deposit (For Multiple Payments)

**USE FOR:**
- Depositing multiple checks at once
- Moving from Undeposited Funds to bank
- Recording actual bank deposit

**STEP-BY-STEP:**

1. **Navigate to Bank Deposit**
   - Go to **+ New** → **Bank Deposit**

2. **Select Payments to Include**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                               BANK DEPOSIT                                           │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Account: [Checking - Operating ▼]                                                  │
│  Date: [04/10/2024]                                                                  │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  SELECT PAYMENTS TO DEPOSIT                                                          │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  ☑  04/10  Smith Residence      Payment      Check #5678      $15,300.00            │
│  ☑  04/10  Johnson Commercial   Payment      Check #9012       $8,500.00            │
│  ☑  04/09  ABC Corporation      Payment      ACH              $25,000.00            │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  SELECTED PAYMENTS TOTAL:                                      $48,800.00            │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Add Cash/Other Items (if any)**
   - Add any cash received
   - Add any items not previously recorded

4. **Save**
   - Creates single deposit matching your bank statement

---

## Part 3: Paying Bills

### Method 1: Pay Bills (Recommended)

**USE FOR:**
- Paying entered bills
- Scheduling payments
- Tracking what's been paid

**STEP-BY-STEP:**

1. **Navigate to Pay Bills**
   - Go to **+ New** → **Pay Bills**

2. **Select Bills to Pay**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                 PAY BILLS                                            │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Payment account: [Checking - Operating ▼]                                          │
│  Payment date: [04/14/2024]                                                          │
│                                                                                      │
│  Filter: [All ▼]  Show: [Last 365 days ▼]                                           │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  PAYEE           │ REF NO.      │ DUE DATE  │ OPEN BALANCE │ CREDIT │ PAYMENT       │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  ☑ ABC Electric   INV-2024-156   04/14/24   $7,650.00      $0.00    [$7,650.00]     │
│  ☑ Home Depot     Various        04/10/24   $1,234.56      $0.00    [$1,234.56]     │
│  ☐ XYZ Plumbing   PLB-001        04/20/24   $3,500.00      $0.00    [$0.00]         │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                             TOTAL PAYMENT:           $8,884.56       │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

3. **Choose Payment Method**
   - **Print later**: Generate checks to print
   - **Check no.**: Enter manual check number
   - **ACH/Online**: Record electronic payment

4. **Save and Print/Pay**

### Method 2: Quick Pay from Bill

**SHORTCUT:**
1. Open the bill
2. Click **Pay bill** button
3. Complete payment details
4. Save

---

## Part 4: Recording Journal Entries

### When to Use Journal Entries

**USE FOR:**
- Month-end adjustments
- WIP adjustments
- Depreciation
- Reclassifying transactions
- Correcting errors
- Internal equipment charges

**DO NOT USE FOR:**
- Regular bills (use Bill)
- Regular invoices (use Invoice)
- Payments (use Pay Bills/Receive Payment)

### Creating a Journal Entry

**STEP-BY-STEP:**

1. **Navigate to Journal Entry**
   - Go to **+ New** → **Journal Entry**

2. **Fill in the Entry**
```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                              JOURNAL ENTRY                                           │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Journal date: [03/31/2024]                                                          │
│  Journal no.: [JE-2024-015]  (auto-generated)                                       │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  #  │ ACCOUNT                  │ DEBITS    │ CREDITS   │ DESCRIPTION  │ CUSTOMER    │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  1  │ 50420 Equipment - Owned  │ $2,500.00 │           │ Excavator    │ Johnson Kit │
│  2  │ 60430 Depreciation Exp   │           │ $2,500.00 │ Offset       │             │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                 $2,500.00   $2,500.00   ◄── Must balance!            │
│                                                                                      │
│  Memo: [Monthly equipment allocation per usage log]                                  │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**RULES:**
- Debits MUST equal Credits
- Include Customer for job-related entries
- Always add descriptive Memo
- Attach supporting documentation

### Common Construction Journal Entries

**1. WIP Adjustment (Under-billing)**
```
Dr. 12500 Costs in Excess of Billings    $10,000
    Cr. 40000 Contract Revenue                      $10,000
Memo: WIP adjustment per schedule dated 3/31/24
```

**2. WIP Adjustment (Over-billing)**
```
Dr. 40000 Contract Revenue               $5,000
    Cr. 24500 Billings in Excess of Costs           $5,000
Memo: WIP adjustment per schedule dated 3/31/24
```

**3. Equipment Allocation**
```
Dr. 50420 Equipment - Owned              $3,500  [Johnson Kitchen]
Dr. 50420 Equipment - Owned              $2,000  [Smith Addition]
    Cr. 60430 Equipment Depreciation                $5,500
Memo: Monthly equipment allocation per usage log
```

**4. Depreciation Entry**
```
Dr. 62500 Depreciation - Vehicles        $1,500
Dr. 62600 Depreciation - Equipment       $2,000
    Cr. 15350 Accum Depr - Vehicles                 $1,500
    Cr. 15450 Accum Depr - Equipment                $2,000
Memo: Monthly depreciation
```

---

## Part 5: Transaction Entry Best Practices

### Always Complete These Fields

| Transaction Type | Required Fields |
|-----------------|-----------------|
| **Bill** | Vendor, Date, Amount, Account, Customer (for job costs) |
| **Expense** | Payee, Date, Amount, Account, Customer (for job costs) |
| **Invoice** | Customer, Project, Date, Items, Amounts |
| **Payment** | Customer, Date, Amount, Invoice applied to |
| **Journal Entry** | Date, Accounts, Amounts, Customer (if applicable), Memo |

### The Customer Field is Critical

**FOR EVERY JOB COST:**
- Bills for materials → Assign to Project
- Bills for subs → Assign to Project
- Credit card purchases → Assign to Project
- Equipment charges → Assign to Project

**WITHOUT CUSTOMER:**
- Cost goes to total COGS
- Doesn't appear on job reports
- Job profitability is wrong

### Memo/Description Best Practices

Good memo helps future you understand the transaction:

**BAD:** "Materials"
**GOOD:** "Framing lumber for 2nd floor addition - delivery 3/15"

**BAD:** "Payment"
**GOOD:** "Progress payment #3 per pay app dated 3/28"

**BAD:** "JE"
**GOOD:** "WIP adjustment per schedule 3/31/24 - reviewed by J.Smith"

---

## Transaction Entry Checklist

### Before Entering Any Transaction:
- [ ] Have source document (invoice, receipt, contract)
- [ ] Know which job it relates to
- [ ] Know correct expense/income account
- [ ] Have vendor/customer set up

### When Entering:
- [ ] Select correct vendor/customer
- [ ] Enter correct date
- [ ] Enter reference number (invoice #, check #)
- [ ] Select correct account/category
- [ ] Assign to Customer/Project for job costs
- [ ] Add meaningful description
- [ ] Attach source document

### After Entering:
- [ ] Verify amount is correct
- [ ] Verify job assignment is correct
- [ ] Match to bank feed when available
- [ ] File/scan original document

---

*[← Previous: Connecting Credit Cards](./02-connecting-credit-cards.md) | [Next: Vendor Setup & AP Management →](./04-vendor-setup-ap.md)*
