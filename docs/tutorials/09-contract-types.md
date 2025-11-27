# Contract Types Deep Dive: T&M, Cost-Plus, GMP & Unit Price

## Overview

Not all construction contracts are created equal. While the core tutorials focus on fixed-price (lump sum) contracts with percentage-of-completion accounting, contractors frequently work with other contract structures that require different accounting approaches.

This guide covers the four major alternative contract types and how to handle each in QuickBooks Online.

---

## The Contract Type Spectrum

```
RISK ALLOCATION SPECTRUM

Contractor Bears More Risk                           Owner Bears More Risk
         ◄─────────────────────────────────────────────────────────►
         │                                                          │
    Fixed Price          GMP           Cost-Plus         T&M
    (Lump Sum)     (Guaranteed Max)   (Cost + Fee)   (Time & Materials)
         │                │                │              │
    Price is set    Price has cap    Price is open   Price is hourly
    Scope is fixed  Scope flexible   Scope evolving  Scope undefined
```

---

## Contract Type 1: Time & Materials (T&M)

### What Is T&M?

> **Time & Materials**: A contract where the owner pays for actual labor hours (at agreed rates) plus actual materials (at cost or with markup), with no guaranteed total price.

**Common Uses:**
- Emergency repairs
- Undefined scope work
- Small projects
- Service/maintenance work
- Change order work within larger contracts

### T&M Pricing Structure

```
T&M BILLING FORMULA

Labor Charge = Hours Worked × Billing Rate per Hour
Material Charge = Material Cost × (1 + Markup %)
Equipment Charge = Hours Used × Equipment Rate

Total T&M Invoice = Labor + Materials + Equipment + Other Direct Costs
```

**Example T&M Rate Sheet:**

| Labor Category | Billing Rate | Includes |
|----------------|--------------|----------|
| Journeyman Carpenter | $85/hour | Labor, burden, overhead, profit |
| Apprentice Carpenter | $55/hour | Labor, burden, overhead, profit |
| Foreman | $95/hour | Labor, burden, overhead, profit |
| Superintendent | $125/hour | Labor, burden, overhead, profit |
| Laborer | $45/hour | Labor, burden, overhead, profit |

| Material Markup | Percentage |
|-----------------|------------|
| Standard materials | Cost + 15% |
| Specialty/custom | Cost + 20% |
| Owner-furnished | No markup |

### Setting Up T&M in QBO

#### Step 1: Create T&M Products/Services

**HOW:**

Go to **Settings ⚙️** → **Products and Services** → **New**

Create Service items for each labor category:

| Name | Type | Rate | Income Account | Description |
|------|------|------|----------------|-------------|
| T&M Labor - Journeyman | Service | $85.00 | 41000 T&M Revenue - Labor | Journeyman carpenter - T&M rate |
| T&M Labor - Apprentice | Service | $55.00 | 41000 T&M Revenue - Labor | Apprentice - T&M rate |
| T&M Labor - Foreman | Service | $95.00 | 41000 T&M Revenue - Labor | Foreman - T&M rate |
| T&M Materials | Service | 0.00 | 41100 T&M Revenue - Materials | Materials at cost + markup |
| T&M Equipment | Service | 0.00 | 41200 T&M Revenue - Equipment | Equipment charges |

#### Step 2: Create T&M Revenue Accounts

**Chart of Accounts Setup:**

| Account # | Name | Type | Detail Type |
|-----------|------|------|-------------|
| 41000 | T&M Revenue - Labor | Income | Service/Fee Income |
| 41100 | T&M Revenue - Materials | Income | Service/Fee Income |
| 41200 | T&M Revenue - Equipment | Income | Service/Fee Income |
| 41300 | T&M Revenue - Other | Income | Service/Fee Income |

#### Step 3: Track T&M Time

**HOW to Enter T&M Time:**

1. Go to **+ New** → **Single Time Activity** (or use Time Tracking)
2. Select **Customer/Project**: [T&M Job Name]
3. Select **Service**: T&M Labor - [Category]
4. Enter **Hours**
5. Check **Billable** ✓
6. Add **Description**: Work performed

**Best Practice:** Require daily time sheets with:
- Employee name
- Date
- Hours (start/end time)
- Description of work
- Materials used
- Customer signature (if required by contract)

#### Step 4: Create T&M Invoices

**HOW:**

1. Go to **+ New** → **Invoice**
2. Select **Customer/Project**
3. Click **Add all billable time and expenses**
4. Review line items:
   - Labor hours by category
   - Materials with markup applied
   - Equipment charges
5. Attach supporting documentation:
   - Signed time sheets
   - Material receipts
   - Equipment logs
6. Save and send

### T&M Revenue Recognition

**WHY T&M Is Different:**

Unlike fixed-price contracts, T&M has no "earned revenue" calculation because:
- There's no contract price to measure against
- Revenue = What you bill
- No over/under billing concept

**GAAP Treatment:**
- Revenue recognized when services performed
- No WIP adjustment needed
- Bill frequently (weekly recommended)

### T&M Profitability Tracking

**The Challenge:** T&M looks profitable on the surface but actual margins vary.

**HOW to Track True T&M Profit:**

Create a T&M Profitability Report:

```
T&M JOB PROFITABILITY ANALYSIS

Job: Emergency Repair - ABC Corp
Period: November 2024

REVENUE
  Labor Billed (40 hrs × $85)           $3,400.00
  Materials Billed ($2,000 + 15%)       $2,300.00
  Equipment Billed                        $400.00
  ─────────────────────────────────────────────────
  Total Revenue                         $6,100.00

ACTUAL COSTS
  Labor Cost (40 hrs × $35 actual)      $1,400.00
  Payroll Burden (30%)                    $420.00
  Materials Cost                        $2,000.00
  Equipment Cost                          $200.00
  ─────────────────────────────────────────────────
  Total Direct Cost                     $4,020.00

GROSS PROFIT                            $2,080.00
GROSS MARGIN                              34.1%
```

### T&M Not-to-Exceed (NTE) Contracts

**What Is NTE?**

A T&M contract with a maximum price cap. You bill T&M until hitting the cap.

**QBO Tracking:**
1. Create the job with budget = NTE amount
2. Track T&M billings against the cap
3. Alert when approaching 80% of cap
4. Stop billing at cap (remaining work is at your risk)

---

## Contract Type 2: Cost-Plus (Cost Reimbursable)

### What Is Cost-Plus?

> **Cost-Plus**: A contract where the owner pays all allowable project costs plus a fee (either fixed or percentage) for contractor overhead and profit.

**Common Uses:**
- Fast-track projects (design not complete)
- Owner wants cost transparency
- Complex projects with uncertain scope
- Trusted contractor relationships

### Cost-Plus Fee Structures

#### Option A: Cost Plus Fixed Fee (CPFF)

```
Owner Pays = All Allowable Costs + Fixed Fee Amount

Example:
  Estimated Costs: $500,000
  Fixed Fee: $75,000 (15% of estimate)

  If Actual Costs = $480,000
  Owner Pays = $480,000 + $75,000 = $555,000

  If Actual Costs = $550,000
  Owner Pays = $550,000 + $75,000 = $625,000
```

**Contractor Impact:** Fee is fixed regardless of final cost. Incentive to control costs (same profit whether costs are high or low).

#### Option B: Cost Plus Percentage Fee (CPPF)

```
Owner Pays = All Allowable Costs + (Costs × Fee %)

Example:
  Fee Percentage: 15%

  If Actual Costs = $480,000
  Owner Pays = $480,000 + ($480,000 × 15%) = $552,000

  If Actual Costs = $550,000
  Owner Pays = $550,000 + ($550,000 × 15%) = $632,500
```

**Contractor Impact:** Fee increases with costs. Less incentive to control costs (more spending = more fee). Owners often avoid this structure.

### Allowable vs. Non-Allowable Costs

**Critical Concept:** Not all costs are reimbursable in cost-plus contracts.

**Typically Allowable:**
- Direct labor (field workers on the project)
- Materials incorporated into the work
- Subcontractor costs
- Equipment rental for the project
- Permits and fees
- Project-specific insurance
- Travel and subsistence (if in contract)

**Typically NOT Allowable:**
- Home office overhead
- Owner/executive salaries (unless on-site)
- Marketing and business development
- Interest expense
- Fines and penalties
- Rework due to contractor error
- Entertainment

**WHERE to Find This:** The contract's "Allowable Costs" or "Reimbursable Expenses" section defines what qualifies.

### Setting Up Cost-Plus in QBO

#### Step 1: Create Detailed Job Cost Tracking

**WHY:** You must prove every dollar you're billing is allowable and actually incurred.

**Chart of Accounts - Cost-Plus Projects:**

| Account # | Name | Type | Purpose |
|-----------|------|------|---------|
| 50100 | Direct Labor - Cost Plus | COGS | Reimbursable labor |
| 50200 | Materials - Cost Plus | COGS | Reimbursable materials |
| 50300 | Subcontractors - Cost Plus | COGS | Reimbursable subs |
| 50400 | Equipment - Cost Plus | COGS | Reimbursable equipment |
| 50500 | Other Direct - Cost Plus | COGS | Other reimbursable |
| 50900 | Non-Allowable Costs | COGS | Costs you can't bill |

#### Step 2: Revenue Accounts for Cost-Plus

| Account # | Name | Type | Purpose |
|-----------|------|------|---------|
| 42000 | Cost-Plus Revenue - Cost Reimbursement | Income | Costs billed to owner |
| 42100 | Cost-Plus Revenue - Fee | Income | Your fee/profit |

#### Step 3: Document Everything

**Required Documentation:**

For Labor:
- Certified payroll records
- Time sheets signed by superintendent
- Labor burden calculation support

For Materials:
- Supplier invoices
- Delivery tickets
- Material requisitions showing job assignment

For Subcontractors:
- Subcontract agreements
- Sub invoices with lien waivers
- Proof of payment

For Equipment:
- Rental agreements or internal rate schedule
- Equipment logs showing job use
- Fuel and maintenance records

### Cost-Plus Billing Process

**HOW to Bill Cost-Plus Monthly:**

1. **Compile all allowable costs for the period**
   - Run P&L by Project report
   - Verify all costs are properly coded
   - Remove any non-allowable costs

2. **Calculate the fee**
   - Fixed Fee: Prorate over project duration or bill based on % complete
   - Percentage Fee: Apply % to period costs

3. **Create the invoice**
   - List costs by category with supporting references
   - Add fee as separate line item
   - Attach cost backup package

4. **Invoice Format:**

```
COST-PLUS BILLING - November 2024
Project: Office Building Renovation

REIMBURSABLE COSTS THIS PERIOD

Labor
  Week ending 11/7    $12,450.00    (See Exhibit A)
  Week ending 11/14   $11,890.00    (See Exhibit A)
  Week ending 11/21   $13,200.00    (See Exhibit A)
  Week ending 11/28   $10,100.00    (See Exhibit A)
  ──────────────────────────────────
  Labor Subtotal      $47,640.00

Materials
  ABC Supply - Invoice #4521    $8,450.00    (See Exhibit B)
  XYZ Lumber - Invoice #892     $3,200.00    (See Exhibit B)
  ──────────────────────────────────
  Materials Subtotal           $11,650.00

Subcontractors
  Smith Electric - Pay App #3  $22,500.00    (See Exhibit C)
  ──────────────────────────────────
  Subcontractor Subtotal       $22,500.00

Equipment
  Crane rental - Week 1-2       $4,800.00    (See Exhibit D)
  ──────────────────────────────────
  Equipment Subtotal            $4,800.00

═══════════════════════════════════════════════════
TOTAL REIMBURSABLE COSTS       $86,590.00

Contractor Fee (15% Fixed,      $11,250.00
  prorated this period)

TOTAL DUE THIS PERIOD          $97,840.00
```

### Cost-Plus WIP Considerations

**Does Cost-Plus Need WIP?**

Generally NO, because:
- You bill actual costs incurred
- No estimated contract price to measure against
- Revenue = Costs billed + Fee earned

**Exception - Fixed Fee Timing:**
If fee is billed unevenly vs. work performed, minor timing adjustment may be needed.

---

## Contract Type 3: Guaranteed Maximum Price (GMP)

### What Is GMP?

> **Guaranteed Maximum Price**: A cost-plus contract with a ceiling price. The owner pays actual costs plus fee, but never more than the GMP. If costs exceed GMP, the contractor absorbs the overage.

**Common Uses:**
- Construction management at-risk
- Design-build contracts
- Large commercial projects
- Owners wanting cost control with flexibility

### GMP Structure

```
GMP CONTRACT MECHANICS

                              ┌─────────────────────────────┐
                              │     GUARANTEED MAXIMUM      │
                              │         $1,000,000          │
                              ├─────────────────────────────┤
  If costs come in            │                             │
  under GMP, savings          │      CONTINGENCY            │
  may be shared ────────────► │        $50,000              │
                              ├─────────────────────────────┤
                              │                             │
                              │    CONTRACTOR FEE           │
                              │       $100,000              │
                              ├─────────────────────────────┤
                              │                             │
                              │                             │
                              │    ESTIMATED COSTS          │
                              │       $850,000              │
                              │                             │
                              │                             │
                              └─────────────────────────────┘

If Actual Costs = $820,000:
  Owner Pays: $820,000 + $100,000 fee = $920,000
  Savings: $80,000 (split per contract terms)

If Actual Costs = $900,000:
  Owner Pays: $900,000 + $100,000 fee = $1,000,000 (GMP cap)
  No savings, but still within GMP

If Actual Costs = $950,000:
  Owner Pays: $1,000,000 (GMP cap)
  Contractor Absorbs: $50,000 loss
```

### GMP Savings Sharing

**Common Split Arrangements:**

| Structure | Owner Gets | Contractor Gets |
|-----------|------------|-----------------|
| Owner takes all | 100% | 0% |
| 50/50 Split | 50% | 50% |
| Sliding scale | First $50K, then 50/50 | Remainder |
| Contractor takes all | 0% | 100% |

### Setting Up GMP in QBO

#### Step 1: Track Like Cost-Plus Initially

GMP tracking is identical to cost-plus until you approach the GMP ceiling.

Use the same:
- Detailed cost accounts
- Documentation requirements
- Monthly billing process

#### Step 2: Create GMP Monitoring Report

**Critical:** You must know where you stand vs. GMP at all times.

**GMP Status Report Template:**

```
GMP STATUS REPORT
Project: Downtown Office Building
As of: November 30, 2024

GUARANTEED MAXIMUM PRICE                    $1,000,000

Components:
  Estimated Direct Costs        $850,000
  Contingency                    $50,000
  Contractor Fee                $100,000
                              ──────────
  Total GMP                   $1,000,000

CURRENT STATUS

Costs Incurred to Date                        $425,000
Committed Costs (POs/Subcontracts)            $380,000
                                            ──────────
Total Committed + Incurred                    $805,000

Estimated Cost to Complete (uncommitted)       $60,000
                                            ──────────
PROJECTED FINAL COST                          $865,000

PROJECTED OUTCOME
  GMP Ceiling                  $1,000,000
  Less: Projected Costs          $865,000
  Less: Contractor Fee           $100,000
                              ────────────
  Projected Savings               $35,000

  Owner Share (50%)               $17,500
  Contractor Share (50%)          $17,500
```

#### Step 3: GMP Contingency Tracking

**WHY Contingency Matters:**

The contingency is your buffer. Track it carefully:

```
GMP CONTINGENCY LOG

Starting Contingency: $50,000

Date       Description                    Used      Remaining
──────────────────────────────────────────────────────────────
11/5/24    Unforeseen soil conditions    $8,500      $41,500
11/12/24   Owner-requested upgrade       $0*         $41,500
11/20/24   Weather delays                $3,200      $38,300
──────────────────────────────────────────────────────────────
Current Contingency Balance                          $38,300

* Owner upgrade was added via Change Order, increasing GMP
```

### GMP Revenue Recognition

**The Complexity:** GMP is a hybrid - cost-plus billing but with a fixed ceiling.

**GAAP Approach:**

1. **During project:** Recognize revenue as costs are incurred plus proportionate fee
2. **If trending under GMP:** Consider savings share in projections
3. **If trending over GMP:** Recognize projected loss immediately

**Loss Recognition Example:**

```
GMP: $1,000,000 (including $100,000 fee)
Current Costs: $700,000
Projected Final Costs: $950,000

Projected Outcome:
  Owner Pays (GMP cap): $1,000,000
  Minus Projected Costs: ($950,000)
  Contractor Fee Realized: $50,000 (vs. $100,000 expected)

Loss to Recognize: $50,000 fee reduction should be recognized
as soon as the loss becomes probable
```

---

## Contract Type 4: Unit Price Contracts

### What Is Unit Price?

> **Unit Price**: A contract where payment is based on actual quantities of work installed at pre-agreed unit prices. Total contract value depends on actual quantities.

**Common Uses:**
- Site work and excavation
- Road and highway construction
- Underground utilities
- Concrete work
- Repetitive tasks with variable quantities

### Unit Price Structure

```
UNIT PRICE CONTRACT EXAMPLE

Bid Item   Description              Unit    Est. Qty    Unit Price    Est. Value
──────────────────────────────────────────────────────────────────────────────────
001        Clearing & Grubbing      Acre       15         $2,500       $37,500
002        Excavation               CY       8,000          $12       $96,000
003        Fill Material            CY       5,000          $18       $90,000
004        Concrete Paving          SY       2,500          $85      $212,500
005        Storm Drainage - 18"     LF       1,200          $45       $54,000
006        Storm Drainage - 24"     LF         800          $62       $49,600
──────────────────────────────────────────────────────────────────────────────────
ESTIMATED CONTRACT TOTAL                                             $539,600

ACTUAL QUANTITIES (End of Project):

Bid Item   Description              Unit    Est. Qty    Act. Qty    Unit Price    Actual Value
───────────────────────────────────────────────────────────────────────────────────────────────
001        Clearing & Grubbing      Acre       15          15         $2,500        $37,500
002        Excavation               CY       8,000       9,200          $12       $110,400
003        Fill Material            CY       5,000       4,800          $18        $86,400
004        Concrete Paving          SY       2,500       2,500          $85       $212,500
005        Storm Drainage - 18"     LF       1,200       1,350          $45        $60,750
006        Storm Drainage - 24"     LF         800         750          $62        $46,500
───────────────────────────────────────────────────────────────────────────────────────────────
FINAL CONTRACT VALUE                                                              $554,050

Variance from Estimate: +$14,450 (+2.7%)
```

### Setting Up Unit Price in QBO

#### Step 1: Create Products/Services for Each Bid Item

**HOW:**

Go to **Settings ⚙️** → **Products and Services** → **New**

| Name | Type | Rate | Income Account |
|------|------|------|----------------|
| UP-001 Clearing & Grubbing | Service | $2,500 | 43000 Unit Price Revenue |
| UP-002 Excavation | Service | $12 | 43000 Unit Price Revenue |
| UP-003 Fill Material | Service | $18 | 43000 Unit Price Revenue |
| UP-004 Concrete Paving | Service | $85 | 43000 Unit Price Revenue |

#### Step 2: Create Quantity Tracking System

**QBO Limitation:** QBO doesn't have native quantity tracking. Options:

**Option A: Excel Quantity Log (Recommended)**

```
QUANTITY LOG - Highway Project

Bid Item 002: Excavation (Unit: CY, Price: $12)

Date        Location      Qty Today    Qty to Date    Value to Date
─────────────────────────────────────────────────────────────────────
11/1/24     Station 0+00      450          450          $5,400
11/2/24     Station 0+00      380          830          $9,960
11/3/24     Station 1+00      420        1,250         $15,000
...
11/30/24    Station 5+00      290        9,200        $110,400
─────────────────────────────────────────────────────────────────────
Monthly Total: 2,100 CY = $25,200
```

**Option B: Use QBO Project with Notes**

Track quantities in project notes or attachments.

#### Step 3: Billing Based on Quantities

**Monthly Billing Process:**

1. Field measures quantities installed this period
2. Quantities verified (often by owner's inspector)
3. Invoice created with verified quantities

**Invoice Example:**

```
UNIT PRICE BILLING - November 2024
Project: Highway Widening - Phase 2

Bid Item    Description         Unit    Qty This Period    Unit Price    Amount
──────────────────────────────────────────────────────────────────────────────────
002         Excavation          CY          2,100            $12.00      $25,200
003         Fill Material       CY          1,200            $18.00      $21,600
004         Concrete Paving     SY            600            $85.00      $51,000
──────────────────────────────────────────────────────────────────────────────────
TOTAL THIS PERIOD                                                       $97,800

Previous Billings                                                      $312,450
Total Billed to Date                                                   $410,250
```

### Unit Price Revenue Recognition

**Percentage of Completion for Unit Price:**

```
% Complete = Quantities Installed to Date ÷ Estimated Total Quantities

OR (more accurate)

% Complete = Revenue Earned to Date ÷ Estimated Total Contract Value
```

**Example:**

```
Estimated Contract Value: $539,600
Revenue to Date (based on quantities): $410,250
% Complete: $410,250 ÷ $539,600 = 76%
```

### Unit Price Profitability Analysis

**The Key Question:** Are your unit prices covering your actual unit costs?

**Unit Cost Analysis:**

```
BID ITEM 002: EXCAVATION

Unit Price: $12.00/CY

ACTUAL COSTS THIS MONTH
  Equipment (excavator, trucks)     $15,400
  Labor                              $6,200
  Fuel                               $3,100
  ─────────────────────────────────────────
  Total Costs                       $24,700

Quantity Installed: 2,100 CY
Actual Unit Cost: $24,700 ÷ 2,100 = $11.76/CY

Unit Profit: $12.00 - $11.76 = $0.24/CY (2% margin)

⚠️ WARNING: Margin is thin. Monitor closely.
```

### Unbalanced Bids in Unit Price

**What Is Unbalancing?**

Contractors sometimes "unbalance" bids by:
- Increasing unit prices on early work items
- Decreasing unit prices on later work items
- Same total bid, but better cash flow

**Example:**

```
BALANCED vs. UNBALANCED BID

Item          Est. Qty    Balanced    Unbalanced    Difference
──────────────────────────────────────────────────────────────
Excavation      8,000       $12.00       $15.00      Front-loaded
(done first)

Paving          2,500       $85.00       $73.00      Back-loaded
(done last)

Total Bid                  $539,600     $539,600     Same total
```

**Cash Flow Impact:** Unbalanced bid collects more money early in the project.

**QBO Tracking:** Track actual profitability by bid item to ensure unbalanced items don't become losses.

---

## Contract Type Comparison Summary

| Feature | Fixed Price | T&M | Cost-Plus | GMP | Unit Price |
|---------|-------------|-----|-----------|-----|------------|
| **Price certainty** | Fixed | None | None | Capped | Variable |
| **Scope definition** | Complete | Open | Evolving | Mostly defined | Defined work, variable qty |
| **Contractor risk** | High | Low | Low | Medium | Medium |
| **Owner risk** | Low | High | High | Medium | Medium |
| **Documentation** | Standard | High | Very High | Very High | High |
| **WIP needed** | Yes | No | Usually no | Hybrid | Modified |
| **Billing basis** | Progress % | Hours + materials | Cost + fee | Cost + fee | Quantities |
| **QBO complexity** | Standard | Medium | High | High | Medium |

---

## QBO Setup Summary by Contract Type

### Products/Services to Create

| Contract Type | Products/Services Needed |
|---------------|-------------------------|
| Fixed Price | Standard job cost items |
| T&M | Labor rates by category, materials markup item |
| Cost-Plus | Cost reimbursement item, fee item |
| GMP | Same as Cost-Plus |
| Unit Price | One item per bid item with unit price |

### Revenue Accounts to Create

| Account # | Name | Used For |
|-----------|------|----------|
| 40000 | Contract Revenue | Fixed price contracts |
| 41000-41300 | T&M Revenue (Labor/Materials/Equipment/Other) | T&M contracts |
| 42000-42100 | Cost-Plus Revenue (Reimbursement/Fee) | Cost-Plus and GMP |
| 43000 | Unit Price Revenue | Unit price contracts |

---

## Common Mistakes by Contract Type

### T&M Mistakes

| Mistake | Impact | Prevention |
|---------|--------|------------|
| Not billing weekly | Cash flow delays | Set weekly billing schedule |
| Missing time documentation | Unbillable hours | Require daily signed time sheets |
| Forgetting material markup | Lost profit | Create markup item in QBO |
| Exceeding NTE without approval | Unbillable work | Track against cap weekly |

### Cost-Plus Mistakes

| Mistake | Impact | Prevention |
|---------|--------|------------|
| Billing non-allowable costs | Disputed invoices, trust issues | Review contract allowable list |
| Poor documentation | Rejected costs | Document everything contemporaneously |
| Overhead confusion | Under-recovery | Clearly separate direct vs. indirect |
| Late billing | Cash flow strain | Bill monthly at minimum |

### GMP Mistakes

| Mistake | Impact | Prevention |
|---------|--------|------------|
| Not tracking contingency | Surprise losses | Maintain contingency log |
| Ignoring cost trends | Late loss recognition | Monthly cost projections |
| Unclear savings sharing | Disputes at closeout | Document split in contract |
| Treating like fixed price | Under-documentation | Maintain cost-plus level documentation |

### Unit Price Mistakes

| Mistake | Impact | Prevention |
|---------|--------|------------|
| Not verifying quantities | Billing disputes | Get owner sign-off on quantities |
| Unbalanced bid backfires | Losses on later items | Track profit by bid item |
| Quantity overruns unnoticed | Scope creep | Compare actual to estimated monthly |
| Missing approved quantity changes | Under-billing | Document all approved qty changes |

---

## Key Takeaways

1. **Know your contract type** before setting up QBO tracking
2. **Documentation requirements vary** - Cost-Plus/GMP need the most
3. **WIP schedules apply differently** - Fixed price needs full WIP; T&M typically doesn't
4. **Cash flow patterns differ** - T&M and Cost-Plus bill as you go; Fixed Price depends on billing schedule
5. **Risk allocation matters** - Higher contractor risk = more importance on estimating and cost control

---

## Next Steps

- For WIP on fixed-price contracts → [WIP Schedules](./04-wip-schedules.md)
- For billing mechanics → [Progress Billing](./05-progress-billing.md)
- For tracking change orders on any contract → [Change Order Management](./08-change-orders.md)

---

*[← Previous: Change Order Management](./08-change-orders.md) | [Next: Cash Flow Forecasting →](./10-cash-flow-forecasting.md)*
