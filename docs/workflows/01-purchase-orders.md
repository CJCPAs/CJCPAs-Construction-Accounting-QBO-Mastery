# Purchase Orders and Three-Way Matching

## Overview

Purchase Orders (POs) are critical control documents for construction companies. They authorize spending, set expectations with vendors, and enable verification of bills before payment. This guide covers PO creation, approval workflows, receiving, and three-way matching.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Consult with a qualified CPA before implementing. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Why Purchase Orders Matter](#why-purchase-orders-matter)
2. [Enabling Purchase Orders](#enabling-purchase-orders)
3. [Creating Purchase Orders](#creating-purchase-orders)
4. [Purchase Order Workflow](#purchase-order-workflow)
5. [Receiving Against POs](#receiving-against-pos)
6. [Matching POs to Bills](#matching-pos-to-bills)
7. [Three-Way Matching](#three-way-matching)
8. [PO Templates and Best Practices](#po-templates-and-best-practices)
9. [Troubleshooting](#troubleshooting)

---

## Why Purchase Orders Matter

### The Cost Control Problem

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    WITHOUT PURCHASE ORDERS                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  SCENARIO: Project Manager calls supplier, orders $15,000 in materials      │
│                                                                              │
│  Problems:                                                                   │
│  • No written authorization → who approved this expense?                    │
│  • No budget check → is this within job budget?                             │
│  • No price verification → are we paying the quoted rate?                   │
│  • No documentation → did we receive what was ordered?                      │
│  • No job assignment → which job should this cost hit?                      │
│                                                                              │
│  Result:                                                                     │
│  ❌ Cost overruns go undetected until too late                              │
│  ❌ Duplicate orders happen                                                  │
│  ❌ Wrong job charged                                                        │
│  ❌ Overpayment to vendors                                                   │
│  ❌ No audit trail for bonding company                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│                    WITH PURCHASE ORDERS                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  SCENARIO: Project Manager creates PO, gets approval, sends to supplier     │
│                                                                              │
│  Benefits:                                                                   │
│  ✅ Written authorization with approver                                     │
│  ✅ Budget checked before ordering                                          │
│  ✅ Negotiated price locked in                                              │
│  ✅ Receiving documented when materials arrive                              │
│  ✅ Job automatically assigned                                              │
│  ✅ Bill matched against PO before payment                                  │
│                                                                              │
│  Result:                                                                     │
│  ✅ Catches budget overruns before they happen                              │
│  ✅ Prevents duplicate orders                                                │
│  ✅ Ensures correct job costing                                             │
│  ✅ Verifies vendor charges                                                  │
│  ✅ Complete audit trail                                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### When to Use Purchase Orders

| Transaction Type | Use PO? | Why |
|-----------------|---------|-----|
| Materials orders | ✅ Yes | Cost control, receiving verification |
| Subcontract work | ✅ Yes | Budget control, scope documentation |
| Equipment rental | ✅ Yes | Rate verification, duration tracking |
| Supplies (misc) | Optional | For amounts over threshold |
| Utilities | No | Recurring, no receiving |
| Fuel cards | No | Handled through card feeds |
| Petty cash | No | Too small for PO process |

### Bonding Company Requirements

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BONDING PERSPECTIVE                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Bonding companies evaluate contractors partially on internal controls.     │
│                                                                              │
│  Key questions they ask:                                                     │
│  • How do you authorize purchases?                                          │
│  • Who can commit the company to spending?                                  │
│  • How do you verify you received what you ordered?                         │
│  • How do you prevent unauthorized spending?                                │
│                                                                              │
│  A robust PO system demonstrates:                                            │
│  ✅ Management oversight of spending                                        │
│  ✅ Separation of duties                                                    │
│  ✅ Written authorization chain                                             │
│  ✅ Verification before payment                                             │
│                                                                              │
│  This can positively impact your bonding capacity!                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Enabling Purchase Orders

### Step-by-Step Setup

**Step 1: Enable PO Feature**

1. Navigate to Settings:
   ```
   ⚙️ Gear Icon → Account and Settings
   ```

2. Go to Expenses Tab:
   ```
   Expenses → Purchase orders
   ```

3. Enable:
   ```
   Use purchase orders: ON ✅
   ```

4. Save

**Step 2: Configure PO Settings**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PURCHASE ORDER SETTINGS                                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Custom transaction numbers: ON                                              │
│  └── Allows manual PO numbering                                             │
│      Recommended format: PO-YYYY-JOB-SEQ                                    │
│      Example: PO-2024-001-015                                               │
│                                                                              │
│  Default message on purchase orders:                                         │
│  └── Enter your standard terms and conditions                               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Step 3: Create PO Template**

1. Go to Custom Form Styles:
   ```
   ⚙️ Gear → Custom Form Styles → New Style → Purchase Order
   ```

2. Configure template:
   - Add company logo
   - Include job/project field
   - Add ship-to address
   - Add terms and conditions
   - Include approval signature line

**Step 4: Set Up Custom Fields**

```
Navigate: ⚙️ → Custom Fields

Create fields for Purchase Orders:
┌─────────────────────────────────────────────────────────────────────────────┐
│  RECOMMENDED PO CUSTOM FIELDS                                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Field 1: Job Number                                                         │
│  └── Type: Text                                                              │
│      Show on forms: Yes                                                      │
│                                                                              │
│  Field 2: Approved By                                                        │
│  └── Type: Dropdown                                                          │
│      Options: [List of authorized approvers]                                │
│      Show on forms: Yes                                                      │
│                                                                              │
│  Field 3: Ship To Site                                                       │
│  └── Type: Text                                                              │
│      Show on forms: Yes                                                      │
│      (Job site address)                                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Creating Purchase Orders

### Step-by-Step: Create a New PO

**Scenario:** Order $5,200 in framing lumber for the Smith Residence project.

**Step 1: Start New PO**

```
Navigation: + New → Purchase Order
```

**Step 2: Fill Header Information**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PURCHASE ORDER - HEADER                                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Vendor: [ABC Lumber Supply ▼]                                              │
│  └── Select from vendor list or create new                                  │
│                                                                              │
│  Mailing address: [Auto-fills from vendor]                                  │
│                                                                              │
│  Ship to: [456 Construction Lane, City, ST 12345]                           │
│  └── Job site address for delivery                                          │
│                                                                              │
│  Purchase Order date: [03/15/2024]                                          │
│                                                                              │
│  Custom fields:                                                              │
│  Job Number: [2024-001]                                                      │
│  Approved By: [John Smith - PM ▼]                                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Step 3: Enter Line Items**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  LINE ITEMS                                                                  │
├─────────────┬─────────────────────────┬─────────┬───────────┬───────────────┤
│ CATEGORY    │ DESCRIPTION             │ QTY     │ RATE      │ AMOUNT        │
├─────────────┼─────────────────────────┼─────────┼───────────┼───────────────┤
│ 50100       │ 2x4x8 SPF #2           │ 500     │ $4.25     │ $2,125.00     │
│ Materials   │ Studs for framing      │ EA      │           │               │
├─────────────┼─────────────────────────┼─────────┼───────────┼───────────────┤
│ 50100       │ 2x6x12 SPF #2          │ 200     │ $8.50     │ $1,700.00     │
│ Materials   │ Headers and blocking   │ EA      │           │               │
├─────────────┼─────────────────────────┼─────────┼───────────┼───────────────┤
│ 50100       │ 2x10x16 SPF #2         │ 80      │ $12.00    │ $960.00       │
│ Materials   │ Floor joists           │ EA      │           │               │
├─────────────┼─────────────────────────┼─────────┼───────────┼───────────────┤
│ 50100       │ Hardware/Fasteners     │ 1       │ $415.00   │ $415.00       │
│ Materials   │ Nails, hangers, plates │ LOT     │           │               │
├─────────────┴─────────────────────────┴─────────┴───────────┴───────────────┤
│                                                   TOTAL:     $5,200.00      │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Step 4: Assign Job/Class**

```
For each line item:
Customer/Project: Smith Family Trust
Class: 2024-001 Smith Residence

⚠️ CRITICAL: Assign class to EACH LINE for proper job costing!
```

**Step 5: Add Message/Instructions**

```
Message displayed on purchase order:
┌─────────────────────────────────────────────────────────────────────────────┐
│  Please deliver to job site address shown above.                            │
│  Call PM John Smith at (555) 123-4567 with ETA.                             │
│  Subject to attached terms and conditions.                                  │
│  Reference PO number on all invoices.                                       │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Step 6: Save and Send**

```
Options:
• Save: Creates PO in Open status
• Save and Send: Creates PO and emails to vendor
• Save and Print: Creates PO and generates PDF
```

### PO Numbering Best Practices

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PO NUMBERING CONVENTIONS                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Option 1: Sequential (Simple)                                               │
│  Format: PO-00001, PO-00002, etc.                                           │
│  Pros: Simple, no gaps                                                       │
│  Cons: No job information in number                                          │
│                                                                              │
│  Option 2: Job-Based                                                         │
│  Format: 2024-001-P01 (Year-Job-PO sequence)                                │
│  Pros: Easy to identify job from PO number                                  │
│  Cons: More complex numbering                                                │
│                                                                              │
│  Option 3: Category-Based                                                    │
│  Format: MAT-2024-0001 (Category-Year-Sequence)                             │
│  Categories: MAT (Materials), SUB (Subs), EQP (Equipment)                   │
│  Pros: Easy to categorize at a glance                                       │
│  Cons: Requires consistent category use                                      │
│                                                                              │
│  RECOMMENDATION: Job-Based for most contractors                             │
│  Example: 2024-001-P01 = First PO for job 2024-001                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Purchase Order Workflow

### Complete PO Lifecycle

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PURCHASE ORDER WORKFLOW                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   1. REQUISITION          2. APPROVAL           3. PO CREATION              │
│   ──────────────          ──────────            ─────────────               │
│   • Need identified       • Manager review      • Create in QBO             │
│   • Qty and specs         • Budget check        • Assign to job             │
│   • Quote obtained        • Authorization       • Send to vendor            │
│        │                       │                      │                     │
│        └───────────────────────┴──────────────────────┘                     │
│                                │                                             │
│                                ▼                                             │
│                         ┌─────────────┐                                     │
│                         │  PO SENT TO │                                     │
│                         │   VENDOR    │                                     │
│                         └──────┬──────┘                                     │
│                                │                                             │
│        ┌───────────────────────┼───────────────────────┐                    │
│        │                       │                       │                    │
│        ▼                       ▼                       ▼                    │
│   4. RECEIVING           5. VENDOR BILL         6. THREE-WAY MATCH         │
│   ────────────           ───────────            ────────────────            │
│   • Materials arrive     • Bill received        • Compare PO               │
│   • Verify qty/quality   • Enter in QBO         • Compare receiving        │
│   • Sign delivery slip   • Reference PO         • Compare bill             │
│        │                       │                      │                     │
│        └───────────────────────┴──────────────────────┘                     │
│                                │                                             │
│                                ▼                                             │
│                         ┌─────────────┐                                     │
│                         │   PAYMENT   │                                     │
│                         │  APPROVED   │                                     │
│                         └─────────────┘                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Approval Process

**For companies without formal approval workflow:**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SIMPLE APPROVAL PROCESS                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  APPROVAL THRESHOLDS (Example):                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  PO Amount              │  Who Can Approve                                  │
│  ───────────────────────┼─────────────────────────────────────────────────  │
│  $0 - $500              │  Foreman (no approval needed)                     │
│  $501 - $2,500          │  Project Manager                                  │
│  $2,501 - $10,000       │  Project Manager + Superintendent                 │
│  $10,001 - $50,000      │  Operations Manager                               │
│  $50,001+               │  Owner/Controller                                 │
│                                                                              │
│  WORKFLOW:                                                                   │
│  ─────────────────────────────────────────────────────────────────────────  │
│  1. PM creates PO in "Draft" (by saving without sending)                    │
│  2. PM requests approval via email/Slack                                    │
│  3. Approver reviews, checks budget                                         │
│  4. Approver adds name to "Approved By" field                               │
│  5. PM sends PO to vendor                                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### PO Status Tracking

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QBO PURCHASE ORDER STATUSES                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  STATUS: OPEN                                                                │
│  ─────────────                                                               │
│  • PO created and sent                                                       │
│  • Waiting for delivery                                                      │
│  • No bill linked yet                                                        │
│                                                                              │
│  STATUS: PARTIALLY RECEIVED                                                  │
│  ────────────────────────                                                    │
│  • Some items billed                                                         │
│  • Some items still on order                                                 │
│  • Split deliveries                                                          │
│                                                                              │
│  STATUS: CLOSED                                                              │
│  ─────────────                                                               │
│  • All items billed                                                          │
│  • Or manually closed                                                        │
│  • Complete                                                                  │
│                                                                              │
│  To view PO status:                                                          │
│  Navigate: Expenses → Purchase Orders                                        │
│  Filter by: Open, Closed, or All                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Receiving Against POs

### Documenting Receipt (Manual Process)

QBO doesn't have a built-in receiving function, so receiving is typically documented manually:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    RECEIVING DOCUMENTATION                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  OPTION 1: Annotated Delivery Ticket                                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Receive delivery ticket from driver                                       │
│  • Compare to PO (have copy at job site)                                    │
│  • Note any discrepancies on ticket                                         │
│  • Sign and date                                                             │
│  • Scan/photo and save with PO                                              │
│                                                                              │
│  OPTION 2: Receiving Log                                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Maintain a receiving log at each job site:                                  │
│                                                                              │
│  Date     │ PO#          │ Vendor       │ Items Received  │ Received By    │
│  ─────────┼──────────────┼──────────────┼─────────────────┼────────────────│
│  03/18/24 │ 2024-001-P01 │ ABC Lumber   │ All per PO      │ M. Johnson     │
│  03/19/24 │ 2024-001-P02 │ XYZ Supply   │ Partial (note)  │ M. Johnson     │
│                                                                              │
│  OPTION 3: QBO Memo Field                                                    │
│  ─────────────────────────────────────────────────────────────────────────  │
│  When creating bill from PO:                                                 │
│  • Add memo: "Received 03/18/24 by MJ, all items complete"                  │
│  • Or: "Received 03/18/24, short 50 studs - will ship 03/20"                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Handling Discrepancies

**Short Shipments:**

```
Scenario: Ordered 500 studs, received 450

Options:
1. PARTIAL BILL NOW
   • Create bill for 450 received
   • PO remains "Partially Received"
   • Bill for remaining 50 when delivered

2. WAIT FOR COMPLETE DELIVERY
   • Hold bill until all received
   • Update PO memo with receipt status

3. ADJUST PO
   • If vendor can't fulfill, reduce PO qty
   • Create bill for reduced amount
   • Close PO
```

**Damaged/Rejected Items:**

```
Scenario: 50 studs damaged in delivery

Steps:
1. Note on delivery ticket: "50 EA 2x4x8 rejected - damage"
2. Have driver sign acknowledgment
3. Take photos
4. Contact vendor for replacement
5. Bill only for accepted quantity
6. Track replacement on separate line or new PO
```

**Price Discrepancies:**

```
Scenario: PO says $4.25/stud, bill says $4.50/stud

Steps:
1. DO NOT pay higher price automatically
2. Contact vendor with PO reference
3. Options:
   a. Vendor corrects bill to PO price
   b. Vendor provides justification (price increase notification)
   c. Negotiate resolution
4. Document resolution in bill memo
5. Update PO if price change accepted
```

---

## Matching POs to Bills

### Creating Bills from POs

**Method 1: From the PO**

```
Step-by-Step:
1. Navigate: Expenses → Purchase Orders
2. Find the PO (status: Open)
3. Click on PO to open
4. Click: "Copy to Bill"
5. Bill auto-populates with PO details
6. Verify/adjust quantities if needed
7. Enter vendor's bill number in Ref #
8. Enter bill date and due date
9. Save
```

**Method 2: From Bill Entry**

```
Step-by-Step:
1. Navigate: + New → Bill
2. Select Vendor
3. QBO prompts: "Add to this bill from..."
4. Click: "Add" next to the PO
5. PO lines auto-populate
6. Enter vendor's bill number
7. Verify amounts
8. Save
```

### Visual: Bill from PO

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  BILL #INV-78451                                              [Save] [X]    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Vendor: ABC Lumber Supply                                                   │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │  Add to this bill from:                                             │    │
│  │  ┌──────────────────────────────────────────────────────────────┐   │    │
│  │  │ ✅ PO-2024-001-P01  $5,200.00  03/15/2024  [Add]             │   │    │
│  │  │    (Smith Residence - Framing Lumber)                        │   │    │
│  │  └──────────────────────────────────────────────────────────────┘   │    │
│  └─────────────────────────────────────────────────────────────────────┘    │
│                                                                              │
│  Bill date: 03/20/2024          Due date: 04/19/2024                        │
│  Ref #: INV-78451               Terms: Net 30                                │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │ Category Details                                                    │    │
│  ├─────────────┬──────────────────────┬──────────┬──────────┬─────────┤    │
│  │ CATEGORY    │ DESCRIPTION          │ QTY      │ RATE     │ AMOUNT  │    │
│  ├─────────────┼──────────────────────┼──────────┼──────────┼─────────┤    │
│  │ 50100       │ 2x4x8 SPF #2        │ 500 EA   │ $4.25    │ $2,125  │    │
│  │ 50100       │ 2x6x12 SPF #2       │ 200 EA   │ $8.50    │ $1,700  │    │
│  │ 50100       │ 2x10x16 SPF #2      │ 80 EA    │ $12.00   │ $960    │    │
│  │ 50100       │ Hardware            │ 1 LOT    │ $415.00  │ $415    │    │
│  ├─────────────┴──────────────────────┴──────────┴──────────┼─────────┤    │
│  │ Linked to PO: PO-2024-001-P01                    TOTAL: │ $5,200  │    │
│  └──────────────────────────────────────────────────────────┴─────────┘    │
│                                                                              │
│  Customer: Smith Family Trust                                                │
│  Class: 2024-001 Smith Residence                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Partial Billing

When you receive partial shipments:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PARTIAL BILLING WORKFLOW                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PO-2024-001-P01: 500 studs @ $4.25 = $2,125                                │
│                                                                              │
│  DELIVERY 1 (03/18): 350 studs received                                      │
│  ───────────────────────────────────────────────────────────────────────    │
│  1. Open PO → Copy to Bill                                                   │
│  2. Change qty from 500 to 350                                               │
│  3. Amount auto-calculates: $1,487.50                                        │
│  4. Save bill                                                                │
│  5. PO status: "Partially Received" (150 remaining)                          │
│                                                                              │
│  DELIVERY 2 (03/25): 150 studs received                                      │
│  ───────────────────────────────────────────────────────────────────────    │
│  1. Open same PO (shows remaining qty)                                       │
│  2. Copy to Bill                                                             │
│  3. Qty shows: 150 (remaining)                                               │
│  4. Amount: $637.50                                                          │
│  5. Save bill                                                                │
│  6. PO status: "Closed"                                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Three-Way Matching

### What Is Three-Way Matching?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    THREE-WAY MATCHING                                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Three-way matching compares three documents before payment:                 │
│                                                                              │
│      ┌───────────────┐                                                       │
│      │ 1. PURCHASE   │  What we ordered                                     │
│      │    ORDER      │  (Qty, price, job)                                   │
│      └───────┬───────┘                                                       │
│              │                                                               │
│              ▼                                                               │
│      ┌───────────────┐                                                       │
│      │ 2. RECEIVING  │  What we actually got                                │
│      │    DOCUMENT   │  (Qty received, condition)                           │
│      └───────┬───────┘                                                       │
│              │                                                               │
│              ▼                                                               │
│      ┌───────────────┐                                                       │
│      │ 3. VENDOR     │  What vendor is charging                             │
│      │    INVOICE    │  (Qty, price, total)                                 │
│      └───────────────┘                                                       │
│                                                                              │
│  ALL THREE MUST MATCH before payment is approved.                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Why Three-Way Matching Matters

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BENEFITS OF THREE-WAY MATCHING                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PREVENTS PAYMENT FOR:                                                       │
│  ✅ Items never received                                                     │
│  ✅ Wrong quantities                                                         │
│  ✅ Unauthorized price increases                                             │
│  ✅ Duplicate invoices                                                       │
│  ✅ Fraudulent invoices                                                      │
│                                                                              │
│  REAL-WORLD SCENARIOS:                                                       │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Scenario 1: "Phantom Invoice"                                               │
│  • Scammer sends fake invoice that looks legitimate                          │
│  • Without PO matching, it might get paid                                   │
│  • With matching: No PO = No payment                                        │
│                                                                              │
│  Scenario 2: "Short Ship, Full Bill"                                         │
│  • Vendor ships 400 units, bills for 500                                    │
│  • Receiving shows 400                                                       │
│  • Bill for 500 doesn't match receiving                                     │
│  • Discrepancy caught before payment                                        │
│                                                                              │
│  Scenario 3: "Price Creep"                                                   │
│  • Quote/PO says $10/unit                                                   │
│  • Bill comes at $12/unit                                                   │
│  • Matching catches the discrepancy                                          │
│  • Negotiate or verify before paying                                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Implementing Three-Way Match in QBO

QBO links POs to bills automatically, but the "receiving" step is manual:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    THREE-WAY MATCH WORKFLOW IN QBO                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  STEP 1: PURCHASE ORDER                                                      │
│  ─────────────────────                                                       │
│  • Created in QBO                                                            │
│  • Documents: qty, price, job                                               │
│  • Sent to vendor                                                            │
│                                                                              │
│  STEP 2: RECEIVING (Manual)                                                  │
│  ─────────────────────────                                                   │
│  • Materials arrive at job site                                              │
│  • Compare to PO (print copy for site)                                      │
│  • Document receipt (signed delivery ticket, receiving log)                 │
│  • Note any discrepancies                                                   │
│  • Scan/photo and attach to PO in QBO                                       │
│    - Open PO → Attachments → Upload                                         │
│                                                                              │
│  STEP 3: BILL ENTRY AND MATCHING                                             │
│  ───────────────────────────────                                             │
│  • Vendor bill arrives                                                       │
│  • Enter bill from PO (links automatically)                                 │
│  • Compare bill to PO:                                                       │
│    ☑️ Quantities match?                                                     │
│    ☑️ Prices match?                                                         │
│    ☑️ Total matches?                                                        │
│  • Compare bill to receiving:                                                │
│    ☑️ Did we receive these items?                                           │
│    ☑️ Qty on bill ≤ qty received?                                           │
│  • If all match: Approve for payment                                        │
│  • If discrepancy: Investigate before paying                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Match Verification Checklist

Use this checklist before approving bills for payment:

```
THREE-WAY MATCH VERIFICATION

Bill #: ________________  Vendor: ____________________  Amount: $________

PO VERIFICATION:
☐ Bill is linked to valid PO
☐ PO was approved by authorized person
☐ Bill prices match PO prices
☐ Bill quantities ≤ PO quantities
☐ Job/Class assignment correct

RECEIVING VERIFICATION:
☐ Receiving document on file (delivery ticket, photo)
☐ Items were actually received
☐ Quantities received match bill quantities
☐ No quality/damage issues noted
☐ Receiving date reasonable vs. bill date

DISCREPANCY CHECK:
☐ No price discrepancies OR discrepancy documented and approved
☐ No quantity discrepancies OR discrepancy documented
☐ Bill number not duplicate of prior payment

APPROVAL:
Verified by: ___________________ Date: ___________
Approved for payment: ☐ Yes  ☐ No (reason: _____________)
```

---

## PO Templates and Best Practices

### Sample PO Template

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│  [YOUR COMPANY LOGO]                                                         │
│                                                                              │
│  ABC CONSTRUCTION, LLC                           PURCHASE ORDER             │
│  123 Builder Street                              ─────────────────          │
│  Anytown, ST 12345                               PO #: 2024-001-P01         │
│  (555) 123-4567                                  Date: March 15, 2024       │
│  License #: CONT-12345                                                       │
│                                                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  VENDOR:                        SHIP TO:                                     │
│  ABC Lumber Supply              Smith Residence                              │
│  456 Supply Road                456 Construction Lane                        │
│  Anytown, ST 12346              Anytown, ST 12345                            │
│                                                                              │
│  JOB #: 2024-001               APPROVED BY: John Smith, PM                  │
│                                                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Item    Description              Qty    Unit    Rate      Amount           │
│  ────    ───────────              ───    ────    ────      ──────           │
│  1       2x4x8 SPF #2 Studs      500    EA      $4.25     $2,125.00        │
│  2       2x6x12 SPF #2           200    EA      $8.50     $1,700.00        │
│  3       2x10x16 SPF #2 Joists   80     EA      $12.00    $960.00          │
│  4       Hardware & Fasteners     1     LOT     $415.00   $415.00          │
│                                                                              │
│                                          SUBTOTAL:        $5,200.00         │
│                                          TAX:             $0.00             │
│                                          TOTAL:           $5,200.00         │
│                                                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  SPECIAL INSTRUCTIONS:                                                       │
│  • Deliver to job site address above                                        │
│  • Call PM John Smith at (555) 987-6543 with delivery ETA                   │
│  • Delivery Mon-Fri, 7am-3pm only                                           │
│  • Reference this PO number on all invoices                                 │
│                                                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TERMS AND CONDITIONS:                                                       │
│  1. This order is subject to our standard purchase terms (attached)         │
│  2. Price quoted is firm for 30 days from PO date                          │
│  3. No substitutions without prior written approval                         │
│  4. All materials must meet specifications provided                         │
│  5. Insurance certificates must be current on file                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Best Practices

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PURCHASE ORDER BEST PRACTICES                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. CREATE PO BEFORE ORDERING                                               │
│     • Never order without a PO                                              │
│     • Emergency orders: Create PO same day                                  │
│     • Verbal orders: Follow up with PO immediately                          │
│                                                                              │
│  2. ONE PO PER VENDOR PER JOB                                               │
│     • Don't combine multiple jobs on one PO                                 │
│     • Makes job costing cleaner                                             │
│     • Exception: Overhead purchases                                         │
│                                                                              │
│  3. BE SPECIFIC                                                              │
│     • Include detailed descriptions                                          │
│     • Specify size, grade, quantity, unit                                   │
│     • Reference quotes or bid documents                                     │
│                                                                              │
│  4. DOCUMENT DELIVERY LOCATION                                               │
│     • Job site address                                                       │
│     • Contact name and phone                                                 │
│     • Delivery instructions                                                  │
│                                                                              │
│  5. ENFORCE PO REQUIREMENT                                                   │
│     • Train vendors: "No PO, No Pay"                                        │
│     • Reject invoices without valid PO reference                            │
│     • Consistent enforcement builds discipline                               │
│                                                                              │
│  6. REVIEW OPEN POs WEEKLY                                                   │
│     • Run Open PO report                                                     │
│     • Follow up on old open orders                                          │
│     • Close POs that are complete                                           │
│                                                                              │
│  7. ATTACH DOCUMENTATION                                                     │
│     • Receiving tickets                                                      │
│     • Quotes                                                                 │
│     • Correspondence                                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Troubleshooting

### Common Issues and Solutions

**Issue: PO doesn't appear when entering bill**

```
Possible causes:
1. Wrong vendor selected on bill
   → Verify vendor matches PO vendor exactly

2. PO already closed
   → Check PO status; reopen if needed

3. PO date in closed period
   → Verify accounting periods

Solution: Manually reference PO in bill memo if can't link
```

**Issue: Can't close PO - shows open balance**

```
Possible causes:
1. Bill qty doesn't match PO qty
   → Create bill for remaining qty, or
   → Edit PO to match what was actually received

2. Multiple bills partially applied
   → Review all bills linked to this PO

Solution: Either bill the remainder or reduce PO qty
```

**Issue: Need to change PO after bill created**

```
You cannot edit a PO after it's been converted to a bill.

Options:
1. Void the bill, edit PO, recreate bill
2. Create a credit memo for the difference
3. Leave as-is and note discrepancy
```

**Issue: Vendor doesn't reference PO on invoice**

```
Prevention:
• Include message on PO: "Reference PO # on all invoices"
• Train vendors on your requirements

When it happens:
• Manually match invoice to PO
• Add PO reference to bill memo
• Follow up with vendor for future orders
```

---

## Reports

### Open Purchase Orders Report

```
Navigation: Reports → Open Purchase Orders

Shows all POs not yet fully billed

Use to:
• Monitor outstanding orders
• Follow up with vendors
• Identify stale POs to close
```

### Purchases by Vendor Detail

```
Navigation: Reports → Expenses and Vendors → Purchases by Vendor Detail

Customize:
• Filter by date range
• Group by vendor
• Shows PO numbers with bills

Use to:
• Verify POs were billed
• Review vendor spending
• Audit PO to bill matching
```

---

## Next Steps

With PO processes established:
- [Recording Transactions](../basics/03-recording-transactions.md) - Complete expense workflows
- [Vendor Setup & AP](../basics/04-vendor-setup-ap.md) - Vendor management
- [Month-End Close](../checklists/11-month-end-close.md) - Include PO review

---

*[Back to Main Guide](../../README.md)*
