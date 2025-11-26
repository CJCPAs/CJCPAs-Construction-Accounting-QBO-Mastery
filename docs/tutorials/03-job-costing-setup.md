# Job Costing Setup in QuickBooks Online

## Overview

Job costing is the foundation of construction accounting. It answers the most critical question: **"Am I making or losing money on this job?"**

This chapter provides a hyper-detailed tutorial on setting up comprehensive job costing in QBO, with every HOW linked to the WHY behind it.

---

## What is Job Costing?

### The Simple Definition
Job costing is tracking every dollar of income and expense associated with a specific project.

### The GAAP Definition

> **GAAP Principle**: Under the **Matching Principle**, costs must be matched to the revenues they help generate within the same accounting period. Job costing is the mechanism that enables this matching at the project level.

### Why Construction Companies MUST Have Job Costing

```
Without Job Costing:
┌────────────────────────────────────────────────┐
│ Income Statement (Monthly)                      │
├────────────────────────────────────────────────┤
│ Total Revenue:          $500,000               │
│ Total Costs:            $450,000               │
│ Gross Profit:            $50,000 (10%)         │
│                                                │
│ Status: "We made money... probably"            │
└────────────────────────────────────────────────┘

With Job Costing:
┌────────────────────────────────────────────────┐
│ Job Profitability Report                        │
├────────────────────────────────────────────────┤
│ Job A: Revenue $200K, Cost $150K = $50K (25%) ✅│
│ Job B: Revenue $150K, Cost $120K = $30K (20%) ✅│
│ Job C: Revenue $100K, Cost $130K = -$30K 🚨    │
│ Job D: Revenue  $50K, Cost  $50K = $0   ⚠️     │
│                                                │
│ Status: "Job C is bleeding $30K - FIX NOW!"   │
└────────────────────────────────────────────────┘
```

**The Power**: With job costing, you can identify and fix problems *during* the project, not after.

---

## The Five Cost Categories for Construction

Every construction project has five core cost categories. Your job costing system must track each separately.

### 1. Labor (Direct)

**What It Includes:**
- Wages paid to workers on the job
- Payroll taxes (employer portion)
- Workers' compensation insurance
- Benefits (health, retirement contributions)

**WHY Track Separately:**
Labor is typically 30-50% of project costs. Tracking it separately reveals:
- Which jobs have labor overruns
- Which crews are most efficient
- Whether estimates are accurate

### 2. Materials

**What It Includes:**
- Lumber, concrete, steel, etc.
- Electrical, plumbing supplies
- Finishing materials
- Fasteners, adhesives, consumables

**WHY Track Separately:**
Material costs can fluctuate dramatically. Tracking reveals:
- Price variance vs. estimate
- Waste factors by project type
- Opportunities for bulk purchasing

### 3. Subcontractors

**What It Includes:**
- Contracted work from licensed subs
- Specialty trades (HVAC, electrical, plumbing)
- Sitework, excavation
- Any work you don't self-perform

**WHY Track Separately:**
Subs are often 40-60% of commercial project costs. Tracking reveals:
- Sub performance and reliability
- Budget variance by trade
- Scope creep indicators

### 4. Equipment

**What It Includes:**
- Equipment rentals
- Owned equipment charges (internal)
- Fuel for job-specific equipment
- Small tools and consumables

**WHY Track Separately:**
Equipment costs are often buried in overhead. Proper tracking:
- Ensures full cost recovery
- Identifies ownership vs. rental decisions
- Supports equipment replacement planning

### 5. Other Direct Costs

**What It Includes:**
- Permits and fees
- Job-site utilities
- Project insurance (if job-specific)
- Testing and inspections
- Bonds (if job-specific)

**WHY Track Separately:**
These costs are easy to forget in estimates. Tracking reveals true job costs.

---

## Step-by-Step: Creating Your Job Cost Structure

### Step 1: Set Up Your Cost Chart of Accounts

**WHY**: Your Chart of Accounts (COA) must have separate accounts for each cost category to enable meaningful job cost reports.

**HOW to Create Job Cost Accounts:**

1. Go to **Settings ⚙️** → **Chart of Accounts**
2. Click **New** to create each account below

**Recommended Cost of Goods Sold Accounts:**

| Account # | Name | Type | Detail Type |
|-----------|------|------|-------------|
| 50000 | Direct Costs | COGS | Cost of Labor-COS |
| 50100 | ↳ Labor - Direct | COGS | Cost of Labor-COS |
| 50110 | ↳ ↳ Labor - Regular | COGS | Cost of Labor-COS |
| 50120 | ↳ ↳ Labor - Overtime | COGS | Cost of Labor-COS |
| 50130 | ↳ ↳ Payroll Taxes | COGS | Cost of Labor-COS |
| 50140 | ↳ ↳ Workers Comp | COGS | Cost of Labor-COS |
| 50200 | ↳ Materials | COGS | Supplies & Materials-COGS |
| 50210 | ↳ ↳ Lumber & Framing | COGS | Supplies & Materials-COGS |
| 50220 | ↳ ↳ Electrical Materials | COGS | Supplies & Materials-COGS |
| 50230 | ↳ ↳ Plumbing Materials | COGS | Supplies & Materials-COGS |
| 50240 | ↳ ↳ Concrete & Masonry | COGS | Supplies & Materials-COGS |
| 50250 | ↳ ↳ Finishes | COGS | Supplies & Materials-COGS |
| 50260 | ↳ ↳ Other Materials | COGS | Supplies & Materials-COGS |
| 50300 | ↳ Subcontractors | COGS | Subcontractors-COGS |
| 50310 | ↳ ↳ Sub - Electrical | COGS | Subcontractors-COGS |
| 50320 | ↳ ↳ Sub - Plumbing | COGS | Subcontractors-COGS |
| 50330 | ↳ ↳ Sub - HVAC | COGS | Subcontractors-COGS |
| 50340 | ↳ ↳ Sub - Drywall | COGS | Subcontractors-COGS |
| 50350 | ↳ ↳ Sub - Concrete | COGS | Subcontractors-COGS |
| 50360 | ↳ ↳ Sub - Other | COGS | Subcontractors-COGS |
| 50400 | ↳ Equipment Costs | COGS | Equipment Rental-COS |
| 50410 | ↳ ↳ Equipment Rental | COGS | Equipment Rental-COS |
| 50420 | ↳ ↳ Equipment - Owned | COGS | Equipment Rental-COS |
| 50430 | ↳ ↳ Fuel - Job | COGS | Equipment Rental-COS |
| 50440 | ↳ ↳ Small Tools | COGS | Supplies & Materials-COGS |
| 50500 | ↳ Other Direct Costs | COGS | Other Costs of Services-COS |
| 50510 | ↳ ↳ Permits & Fees | COGS | Other Costs of Services-COS |
| 50520 | ↳ ↳ Job Site Utilities | COGS | Other Costs of Services-COS |
| 50530 | ↳ ↳ Testing & Inspections | COGS | Other Costs of Services-COS |
| 50540 | ↳ ↳ Job Insurance | COGS | Other Costs of Services-COS |

**WHY This Structure:**
- **Sub-accounts** create hierarchy: You can see total Direct Costs OR drill into Labor detail
- **Consistent numbering**: Easy to sort and find accounts
- **COGS classification**: These show *before* Gross Profit on P&L, distinguishing from overhead

### Step 2: Set Up Income Accounts

**HOW to Create Income Accounts:**

| Account # | Name | Type | Detail Type |
|-----------|------|------|-------------|
| 40000 | Contract Revenue | Income | Service/Fee Income |
| 40100 | ↳ Labor Revenue | Income | Service/Fee Income |
| 40200 | ↳ Materials Revenue | Income | Sales of Product Income |
| 40300 | ↳ Subcontractor Revenue | Income | Service/Fee Income |
| 40400 | ↳ Equipment Revenue | Income | Service/Fee Income |
| 40500 | ↳ Other Revenue | Income | Service/Fee Income |
| 40600 | Change Order Revenue | Income | Service/Fee Income |

**WHY Separate Income Categories:**
This structure lets you see not just total revenue, but where that revenue comes from. Common insights:
- "We're losing money on material pass-throughs" 
- "Labor revenue doesn't cover labor cost - raise billing rates!"
- "Equipment charges cover only 60% of equipment costs"

### Step 3: Link Products/Services to Accounts

**WHY This Matters:**
When you select a Product/Service on an invoice or bill, it determines which account is affected. Proper linking = accurate reports.

**HOW to Create/Update Products & Services:**

1. Go to **Settings ⚙️** → **Products and Services**
2. Click **New** or edit existing items

**Income Items (for Invoices):**

| Product/Service Name | Type | Income Account | Rate |
|---------------------|------|----------------|------|
| Labor - T&M | Service | 40100 Labor Revenue | Hourly |
| Labor - Fixed | Service | 40100 Labor Revenue | Per job |
| Materials - Cost Plus | Service | 40200 Materials Revenue | Cost + % |
| Materials - Lump Sum | Service | 40200 Materials Revenue | Fixed |
| Subcontractor Markup | Service | 40300 Sub Revenue | Per invoice |
| Equipment Charge | Service | 40400 Equipment Revenue | Daily/Weekly |
| Permit Reimbursement | Service | 40500 Other Revenue | Cost |
| Change Order | Service | 40600 Change Order Revenue | Per CO |

**Expense Items (for Bills/Expenses):**

| Product/Service Name | Type | Expense Account | Description |
|---------------------|------|-----------------|-------------|
| Labor Cost | Service | 50100 Labor - Direct | For time tracking import |
| Materials - Lumber | Service | 50210 Lumber & Framing | Material purchases |
| Materials - Electrical | Service | 50220 Electrical Materials | Material purchases |
| Sub - Electrical | Service | 50310 Sub - Electrical | Sub bills |
| Sub - Plumbing | Service | 50320 Sub - Plumbing | Sub bills |
| Equipment Rental | Service | 50410 Equipment Rental | Rental invoices |
| Permits | Service | 50510 Permits & Fees | Permit payments |

### Step 4: Create Projects for Each Job

**HOW:**
1. Go to **Projects** in left navigation
2. Click **New project** (or **Start a project**)
3. Enter:
   - **Name**: Use established naming convention (e.g., `2024-001-SmithResidence-Kitchen`)
   - **Customer**: Select or create customer
   - **Status**: Active (or your preferred status)
4. Click **Save**

**WHY Projects vs. Just Customers:**
Projects give you:
- Single dashboard showing all job activity
- Easy project-level P&L reports
- Time tracking by project
- Billable expense tracking by project

---

## Recording Job Costs: Detailed Workflows

### Recording Labor Costs

#### Method 1: Time Tracking (Recommended)

**HOW:**
1. Go to **Time** (left navigation) → **Enter time** or use **Single time activity**
2. Fill in:
   - **Employee/Contractor**: Who worked
   - **Customer**: Which customer
   - **Service**: Labor - T&M (or appropriate item)
   - **Billable**: Check if billing to customer
   - **Hours**: Time worked
   - **Rate**: Employee's hourly cost (not bill rate)
3. Save

**WHY Time Tracking is Superior:**
- Creates audit trail for billing disputes
- Enables comparison of estimated vs. actual hours
- Supports compliance (certified payroll, prevailing wage)
- Auto-populates invoices (billable time)

#### Method 2: Payroll Integration

If using QBO Payroll:
1. Employee hours flow to Projects automatically
2. Ensure employees select correct Project when entering time
3. Review **Reports** → **Project Profitability** to verify

**WHY Integration Matters:**
Manual entry of labor costs risks:
- Missed hours (costs not captured)
- Duplicate entry (costs overstated)
- Timing errors (wrong period)

### Recording Material Costs

**HOW to Enter Material Bills:**

1. Go to **Expenses** → **Bills** → **Create bill**
2. Fill in:
   - **Vendor**: Supplier name
   - **Bill date**: Invoice date from supplier
   - **Due date**: Payment deadline
3. In the **Item details** section:
   - **Product/Service**: Select appropriate material item
   - **Qty**: Quantity purchased
   - **Rate**: Unit cost
   - **Customer**: Assign to project
   - **Billable**: Check if passing through to customer
4. Attach supplier invoice (recommended)
5. Save

**Example Entry:**
```
Vendor: ABC Lumber Supply
Date: 2024-01-15
Due: 2024-02-14

Item Details:
┌────────────────────┬─────┬───────┬──────────┬───────────────────────┬──────────┐
│ Product/Service    │ Qty │ Rate  │ Amount   │ Customer              │ Billable │
├────────────────────┼─────┼───────┼──────────┼───────────────────────┼──────────┤
│ Materials - Lumber │ 200 │ $4.50 │ $900.00  │ 2024-001-SmithRes...  │ ✓        │
│ Materials - Lumber │ 50  │ $8.00 │ $400.00  │ 2024-001-SmithRes...  │ ✓        │
│ Materials - Other  │ 1   │ $75.00│ $75.00   │ 2024-001-SmithRes...  │ ✓        │
└────────────────────┴─────┴───────┴──────────┴───────────────────────┴──────────┘
Total: $1,375.00
```

**WHY Assign Customer/Project:**
Without project assignment:
- Cost appears in total COGS but not on project report
- Job profitability is understated
- You can't identify which job drove the material purchase

### Recording Subcontractor Costs

**HOW to Enter Sub Bills:**

1. Go to **Expenses** → **Bills** → **Create bill**
2. Fill in vendor (subcontractor), dates
3. In **Item details**:
   - **Product/Service**: Sub - [Trade] (e.g., Sub - Electrical)
   - **Amount**: Invoice amount
   - **Customer**: Assign to project
   - **Billable**: Check if marking up to customer
4. **CRITICAL**: Attach sub's invoice and any lien waivers
5. Save

**WHY Lien Waiver Attachment:**
- Creates paper trail for payment disputes
- Proves payment was made before releasing retention
- Required by most GCs for payment

### Recording Equipment Costs

#### For Equipment Rentals

**HOW:**
1. Create bill from rental company
2. Use Product/Service: Equipment Rental
3. Assign to project

#### For Owned Equipment (Internal Charges)

**WHY Charge Internal Equipment:**
Your backhoe costs money whether it's working or not (depreciation, insurance, maintenance). If you don't charge jobs for equipment use, you:
- Understate job costs
- Overstate job profitability
- Have no data for own vs. rent decisions

**HOW to Set Up Internal Equipment Charges:**

Method A: Journal Entry (Monthly)
1. Go to **+ New** → **Journal Entry**
2. Entry:
   ```
   Date: [Last day of month]
   
   | Account                    | Debit     | Credit    | Customer              |
   |----------------------------|-----------|-----------|----------------------|
   | 50420 Equipment - Owned    | $2,500.00 |           | 2024-001-SmithRes... |
   | 16000 Accum Depreciation   |           | $2,000.00 |                      |
   | 60400 Equipment Maint Exp  |           | $500.00   |                      |
   ```

Method B: Create "Internal Equipment" Vendor
1. Create vendor named "Internal Equipment Charges"
2. Create bill from this vendor for equipment used
3. Pay bill from an equity account (to avoid affecting cash)

**WHY Journal Entry vs. Bill:**
- Journal entries are cleaner for recurring charges
- Bills create a paper trail but add AP complexity
- Choose based on your audit requirements

---

## Job Cost Budget Setup

### Creating Project Budgets in QBO

**WHY Budgets Matter:**

> **The 80/20 Rule**: 80% of your project overruns will be caught in the first 20% of the project—IF you have budgets and monitor them.

Without budgets, you discover problems when the job is done (too late).

**HOW to Create a Project Budget:**

1. Go to **Settings ⚙️** → **Budgeting** 
2. Click **Add budget**
3. Fill in:
   - **Name**: Budget for [Project Name]
   - **Fiscal year**: Current year
   - **Interval**: Monthly (or quarterly)
   - **Pre-fill data**: Optionally copy from prior year
4. Click **Next**
5. **Critical**: Select **By Customer** view and filter to your project
6. Enter budgeted amounts for each cost account per period
7. Save

**Sample Project Budget:**

```
Project: 2024-001-SmithResidence
Contract Value: $150,000
Duration: Jan-Mar 2024

┌────────────────────────┬──────────┬──────────┬──────────┬──────────┐
│ Account                │ January  │ February │ March    │ Total    │
├────────────────────────┼──────────┼──────────┼──────────┼──────────┤
│ 40000 Contract Revenue │ $50,000  │ $50,000  │ $50,000  │ $150,000 │
├────────────────────────┼──────────┼──────────┼──────────┼──────────┤
│ 50100 Labor - Direct   │ $15,000  │ $18,000  │ $12,000  │ $45,000  │
│ 50200 Materials        │ $20,000  │ $12,000  │ $8,000   │ $40,000  │
│ 50300 Subcontractors   │ $5,000   │ $15,000  │ $10,000  │ $30,000  │
│ 50400 Equipment        │ $2,000   │ $2,000   │ $1,000   │ $5,000   │
│ 50500 Other Direct     │ $1,000   │ $500     │ $500     │ $2,000   │
├────────────────────────┼──────────┼──────────┼──────────┼──────────┤
│ TOTAL COSTS            │ $43,000  │ $47,500  │ $31,500  │ $122,000 │
│ GROSS PROFIT           │ $7,000   │ $2,500   │ $18,500  │ $28,000  │
│ GROSS MARGIN           │ 14%      │ 5%       │ 37%      │ 18.7%    │
└────────────────────────┴──────────┴──────────┴──────────┴──────────┘
```

---

## Running Job Cost Reports

### Essential Job Cost Reports

#### Report 1: Project Profitability (Built-in)

**HOW:**
1. Go to **Reports** → Search "Project Profitability"
2. Set date range
3. Run report

**WHAT You'll See:**
- Revenue by project
- Costs by project
- Gross profit by project

**WHY This Report:**
The 30-second answer to "Which jobs are making/losing money?"

#### Report 2: Profit & Loss by Customer (Detailed)

**HOW:**
1. Go to **Reports** → Search "Profit and Loss by Customer"
2. Set date range
3. Customize: Select specific customers/projects if needed
4. Run report

**WHAT You'll See:**
Full P&L for each customer, with cost breakdown

**WHY This Report:**
Deeper dive into where costs are incurred within each job

#### Report 3: Budget vs. Actual by Customer

**HOW:**
1. Go to **Reports** → Search "Budget vs. Actuals"
2. Set date range and budget
3. Display columns: Budget, Actual, Difference, % of Budget
4. Customize by Customer
5. Run report

**WHAT You'll See:**
```
2024-001-SmithResidence - Jan 2024
┌─────────────────────┬──────────┬──────────┬────────────┬─────────┐
│ Account             │ Budget   │ Actual   │ Difference │ % Used  │
├─────────────────────┼──────────┼──────────┼────────────┼─────────┤
│ Materials           │ $20,000  │ $22,500  │ $(2,500)   │ 112.5%  │ 🚨
│ Labor               │ $15,000  │ $13,800  │ $1,200     │ 92%     │ ✅
│ Subcontractors      │ $5,000   │ $4,200   │ $800       │ 84%     │ ✅
└─────────────────────┴──────────┴──────────┴────────────┴─────────┘
```

**WHY This Report:**
Catch problems DURING the job:
- Material costs at 112% = investigate immediately!
- Why is lumber running over? Waste? Price increase? Scope change?

---

## The Job Costing Cycle: Putting It All Together

```
┌───────────────────────────────────────────────────────────────────────────────┐
│                        WEEKLY JOB COSTING CYCLE                               │
├───────────────────────────────────────────────────────────────────────────────┤
│                                                                               │
│  Monday: Enter Time                                                          │
│  ┌────────────────────┐                                                      │
│  │ • Review timesheets│ ───▶ Time entries by project                        │
│  │ • Enter in QBO     │                                                      │
│  │ • Verify projects  │                                                      │
│  └────────────────────┘                                                      │
│           │                                                                   │
│           ▼                                                                   │
│  Tuesday-Thursday: Enter Costs                                               │
│  ┌────────────────────┐                                                      │
│  │ • Enter AP bills   │ ───▶ Costs coded to projects                        │
│  │ • Match to POs     │                                                      │
│  │ • Verify coding    │                                                      │
│  └────────────────────┘                                                      │
│           │                                                                   │
│           ▼                                                                   │
│  Friday: Review & Report                                                      │
│  ┌────────────────────┐                                                      │
│  │ • Run job cost rpts│ ───▶ Identify issues                                │
│  │ • Review budget    │      Flag overruns                                   │
│  │ • Meet with PMs    │      Take action                                     │
│  └────────────────────┘                                                      │
│                                                                               │
└───────────────────────────────────────────────────────────────────────────────┘
```

---

## Common Job Costing Mistakes

### Mistake 1: Not Assigning to Project

**Symptom**: Job reports show less cost than expected
**Cause**: Expenses entered without Customer/Project assignment
**Fix**: 
1. Run **Transaction List by Customer** 
2. Filter for blank customer
3. Edit transactions to add project

### Mistake 2: Using Wrong Accounts

**Symptom**: Labor shows in Materials, etc.
**Cause**: Products/Services linked to wrong accounts
**Fix**: Audit Products/Services settings

### Mistake 3: Ignoring Small Transactions

**Symptom**: Job profits mysteriously low
**Cause**: Job-site gas, small tools, etc. not coded
**Fix**: Create petty cash process that requires project coding

### Mistake 4: No Budget Comparison

**Symptom**: Problems discovered at job completion
**Cause**: No benchmark for comparison during job
**Fix**: Enter budgets before starting work

### Mistake 5: Equipment Not Charged

**Symptom**: Jobs with heavy equipment use show high profit
**Cause**: Internal equipment costs not allocated
**Fix**: Implement internal equipment charge system

---

## Job Costing Verification Checklist

Weekly verification:
- [ ] All timesheets entered and coded to projects
- [ ] All AP bills entered and coded to projects  
- [ ] No transactions with blank Customer/Project
- [ ] Job cost reports match expectations
- [ ] Budget vs. actual reviewed for active projects

Monthly verification:
- [ ] All payroll entries coded to projects
- [ ] Equipment charges allocated
- [ ] WIP analysis completed (see next chapter)
- [ ] Problem jobs flagged and discussed

---

## Next Steps

Now that you have job costing set up, the next step is understanding how costs translate to financial reporting. In [WIP Schedules & Percentage-of-Completion](./04-wip-schedules.md), you'll learn:
- How to calculate percentage of completion
- When to recognize revenue under GAAP
- Over/under billing analysis
- Producing WIP reports for your bonding company

---

*[← Previous: Getting Started](../02-getting-started.md) | [Next: WIP Schedules →](./04-wip-schedules.md)*
