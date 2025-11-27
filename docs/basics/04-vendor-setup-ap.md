# Vendor Setup & Accounts Payable Management

## Overview

Proper vendor setup is essential for construction accounting. This chapter provides detailed instructions for creating vendors optimized for job costing, managing accounts payable, and ensuring seamless assignment of costs to projects.

---

## Why Vendor Setup Matters

### The Problem with Poor Vendor Setup

```
POOR VENDOR SETUP:
- Vendor: "Home Depot"
- No address, no terms, no default account
- Every transaction requires manual entry of all details
- Can't generate 1099s at year-end
- No visibility into spending by vendor

PROPER VENDOR SETUP:
- Vendor: "Home Depot Store #1234"
- Full W-9 information captured
- Default expense account: 51000 Materials
- Terms: Due on receipt
- Automatic 1099 tracking
- Spending history at a glance
```

---

## Step-by-Step: Creating a New Vendor

### Navigate to Vendor Center

**HOW:**
1. Click **Expenses** in left navigation
2. Click **Vendors** tab
3. Click **New vendor**

### Complete Vendor Information

**Section 1: Basic Information**

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                              NEW VENDOR                                              │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  VENDOR INFORMATION                                                                  │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  Company:      [ABC Electrical Contractors, Inc.]                                   │
│                                                                                      │
│  Display name: [ABC Electrical - Main]  ◄── What shows in QBO dropdowns            │
│                                                                                      │
│  ☑ Use display name in transactions                                                │
│                                                                                      │
│  Print name:   [ABC Electrical Contractors, Inc.]  ◄── What prints on checks       │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**Section 2: Address Information**

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  ADDRESS                                                                             │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  Street:  [123 Industrial Parkway]                                                  │
│  City:    [Anytown]                                                                  │
│  State:   [CA]                                                                       │
│  ZIP:     [90210]                                                                    │
│  Country: [United States]                                                            │
│                                                                                      │
│  Note: Address pre-fills on bills and checks                                        │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**Section 3: Contact Information**

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  CONTACT DETAILS                                                                     │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  First name: [John]                                                                  │
│  Last name:  [Smith]                                                                 │
│  Email:      [john@abcelectrical.com]  ◄── For sending POs, remittances            │
│  Phone:      [(555) 123-4567]                                                        │
│  Mobile:     [(555) 987-6543]                                                        │
│  Fax:        [(555) 123-4568]                                                        │
│  Website:    [www.abcelectrical.com]                                                │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**Section 4: Payment Information (CRITICAL)**

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  PAYMENT AND BILLING                                                                 │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  Terms:        [Net 30 ▼]  ◄── Auto-calculates due dates on bills                   │
│                                                                                      │
│  Opening balance: [$0.00]                                                            │
│  as of:          [01/01/2024]                                                        │
│                                                                                      │
│  Account no.:    [CUST-12345]  ◄── Your account number with vendor                  │
│                                                                                      │
│  Credit limit:   [$50,000.00]  (optional)                                           │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**Section 5: Tax Information (ESSENTIAL FOR 1099s)**

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  TAX INFORMATION                                                                     │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  Business ID (EIN/SSN): [12-3456789]  ◄── From W-9                                  │
│                                                                                      │
│  ☑ Track payments for 1099  ◄── CHECK THIS FOR SUBS!                               │
│                                                                                      │
│  Note: Subcontractors, landlords, and other service providers                       │
│        typically require 1099 reporting if paid $600+ annually                      │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**Section 6: Default Account (Time Saver)**

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  ADDITIONAL INFO                                                                     │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  Default expense account: [52600 Sub - Electrical ▼]                                │
│                                                                                      │
│  Note: This account pre-fills when you create a bill for this vendor.              │
│        You can override it on individual transactions.                              │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  Notes:                                                                              │
│  [Electrical subcontractor - commercial/residential                                 │
│   License #12345                                                                     │
│   Primary contact: John Smith                                                        │
│   Typical lead time: 1 week for small jobs]                                         │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Save the Vendor

Click **Save** to create the vendor.

---

## Vendor Setup by Type

### Subcontractor Vendors

**CRITICAL SETTINGS:**
- ☑ Track payments for 1099
- Business ID (EIN): Required
- Terms: Match your subcontract (typically Net 30)
- Default account: 52XXX Subcontractor expense account

**RECOMMENDED NAMING:**
```
[Trade] - [Company Name]
Examples:
- Electrical - ABC Electric
- Plumbing - Smith Plumbing Inc
- HVAC - Johnson Mechanical
- Drywall - Quality Drywall Services
```

**WHY THIS NAMING:**
- Sorts vendors by trade in dropdown
- Easy to find correct vendor
- Visible trade on reports

### Material Supplier Vendors

**CRITICAL SETTINGS:**
- Terms: Usually Net 30 or On Receipt
- Default account: 51XXX Materials expense
- ☑ Track for 1099: Usually NO (corporations exempt)

**COMMON SUPPLIERS:**
```
Name                    Default Account         1099?
──────────────────────────────────────────────────────────
Home Depot              51000 Materials         No
Lowe's                  51000 Materials         No  
Local Lumber Yard       51100 Lumber & Framing  No
Electrical Supply Co    51300 Electrical Mat.   Maybe
Plumbing Wholesale      51400 Plumbing Mat.     Maybe
```

### Equipment Rental Vendors

**CRITICAL SETTINGS:**
- Terms: Varies (often due on return)
- Default account: 54200 Equipment Rental
- 1099: Usually NO (corporations)

**EXAMPLES:**
```
- United Rentals
- Sunbelt Rentals
- Herc Rentals
- Local rental companies
```

### Utility/Overhead Vendors

**CRITICAL SETTINGS:**
- Default account: Appropriate overhead account
- Terms: Usually Net 15-30
- 1099: Usually NO

**EXAMPLES:**
```
Vendor                  Default Account
──────────────────────────────────────────────────
Electric Company        61300 Utilities
Gas Company             61300 Utilities
Phone Provider          63300 Telephone
Internet Provider       63300 Internet
Insurance Company       64100 Insurance
```

---

## Managing W-9 and 1099 Requirements

### When to Collect W-9

**REQUIRED W-9:**
- All subcontractors (before first payment)
- Landlords (if applicable)
- Professional services (accountants, lawyers if not incorporated)
- Any service provider you'll pay $600+ annually

**NOT REQUIRED:**
- Corporations (but good practice to collect anyway)
- Material suppliers (product purchases)
- Utility companies

### W-9 Workflow

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                           W-9 COLLECTION WORKFLOW                                    │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  1. BEFORE FIRST JOB                                                                 │
│     ├── Send W-9 request to new vendor                                              │
│     └── Include with subcontract package                                            │
│                                                                                      │
│  2. RECEIVE W-9                                                                      │
│     ├── Verify information is complete                                              │
│     ├── Check EIN/SSN format is correct                                             │
│     └── Confirm entity type matches                                                 │
│                                                                                      │
│  3. ENTER IN QBO                                                                     │
│     ├── Add Business ID (EIN) to vendor record                                      │
│     ├── Check "Track payments for 1099"                                             │
│     └── Attach W-9 PDF to vendor                                                    │
│                                                                                      │
│  4. FILE SECURELY                                                                    │
│     └── Keep W-9 for 4 years minimum                                                │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### 1099 Tracking in QBO

**HOW TO VERIFY 1099 SETUP:**
1. Go to **Expenses** → **Vendors**
2. Find the vendor
3. Click to edit
4. Verify:
   - Business ID is entered
   - "Track payments for 1099" is checked
   - Entity type is correct

**HOW TO RUN 1099 REPORT:**
1. Go to **Reports** → Search "1099"
2. Select "1099 Transaction Detail Report"
3. Set date range (calendar year)
4. Review for completeness

---

## Recording Vendor Bills: Complete Workflow

### Step 1: Receive and Review Invoice

Before entering, verify:
- [ ] Invoice is addressed to your company
- [ ] Work/materials match what was ordered
- [ ] Prices match quote/contract
- [ ] Job number is clear

### Step 2: Enter the Bill

**HOW:**
1. Go to **+ New** → **Bill**
2. Select Vendor from dropdown
3. Enter bill details:

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                   BILL                                               │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Vendor: [ABC Electrical ▼]      Mailing address: (auto-fills)                      │
│                                                                                      │
│  Terms: [Net 30 ▼] (auto-fills from vendor)                                         │
│  Bill date: [03/25/2024]                                                             │
│  Due date: [04/24/2024] (auto-calculates)                                           │
│                                                                                      │
│  Bill no.: [INV-2024-0178]  ◄── ENTER VENDOR'S INVOICE NUMBER                       │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Step 3: Add Line Items with Job Assignment

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  ITEM DETAILS                                                                        │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  #  │ PRODUCT/SERVICE      │ DESCRIPTION               │ QTY │ RATE    │ AMOUNT     │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  1  │ [Sub - Electrical ▼] │ [Rough-in per contract]   │ 1   │ $12,000 │ $12,000    │
│      │                      │                           │     │         │            │
│      │ Customer: [2024-015-Johnson-Kitchen ▼]  ◄── CRITICAL!                        │
│      │ ☑ Billable  (if marking up to customer)                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│  2  │ [Retention Payable ▼]│ [10% retention held]      │ 1   │ -$1,200 │ -$1,200    │
│      │                      │                           │     │         │            │
│      │ Customer: [2024-015-Johnson-Kitchen ▼]                                        │
│      │ ☐ Billable                                                                    │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│                                                   TOTAL:            $10,800          │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Step 4: Attach Documentation

**ALWAYS ATTACH:**
- Vendor invoice (PDF or photo)
- Lien waiver (if received)
- PO or contract reference

**HOW:**
1. Click **Attachments** at bottom
2. Drag and drop files or click to browse
3. Files attach to this bill

### Step 5: Save

Click **Save and close** or **Save and new**

---

## Bills from Subcontractor Pay Applications

### Understanding Sub Pay Apps

Subcontractors often submit pay applications similar to your pay apps to the GC:
- Schedule of Values breakdown
- Percentage complete by line item
- Retention calculations
- Backup documentation

### Recording a Sub Pay App

**SCENARIO:**
Sub submits pay app for $50,000 with 10% retention

**HOW TO RECORD:**

```
BILL ENTRY:
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                      │
│  Line 1: Sub - [Trade]                                                              │
│          Description: Pay App #3 - [Date range]                                     │
│          Amount: $50,000                                                             │
│          Customer: [Job Name]                                                        │
│          Billable: ☑ (if passing through)                                           │
│                                                                                      │
│  Line 2: Retention Payable                                                          │
│          Description: 10% retention per contract                                    │
│          Amount: -$5,000                                                             │
│          Customer: [Job Name]                                                        │
│          Billable: ☐                                                                │
│                                                                                      │
│  BILL TOTAL: $45,000 (what you'll pay now)                                          │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

**RESULT:**
- Subcontractor expense: $50,000 (job cost)
- Accounts Payable: $45,000 (pay now)
- Retention Payable: $5,000 (pay later)

---

## Mapping Vendor Invoices to Your Pay Apps

### The Connection: Vendor Bills → Your Invoices

```
                    FLOW OF COSTS AND BILLING
                    
Vendor Invoice                              Your Invoice
────────────────                            ─────────────
ABC Electric: $12,000 ──────┐
                            │
DEF Plumbing: $8,000 ──────┼────► TOTAL COSTS ────► Progress Billing
                            │     to Job ABC       to Customer
GHI Materials: $5,000 ─────┘
XYZ Lumber: $3,000 ─────────┘

Total Costs: $28,000 ────► Invoice includes Sub + Materials + Markup
```

### Creating Invoice from Billable Expenses

**SCENARIO:**
You have billable expenses totaling $28,000 ready to invoice

**HOW:**
1. Create new Invoice for customer
2. Look for **Billable Expenses** panel on right side
3. Select items to add to invoice

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                  INVOICE                                             │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Customer: [Smith Residence ▼]                                                       │
│  Project: [2024-015-Johnson-Kitchen ▼]                                              │
│                                                                                      │
├───────────────────────────────────────────────────────────────────────────┬─────────┤
│  INVOICE LINE ITEMS                                                       │ BILLABLE│
│  ─────────────────────────────────────────────────────────────────────────│ EXPENSES│
│  Add manually:                                                            │ ────────│
│  1. Labor - General    80 hrs @ $75    $6,000                             │         │
│                                                                           │ ☑ ABC   │
│  Add from Billable:                                                       │   Elec  │
│  2. Sub - Electrical   ABC inv 3/25    $12,000  ◄── Added from billable  │   $12K  │
│  3. Sub - Plumbing     DEF inv 3/22    $8,000   ◄── Added from billable  │         │
│  4. Materials          GHI/XYZ         $8,000   ◄── Added from billable  │ ☑ DEF   │
│                                                                           │   Plumb │
│  ─────────────────────────────────────────────────────────────────────────│   $8K   │
│  Subtotal:                             $34,000                            │         │
│  Less Retention:                       -$3,400                            │ ☑ Mat'ls│
│  TOTAL DUE:                            $30,600                            │   $8K   │
│                                                                           │         │
└───────────────────────────────────────────────────────────────────────────┴─────────┘
```

### Tracking What's Been Billed

**HOW TO SEE UNBILLED COSTS:**
1. Go to **Reports** → "Unbilled Charges"
2. Filter by Customer/Project
3. See all billable items not yet invoiced

**WHY THIS MATTERS:**
- Ensures you don't forget to bill costs
- Shows pass-through items awaiting invoice
- Identifies potential cash flow issues

---

## AP Aging and Payment Management

### Running AP Aging Report

**HOW:**
1. Go to **Reports** → "A/P Aging Summary"
2. Review outstanding bills by age

```
A/P AGING SUMMARY
As of 04/15/2024

                        CURRENT   1-30    31-60   61-90   91+     TOTAL
─────────────────────────────────────────────────────────────────────────
ABC Electrical          $10,800   $0      $0      $0      $0      $10,800
DEF Plumbing            $0        $7,200  $0      $0      $0      $7,200
Home Depot              $1,234    $567    $0      $0      $0      $1,801
XYZ Materials           $0        $0      $3,456  $0      $0      $3,456  ⚠️
─────────────────────────────────────────────────────────────────────────
TOTAL                   $12,034   $7,767  $3,456  $0      $0      $23,257
```

### Managing Cash Flow with AP

**BEST PRACTICE WORKFLOW:**

```
Weekly AP Review:
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                      │
│  1. Run AP Aging Summary                                                             │
│                                                                                      │
│  2. Identify bills due this week                                                     │
│                                                                                      │
│  3. Check available cash                                                             │
│                                                                                      │
│  4. Prioritize payments:                                                             │
│     ├── Critical vendors (keep you working)                                         │
│     ├── Subcontractors (relationship + lien risk)                                   │
│     ├── Terms with early pay discounts                                              │
│     └── Other vendors                                                                │
│                                                                                      │
│  5. Schedule payments in Pay Bills                                                   │
│                                                                                      │
│  6. Update cash flow forecast                                                        │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

---

## Vendor Management Best Practices

### Vendor Naming Convention

**RECOMMENDED FORMAT:**
```
[Category] - [Company Name]
Examples:
Sub - ABC Electrical
Sub - DEF Plumbing  
Mat - Home Depot #1234
Rent - United Rentals
```

**WHY:**
- Sorts vendors by type
- Easy to find in dropdowns
- Clear on reports

### Handling Multiple Locations

**SCENARIO:** You shop at multiple Home Depot stores

**OPTION 1: Single Vendor**
- Create one "Home Depot" vendor
- Track individual store in memo field
- Simpler, fewer vendors

**OPTION 2: Multiple Vendors**
- "Home Depot #1234 - Main Street"
- "Home Depot #5678 - Industrial Blvd"
- More tracking, more detail

**RECOMMENDATION:** Use Option 1 unless you need store-level reporting

### Inactive Vendors

**WHEN TO MAKE INACTIVE:**
- Vendor no longer in business
- You no longer use vendor
- Vendor was created in error (duplicate)

**HOW:**
1. Go to **Expenses** → **Vendors**
2. Find vendor
3. Click **Edit**
4. Check "Make inactive"
5. Save

**NOTE:** Inactive vendors:
- Don't appear in dropdowns
- Historical transactions remain
- Can be reactivated if needed

---

## Vendor Checklist

### New Vendor Setup:
- [ ] Collect W-9 (for subs and 1099-required vendors)
- [ ] Create vendor in QBO
- [ ] Enter complete contact information
- [ ] Set appropriate payment terms
- [ ] Set default expense account
- [ ] Enter EIN/SSN for 1099 tracking
- [ ] Check "Track payments for 1099" if applicable
- [ ] Attach W-9 PDF to vendor record

### Ongoing Vendor Management:
- [ ] Keep contact information updated
- [ ] Review AP aging weekly
- [ ] Pay within terms to maintain relationships
- [ ] Track lien waiver receipt
- [ ] Annual W-9 verification (if info changed)

### Year-End:
- [ ] Run 1099 report
- [ ] Verify all 1099 vendors have EIN
- [ ] Request missing W-9s
- [ ] File 1099s by deadline (January 31)

---

*[← Previous: Recording Transactions](./03-recording-transactions.md) | [Next: Invoice Tie-Out & Reconciliation →](./05-invoice-tieout.md)*
