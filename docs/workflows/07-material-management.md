# Material Management for Construction

## Overview

Materials typically represent 30-50% of construction costs. Proper material management—tracking purchases, deliveries, storage, and job allocation—is essential for job costing accuracy and profitability.

This guide covers material tracking in QuickBooks Online for construction companies.

---

## Material Cost Categories

### Types of Materials

```
MATERIAL CATEGORIES FOR CONSTRUCTION

┌─────────────────────────────────────────────────────────────────────────────────┐
│                                                                                  │
│  DIRECT MATERIALS (Job-Specific)                                                 │
│  ├── Installed Materials - Permanently incorporated into the work               │
│  │   • Lumber, concrete, steel, drywall, etc.                                   │
│  │   • Fixtures, equipment, finishes                                            │
│  │                                                                               │
│  ├── Stored Materials - Purchased for job, not yet installed                    │
│  │   • On-site storage                                                          │
│  │   • Off-site/fabrication shop                                                │
│  │                                                                               │
│  └── Consumables - Used on job but not incorporated                             │
│      • Fasteners, adhesives, caulk                                              │
│      • Blades, bits, sandpaper                                                  │
│      • Temporary protection materials                                            │
│                                                                                  │
│  INDIRECT MATERIALS (Overhead)                                                   │
│  ├── Office Supplies                                                            │
│  ├── Safety Equipment (general stock)                                           │
│  ├── Small Tools (under capitalization threshold)                               │
│  └── Shop/Yard Supplies                                                         │
│                                                                                  │
│  INVENTORY MATERIALS (If you stock materials)                                    │
│  ├── Common materials kept in stock                                             │
│  ├── Bulk purchases for multiple jobs                                           │
│  └── Requires inventory tracking                                                │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## Material Tracking Options in QBO

### Option 1: Direct Job Costing (Most Common)

**How It Works:**
- Purchase materials → code directly to job
- No inventory tracking
- Simple and straightforward

**Best For:**
- Project-specific material purchases
- Custom/one-time orders
- Most residential and commercial GCs

**QBO Setup:**
```
When purchasing materials for Job A:

Bill Entry:
  Vendor: ABC Lumber Supply
  Account: 51200 Materials - Lumber
  Amount: $5,000
  Customer: Job A - Smith Residence
  Memo: Framing lumber per PO-2024-045

Result: Cost immediately hits Job A
```

### Option 2: Inventory Tracking

**How It Works:**
- Purchase materials → add to inventory
- Transfer from inventory to job when used
- Track quantity on hand

**Best For:**
- Contractors who stock common materials
- Fabrication shops
- Service contractors with truck stock

**QBO Inventory Setup:**

1. **Enable Inventory:**
   - Settings → Account and Settings → Sales
   - Turn on "Track inventory quantity on hand"

2. **Create Inventory Items:**
   ```
   Product/Service: 1/2" Copper Pipe - 10ft
   Type: Inventory
   Initial Qty: 50
   Reorder Point: 20
   Cost: $12.00
   Sales Price: $18.00 (if you sell materials)
   Asset Account: 13000 Inventory
   COGS Account: 51300 Materials - Plumbing
   ```

3. **Issue to Jobs:**
   - Create Invoice or Sales Receipt to internal customer
   - Or use Inventory Adjustment

### Option 3: Stored Materials (WIP)

**How It Works:**
- Purchase materials → track as asset
- Bill owner for stored materials
- Transfer to COGS when installed

**Best For:**
- Large commercial projects
- Long-lead items (windows, equipment)
- AIA billing with stored materials

**QBO Setup:**
```
When materials arrive but aren't installed:

Purchase Entry:
  Debit: 13100 Stored Materials - Job A    $25,000
  Credit: Accounts Payable                         $25,000

When installed:
  Debit: 51200 Materials - Windows (Job A) $25,000
  Credit: 13100 Stored Materials - Job A           $25,000
```

---

## Chart of Accounts for Materials

### Recommended Structure

```
MATERIAL ACCOUNTS

ASSETS
13000 Inventory (if using inventory)
├── 13100 Inventory - Lumber
├── 13200 Inventory - Plumbing
├── 13300 Inventory - Electrical
└── 13400 Inventory - General

13500 Stored Materials (for WIP tracking)
├── 13510 Stored Materials - Job A
├── 13520 Stored Materials - Job B
└── 13530 Stored Materials - Job C

COST OF GOODS SOLD
51000 Materials
├── 51100 Materials - Lumber & Framing
├── 51200 Materials - Concrete
├── 51300 Materials - Plumbing
├── 51400 Materials - Electrical
├── 51500 Materials - HVAC
├── 51600 Materials - Roofing
├── 51700 Materials - Drywall & Paint
├── 51800 Materials - Flooring
├── 51900 Materials - Fixtures & Hardware
└── 51950 Materials - Other

52000 Consumables & Small Tools
├── 52100 Fasteners & Adhesives
├── 52200 Blades, Bits & Abrasives
├── 52300 Safety Supplies
└── 52400 Other Consumables
```

---

## Purchase Order Integration

### Using POs for Material Control

**Benefits of POs:**
1. Prevents unauthorized purchases
2. Enables three-way matching
3. Tracks committed costs
4. Helps with budgeting

**QBO PO Workflow:**

```
MATERIAL PURCHASE WORKFLOW

Step 1: Create Purchase Order
├── Specify vendor, items, quantities
├── Assign to job/project
├── Get approval (if required)
└── Send to vendor

Step 2: Receive Materials
├── Verify delivery matches PO
├── Note any variances
├── Sign delivery ticket
└── Store or install materials

Step 3: Receive Bill
├── Match bill to PO
├── Convert PO to Bill in QBO
├── Verify pricing matches
└── Code to correct job

Step 4: Three-Way Match
├── PO = What you ordered
├── Receiving = What you got
├── Bill = What they're charging
└── All three should match
```

---

## Handling Material Issues

### Returns and Credits

**When You Return Materials:**

```
QBO Entry - Vendor Credit:

Vendor Credit from: ABC Lumber Supply
Date: [Return date]
Account: 51100 Materials - Lumber
Amount: $500
Customer: Job A - Smith Residence
Memo: Returned excess 2x4s, RA#12345
```

**Apply Credit to Future Bill:**
- When paying next bill, apply the credit
- Or request refund check

### Defective Materials

**Discovery Before Installation:**
1. Return to vendor
2. Record vendor credit
3. Reorder correct materials

**Discovery After Installation:**
1. Document the issue
2. Determine responsibility (vendor, manufacturer, installer)
3. File warranty claim if applicable
4. Back-charge if appropriate

### Material Theft or Loss

**When Materials Are Stolen:**
```
Journal Entry:

Debit: 67000 Theft & Casualty Loss     $5,000
Credit: 51100 Materials - Lumber               $5,000

Memo: Lumber stolen from Job A site, police report #12345
```

**File Insurance Claim:**
- Document loss thoroughly
- Provide police report
- Record insurance recovery when received

---

## Material Allocation Methods

### Job-Specific Purchases

**Best Practice:** Purchase specifically for each job when possible.

**Benefits:**
- Clear job cost tracking
- No allocation needed
- Accurate profitability

### Bulk Purchase Allocation

**When You Buy in Bulk:**

```
BULK MATERIAL ALLOCATION EXAMPLE

Purchase: 100 sheets drywall @ $15 = $1,500

Usage:
  Job A: 40 sheets (40%)
  Job B: 35 sheets (35%)
  Job C: 25 sheets (25%)

Allocation Entry:
  Debit: 51700 Materials - Drywall (Job A)    $600
  Debit: 51700 Materials - Drywall (Job B)    $525
  Debit: 51700 Materials - Drywall (Job C)    $375
  Credit: 13100 Inventory - Drywall                   $1,500
```

### Consumables Allocation

**Options for Job-Charging Consumables:**

1. **Per-Job Tracking** (Most Accurate)
   - Track consumables by job
   - Time-consuming but accurate

2. **Percentage of Labor** (Common)
   - Consumables = X% of labor cost
   - Estimate based on historical data

3. **Flat Rate per Job** (Simple)
   - Include standard consumable allowance
   - Adjust for job type/size

---

## Material Cost Tracking Reports

### QBO Reports for Materials

**1. Purchases by Vendor Summary**
- Shows total spent with each supplier
- Helps negotiate volume discounts

**2. Transaction Detail by Account (Material Accounts)**
- All material purchases by account
- Filter by customer for job-specific view

**3. Profit & Loss by Customer**
- Materials cost per job
- Compare to budget

**4. Purchase Order List**
- Open POs (committed costs)
- Completed POs

### Custom Material Reports

**Material Cost by Job Report:**

```
MATERIAL COST BY PROJECT
Period: Year to Date

Job                      Budget      Actual      Variance    % of Budget
───────────────────────────────────────────────────────────────────────────
Smith Residence         $85,000     $82,500      $2,500        97.1%
Jones Office Build     $140,000    $148,200     ($8,200)      105.9% ⚠️
ABC Retail TI           $45,000     $41,800      $3,200        92.9%
───────────────────────────────────────────────────────────────────────────
TOTAL                  $270,000    $272,500     ($2,500)      100.9%

⚠️ Jones Office Build over budget - investigate
```

---

## Material Management Best Practices

### Purchasing Best Practices

| Practice | Benefit |
|----------|---------|
| **Get multiple quotes** | Best pricing |
| **Use POs always** | Control and tracking |
| **Verify before ordering** | Prevent over-ordering |
| **Schedule deliveries** | Reduce storage needs |
| **Inspect on receipt** | Catch issues early |
| **Keep delivery tickets** | Proof of receipt |

### Storage Best Practices

| Practice | Benefit |
|----------|---------|
| **Secure storage** | Prevent theft |
| **Weather protection** | Prevent damage |
| **Organize by job** | Easy identification |
| **FIFO rotation** | Use older stock first |
| **Regular counts** | Catch shrinkage |

### Cost Control Best Practices

| Practice | Benefit |
|----------|---------|
| **Compare to estimate** | Catch overruns early |
| **Track waste** | Identify inefficiency |
| **Return unused** | Recover cost |
| **Negotiate terms** | Improve cash flow |
| **Volume discounts** | Reduce costs |

---

## Material Waste and Scrap

### Tracking Material Waste

**Normal Waste (Built into Estimates):**
- Cutting waste
- Normal breakage
- Standard overages
- Included in job cost

**Abnormal Waste (Investigate):**
- Excessive cuts
- Damaged materials
- Theft
- Should be tracked separately

```
WASTE FACTOR BY MATERIAL TYPE

Material              Normal Waste    Abnormal If >
─────────────────────────────────────────────────────
Lumber (framing)           5-8%           12%
Drywall                    8-10%          15%
Roofing shingles          5-10%          15%
Flooring (wood)           5-8%           12%
Tile/Stone               10-15%          20%
Concrete                  3-5%            8%
Electrical wire          3-5%            8%
Plumbing pipe            5-8%           12%
```

### Recording Scrap Value

**If Materials Have Scrap Value:**
```
Journal Entry:

Debit: 1000 Cash (or Receivable)       $200
Credit: 51950 Materials - Other                 $200

Memo: Scrap metal sold from Job A
```

---

## Integration with Estimating

### Estimate to Actual Comparison

**Track These Metrics:**

```
MATERIAL COST ANALYSIS - JOB A

Category              Estimated    Actual      Variance    Notes
────────────────────────────────────────────────────────────────────
Lumber                 $25,000    $26,200     ($1,200)    Price increase
Concrete               $12,000    $11,500        $500     Less waste
Roofing                 $8,500     $8,800       ($300)    Extra flashing
Fixtures               $15,000    $14,200        $800     Negotiated price
Other                   $5,000     $5,500       ($500)    Added items
────────────────────────────────────────────────────────────────────
TOTAL MATERIALS        $65,500    $66,200       ($700)    1.1% over
```

### Feedback Loop for Estimating

**Use Actual Data to Improve Estimates:**

1. Track actual quantities used
2. Compare to estimated quantities
3. Update unit costs in estimating database
4. Adjust waste factors
5. Review pricing with suppliers

---

## Key Takeaways

1. **Code to jobs immediately** - Don't let materials float in unassigned accounts
2. **Use purchase orders** - Control spending and track commitments
3. **Match PO to bill** - Verify pricing and quantities
4. **Track stored materials** - Important for WIP and AIA billing
5. **Monitor waste** - Abnormal waste kills margins
6. **Return unused materials** - Recover what you can
7. **Compare to estimates** - Learn and improve

---

## Next Steps

- For purchase orders → [Purchase Orders & Three-Way Matching](./01-purchase-orders.md)
- For job costing → [Job Costing Setup](../tutorials/03-job-costing-setup.md)
- For WIP tracking → [WIP Schedules](../tutorials/04-wip-schedules.md)
- For budget tracking → [Budget vs. Actual Reporting](../tutorials/11-budget-vs-actual.md)

---

*[← Previous: Insurance Tracking](./06-insurance-tracking.md) | [Next: Electronic Documents →](./08-electronic-documents.md)*
