# Equipment Allocation in QuickBooks Online

## Overview

Construction companies use significant equipment—from small tools to heavy machinery. Properly allocating equipment costs to jobs is essential for:
- Accurate job costing
- Informed rent vs. own decisions
- Equipment replacement planning
- Full cost recovery on projects

This chapter covers equipment tracking strategies and implementation in QBO.

---

## The Equipment Cost Problem

### Why Equipment Gets Ignored in Job Costing

```
TYPICAL SCENARIO (WRONG):
Job A uses your excavator for 2 weeks
Job B uses your excavator for 1 week

Income Statement Shows:
  Equipment Depreciation: $5,000/month (overhead)
  Job A Direct Costs: $0 equipment
  Job B Direct Costs: $0 equipment

Result: Jobs look more profitable than they are
        Equipment appears to be "free"
```

```
CORRECT APPROACH:
Job A: Charged $3,333 for equipment (2 weeks)
Job B: Charged $1,667 for equipment (1 week)

Income Statement Shows:
  Job A Direct Costs: $3,333 equipment
  Job B Direct Costs: $1,667 equipment
  Equipment overhead: Offset by charges to jobs

Result: True job profitability visible
        Equipment cost recovery tracked
```

### The Hidden Cost of Equipment

| Cost Category | Example Costs | Often Forgotten? |
|--------------|---------------|------------------|
| Depreciation | Purchase price over useful life | Yes - "It's paid for" |
| Insurance | Annual premium | Sometimes |
| Maintenance | Oil, filters, repairs | No - visible expense |
| Fuel | Diesel, gasoline | No - visible expense |
| Storage | Shop space allocation | Yes |
| Licensing | Registration, permits | Sometimes |
| Interest | Financing costs | Yes - "It's overhead" |

**WHY Full Cost Matters**: If you don't charge jobs for equipment, you:
1. Understate job costs (false profitability)
2. Can't compare rent vs. own economics
3. Have no data for equipment replacement decisions
4. Leave money on the table when billing T&M work

---

## Calculating Internal Equipment Rates

### The Goal: Full Cost Recovery

Your internal equipment rate should recover all costs of owning and operating equipment.

### Rate Calculation Formula

```
Annual Equipment Cost = Depreciation + Insurance + Maintenance + Storage + Licensing + Interest

Hourly Rate = Annual Equipment Cost ÷ Estimated Annual Hours of Use

Daily Rate = Hourly Rate × 8 hours
Weekly Rate = Daily Rate × 5 days
Monthly Rate = Weekly Rate × 4.33 weeks
```

### Example: Calculating Excavator Rate

```
ASSET: CAT 320 Excavator
Purchase Price: $180,000
Useful Life: 6 years (10,000 hours)
Salvage Value: $30,000

ANNUAL COSTS:
Depreciation:     ($180,000 - $30,000) ÷ 6 years = $25,000/year
Insurance:        $3,000/year
Estimated Maint.: $8,000/year
Storage (shared): $2,400/year
Licensing:        $600/year
Financing (avg):  $4,000/year
─────────────────────────────────────────────────────────────────
TOTAL ANNUAL COST:                                 $43,000/year

RATE CALCULATIONS:
Estimated annual use: 1,500 hours
Hourly Rate: $43,000 ÷ 1,500 = $28.67/hour

Alternate Rates:
Daily (8 hours):  $28.67 × 8 = $230/day
Weekly (5 days):  $230 × 5 = $1,150/week
Monthly:          $1,150 × 4.33 = $4,980/month
```

### Rate Comparison: Own vs. Rent

```
EXCAVATOR ANALYSIS:
Your Internal Rate: $230/day
Rental Company Rate: $450/day

Break-Even Analysis:
If you use the excavator 95+ days/year, ownership is cheaper.
Actual use last year: 180 days
Decision: Ownership is correct.

AT T&M BILLING:
Internal cost: $230/day
Bill customer: $450/day (market rate)
Equipment profit: $220/day
```

---

## Setting Up Equipment in QBO

### Option 1: Equipment as Fixed Assets with Internal Billing

**Step 1: Create Fixed Asset Accounts**

1. Go to **Settings ⚙️** → **Chart of Accounts**
2. Create accounts:

| Account # | Name | Type | Detail Type |
|-----------|------|------|-------------|
| 15000 | Equipment & Vehicles | Fixed Assets | Machinery & Equipment |
| 15100 | ↳ Excavators | Fixed Assets | Machinery & Equipment |
| 15200 | ↳ Loaders | Fixed Assets | Machinery & Equipment |
| 15300 | ↳ Trucks | Fixed Assets | Machinery & Equipment |
| 15400 | ↳ Small Equipment | Fixed Assets | Machinery & Equipment |
| 15500 | ↳ Tools | Fixed Assets | Machinery & Equipment |
| 15900 | Accumulated Depreciation - Equip | Fixed Assets | Accumulated Depreciation |

**Step 2: Create Equipment Cost Accounts**

| Account # | Name | Type | Detail Type |
|-----------|------|------|-------------|
| 50400 | Equipment Costs - Direct | COGS | Equipment Rental-COS |
| 50410 | ↳ Equipment - Owned | COGS | Equipment Rental-COS |
| 50420 | ↳ Equipment - Rental | COGS | Equipment Rental-COS |
| 50430 | ↳ Equipment - Fuel | COGS | Equipment Rental-COS |
| 50440 | ↳ Small Tools | COGS | Supplies & Materials-COGS |
| 60400 | Equipment Expenses - Overhead | Expense | Equipment Rental |
| 60410 | ↳ Equipment Maintenance | Expense | Repairs & Maintenance |
| 60420 | ↳ Equipment Insurance | Expense | Insurance |
| 60430 | ↳ Equipment Depreciation | Expense | Depreciation |

**Step 3: Create Internal Equipment "Vendor"**

1. Go to **Expenses** → **Vendors** → **New vendor**
2. Name: "Internal Equipment Charges"
3. This is a placeholder vendor for equipment allocations

**Step 4: Create Equipment Products/Services**

1. Go to **Settings ⚙️** → **Products and Services**
2. Create for each major equipment item:

| Name | Type | Income Account | Expense Account |
|------|------|----------------|-----------------|
| Equipment - Excavator | Service | 40400 Equipment Income | 50410 Equipment-Owned |
| Equipment - Loader | Service | 40400 Equipment Income | 50410 Equipment-Owned |
| Equipment - Skid Steer | Service | 40400 Equipment Income | 50410 Equipment-Owned |
| Equipment Rental Expense | Service | N/A | 50420 Equipment-Rental |

### Option 2: Equipment as Inventory (For Equipment-Heavy Operations)

For companies that manage large equipment fleets, consider:
- Dedicated equipment management software
- Integration with QBO for financials
- Examples: EquipmentShare, HCSS Equipment

This is beyond standard QBO capabilities but worth considering for $1M+ equipment fleets.

---

## Recording Equipment Usage by Job

### Method 1: Monthly Journal Entry (Simplest)

At month-end, allocate equipment costs to jobs based on usage logs.

**HOW:**

**Step 1: Track Equipment Usage**
Maintain a simple log (spreadsheet or app):

```
EQUIPMENT USAGE LOG - January 2024

Equipment     | Job A  | Job B  | Job C  | Shop/Idle | Total
──────────────┼────────┼────────┼────────┼───────────┼──────
Excavator     | 10 days| 8 days | 0 days | 2 days    | 20 days
Loader        | 5 days | 10 days| 5 days | 0 days    | 20 days
Skid Steer    | 15 days| 0 days | 5 days | 0 days    | 20 days
```

**Step 2: Calculate Allocations**

```
EXCAVATOR: $230/day × 20 days = $4,600 total
  Job A: $230 × 10 = $2,300
  Job B: $230 × 8 = $1,840
  Shop/Idle: $230 × 2 = $460 (stays in overhead)

LOADER: $180/day × 20 days = $3,600 total
  Job A: $180 × 5 = $900
  Job B: $180 × 10 = $1,800
  Job C: $180 × 5 = $900

SKID STEER: $150/day × 20 days = $3,000 total
  Job A: $150 × 15 = $2,250
  Job C: $150 × 5 = $750
```

**Step 3: Create Journal Entry in QBO**

```
Date: January 31, 2024
Memo: Equipment allocations per usage log

Account                           Debit      Credit    Customer
───────────────────────────────────────────────────────────────────────────
50410 Equipment - Owned          $2,300                Job A
50410 Equipment - Owned          $1,840                Job B
50410 Equipment - Owned            $900                Job A
50410 Equipment - Owned          $1,800                Job B
50410 Equipment - Owned            $900                Job C
50410 Equipment - Owned          $2,250                Job A
50410 Equipment - Owned            $750                Job C
60430 Equipment Depreciation       $460                (Shop/Idle)
  60430 Equipment Depreciation               $11,200
───────────────────────────────────────────────────────────────────────────

Summary by Job:
Job A: $2,300 + $900 + $2,250 = $5,450
Job B: $1,840 + $1,800 = $3,640
Job C: $900 + $750 = $1,650
Overhead (Idle): $460
```

**WHY This Entry Works:**
- Debits go to job-level COGS (with Customer assignment)
- Credit offsets the overhead depreciation expense
- Net effect: Equipment costs moved from overhead to jobs

### Method 2: Bills from Internal Equipment Company

Create a bill from your internal equipment "vendor" for each allocation.

**HOW:**

1. Go to **+ New** → **Bill**
2. Vendor: Internal Equipment Charges
3. Bill Date: Last day of month
4. Add line items:
   - **Product/Service**: Equipment - Excavator
   - **Amount**: $2,300
   - **Customer**: Job A
5. Repeat for each job/equipment combination
6. Save

**WHY Bills Work:**
- Creates clear paper trail
- Easy to see equipment charges by job
- Appears in job cost reports naturally

**The Payment Problem:**
These bills need to be "paid" to clear AP. Create a journal entry:
```
Debit: Internal Equipment Clearing (or Equity account)
Credit: Accounts Payable (to Internal Equipment vendor)
```

### Method 3: Time Tracking for Equipment

Use QBO's time tracking to log equipment hours.

**HOW:**

1. Create an "employee" for each equipment unit: "Excavator - CAT 320"
2. Create service item: "Equipment - Excavator" with hourly rate
3. Log "time" entries for equipment usage:
   - Time: 8 hours
   - Customer: Job A
   - Service: Equipment - Excavator
4. At month-end, these hours appear in time reports by customer

**Pros**: Uses existing QBO feature, easy logging
**Cons**: Confuses equipment with labor, reporting challenges

---

## Equipment Rental Tracking

### Recording Rental Expenses

When renting equipment:

**HOW:**

1. Go to **+ New** → **Bill** (or Expense)
2. Vendor: Rental company name
3. In line items:
   - **Product/Service**: Equipment Rental Expense
   - **Amount**: Rental cost
   - **Customer**: Assign to project
4. Save

**Example:**
```
Bill from: United Rentals
Date: January 15, 2024

Item Details:
┌────────────────────────────┬───────────┬─────────────────────────────┐
│ Product/Service            │ Amount    │ Customer                    │
├────────────────────────────┼───────────┼─────────────────────────────┤
│ Equipment Rental Expense   │ $2,400.00 │ 2024-001-ABC Office Project │
└────────────────────────────┴───────────┴─────────────────────────────┘
Description: Mini excavator rental 1/8-1/15
```

### Billing Rental Equipment to Customers

For T&M contracts, you may bill equipment to customers with markup.

**HOW:**

1. On customer invoice, add line item:
   - **Product/Service**: Equipment Charge (create with income account)
   - **Amount**: Rental cost + markup
   - **Description**: Equipment rental per [vendor] invoice

**Example Markup Calculation:**
```
Rental cost:     $2,400
Markup (15%):      $360
Bill to customer: $2,760
Equipment profit:  $360
```

---

## Equipment Profitability Analysis

### Tracking Equipment Performance

**Report: Equipment Utilization**

```
EQUIPMENT UTILIZATION REPORT - Q1 2024

Equipment        │ Days Available │ Days Used │ Utilization │ Revenue │ Cost    │ Profit
─────────────────┼────────────────┼───────────┼─────────────┼─────────┼─────────┼────────
Excavator #1     │ 65             │ 52        │ 80%         │ $23,400 │ $11,960 │ $11,440
Excavator #2     │ 65             │ 38        │ 58%         │ $17,100 │ $8,740  │ $8,360
Loader #1        │ 65             │ 61        │ 94%         │ $10,980 │ $10,980 │ $0 *
Loader #2        │ 65             │ 22        │ 34%         │ $3,960  │ $3,960  │ $0 *
Skid Steer       │ 65             │ 58        │ 89%         │ $8,700  │ $8,700  │ $0 *
─────────────────┴────────────────┴───────────┴─────────────┴─────────┴─────────┴────────

* Loaders and Skid Steer charged at internal cost only (not billed to customers)

Analysis:
- Excavator #2 at 58% utilization - consider selling or increasing marketing
- Loader #1 at 94% - may need additional unit or rental backup
- Loader #2 at 34% - evaluate need for second loader
```

### When to Rent vs. Own

**Decision Framework:**

```
RENT VS. OWN ANALYSIS

Equipment: Compact Track Loader
Purchase Price: $65,000
Useful Life: 5 years
Annual Operating Costs: $12,000

OWNERSHIP COST:
Depreciation: $65,000 ÷ 5 = $13,000/year
Operating: $12,000/year
Total: $25,000/year
Daily cost (250 working days): $100/day

RENTAL COST:
Daily rate: $350/day

BREAK-EVEN:
$25,000 ÷ $350 = 71 days

DECISION:
If using > 71 days/year: OWN
If using < 71 days/year: RENT

Your projected usage: 120 days/year
Recommendation: OWN (saves $17,000/year vs. rental)
```

---

## Fuel Tracking by Job

### WHY Job-Level Fuel Tracking Matters

Fuel is a significant equipment cost that's often buried in overhead. Tracking by job reveals true costs.

### Method 1: Fuel Card with Job Codes

Many fuel card providers allow job coding at pump:
1. Driver enters job code when fueling
2. Monthly statement shows fuel by job
3. Enter as bill with multiple line items by job

### Method 2: Manual Fuel Log

```
FUEL LOG - Week of January 15, 2024

Date    │ Equipment     │ Gallons │ Price  │ Job      │ Amount
────────┼───────────────┼─────────┼────────┼──────────┼────────
1/15    │ Excavator #1  │ 50      │ $3.50  │ Job A    │ $175.00
1/16    │ Loader #1     │ 35      │ $3.45  │ Job B    │ $120.75
1/17    │ Truck #3      │ 28      │ $3.50  │ Job A    │ $98.00
...
```

### Recording Fuel in QBO

**HOW:**

1. Create Product/Service: "Fuel - Job"
2. When entering fuel expense:
   - **Product/Service**: Fuel - Job
   - **Amount**: Fuel cost
   - **Customer**: Assign to project
3. For shop/general fuel, leave Customer blank (goes to overhead)

---

## Small Tools and Consumables

### Tracking Strategies

Small tools (< $500) and consumables are typically:
- Expensed when purchased (not capitalized)
- Allocated to jobs if significant

### When to Allocate Small Tools

| Item Value | Job-Specific? | Action |
|------------|---------------|--------|
| < $100 | No | Expense to overhead |
| < $100 | Yes | Expense to job |
| $100 - $500 | No | Expense to overhead |
| $100 - $500 | Yes | Expense to job |
| > $500 | N/A | Evaluate capitalization |

### Recording Small Tools

**HOW:**
1. Use Product/Service: "Small Tools"
2. Expense account: 50440 Small Tools (COGS) if assigning to job
3. Expense account: 60450 Small Tools & Supplies if overhead

---

## Equipment Cost Recovery Verification

### Monthly Reconciliation

**Goal**: Verify equipment costs allocated to jobs equal (or approximate) actual equipment costs.

```
EQUIPMENT COST RECOVERY CHECK - January 2024

ACTUAL EQUIPMENT COSTS:
Depreciation expense:         $11,200
Insurance (allocated):         $1,500
Maintenance:                   $2,800
Fuel (direct to jobs):        $4,200
────────────────────────────────────────
Total Equipment Cost:         $19,700

COSTS ALLOCATED TO JOBS:
Per journal entries/bills:    $18,500
Overhead (idle time):          $1,200
────────────────────────────────────────
Total Allocated:              $19,700

Difference:                        $0 ✓

Job Detail:
Job A:  $5,450 equipment + $1,800 fuel = $7,250
Job B:  $3,640 equipment + $1,400 fuel = $5,040
Job C:  $1,650 equipment + $1,000 fuel = $2,650
Idle:   $1,200
────────────────────────────────────────
Total:                        $16,140 (excluding insurance, shop fuel)
```

---

## Common Equipment Tracking Mistakes

### Mistake 1: Equipment Treated as "Free"

**Problem**: No internal rates, equipment not charged to jobs
**Impact**: Jobs appear more profitable than reality
**Solution**: Establish internal rates, monthly allocation

### Mistake 2: Using Rental Rates for Owned Equipment

**Problem**: Charging market rental rates instead of actual cost
**Impact**: Distorts job profitability (may look unprofitable when profitable)
**Solution**: Calculate true ownership cost rates

### Mistake 3: Not Tracking Utilization

**Problem**: No data on how often equipment is used
**Impact**: Can't make informed rent vs. own decisions
**Solution**: Implement usage logging (manual or app-based)

### Mistake 4: Ignoring Idle Time

**Problem**: Equipment idle time not tracked or analyzed
**Impact**: Hidden cost of ownership, fleet right-sizing impossible
**Solution**: Track idle time, allocate to overhead, analyze monthly

### Mistake 5: Fuel Buried in Overhead

**Problem**: All fuel goes to general expense account
**Impact**: Job costs understated
**Solution**: Job-code fuel at purchase, allocate to jobs

---

## Equipment Tracking Checklist

### Setup:
- [ ] Equipment fixed asset accounts created
- [ ] Equipment cost accounts created (COGS for jobs, Expense for overhead)
- [ ] Internal equipment rates calculated
- [ ] Equipment products/services created
- [ ] Internal Equipment vendor created (if using bill method)
- [ ] Equipment usage log established

### Monthly:
- [ ] Equipment usage logged by job
- [ ] Allocations calculated based on usage
- [ ] Journal entry or bills created for allocations
- [ ] Rental equipment coded to jobs
- [ ] Fuel costs allocated to jobs
- [ ] Reconciliation performed

### Quarterly/Annual:
- [ ] Utilization report reviewed
- [ ] Internal rates recalculated if costs changed
- [ ] Rent vs. own analysis for major equipment
- [ ] Equipment replacement planning updated

---

## Next Steps

With equipment costs properly allocated, the final major tracking element is change orders. In [Change Order Management](./08-change-orders.md), you'll learn:
- Change order lifecycle tracking
- Approved vs. pending change orders
- Impact on contract value and billing
- Change order profitability analysis

---

*[← Previous: Retention Tracking](./06-retention-tracking.md) | [Next: Change Orders →](./08-change-orders.md)*
