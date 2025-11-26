# Getting Started with QBO for Construction

## Overview

Before diving into job costing and WIP schedules, we need to configure QuickBooks Online with the proper settings for construction accounting. This chapter covers the essential setup that makes everything else possible.

---

## Required QBO Subscription Level

### Why QBO Plus or Advanced?

| Feature | Simple Start | Essentials | Plus | Advanced |
|---------|--------------|------------|------|----------|
| **Class Tracking** | ❌ | ❌ | ✅ | ✅ |
| **Location Tracking** | ❌ | ❌ | ✅ | ✅ |
| **Project Tracking** | ❌ | ❌ | ✅ | ✅ |
| **Budgets** | ❌ | ❌ | ✅ | ✅ |
| **Custom Fields** | ❌ | ❌ | Limited | ✅ |
| **Bill by Customer** | ❌ | ✅ | ✅ | ✅ |
| **Inventory** | ❌ | ❌ | ✅ | ✅ |

> **WHY IT MATTERS**: Job costing requires tracking income and expenses by project. Without Class/Location/Project tracking (available only in Plus and Advanced), you cannot generate job-level profitability reports.

---

## Step 1: Enable Essential Features

### Turn On Project Tracking

**HOW:**
1. Go to **Settings ⚙️** → **Account and Settings**
2. Select **Advanced** tab
3. Under **Projects**, turn on "Organize all job-related activity in one place"
4. Click **Save**, then **Done**

**WHY:** Projects in QBO act as containers for all job-related transactions. Without Projects enabled:
- You can't see all income/expenses for a job in one place
- You'll struggle to calculate job profitability
- Progress billing becomes a manual nightmare

### Turn On Class Tracking

**HOW:**
1. Go to **Settings ⚙️** → **Account and Settings**
2. Select **Advanced** tab
3. Under **Categories**, turn on "Track classes"
4. Choose "One to entire transaction" OR "One to each row in transaction" (recommended: "One to each row" for construction)
5. Click **Save**, then **Done**

**WHY (The Accounting Reason):** 
Classes create a parallel tracking dimension. While your Chart of Accounts tracks *what* money is (labor, materials, equipment), Classes track *which job* the money relates to. This enables:
- Job-level P&L statements
- Comparison across jobs of the same type
- Departmental tracking (if you have multiple divisions)

**WHY (The Practical Reason):**
When your bonding company asks "What's your gross profit on commercial projects vs. residential?" you can answer in 2 minutes instead of 2 days.

### Turn On Location Tracking (Optional but Recommended)

**HOW:**
1. Go to **Settings ⚙️** → **Account and Settings**
2. Select **Advanced** tab
3. Under **Categories**, turn on "Track locations"
4. Click **Save**, then **Done**

**WHY:** If you work in multiple states/cities, Location tracking helps with:
- Multi-state tax compliance
- Regional profitability analysis
- Worker's comp audits (rates vary by state)

---

## Step 2: Set Up Your Fiscal Year and Accounting Method

### Configure Fiscal Year

**HOW:**
1. Go to **Settings ⚙️** → **Account and Settings**
2. Select **Advanced** tab
3. Under **Accounting**, set your fiscal year start month
4. Click **Save**, then **Done**

### Cash vs. Accrual Basis

**HOW:**
1. Go to **Settings ⚙️** → **Account and Settings**
2. Select **Advanced** tab
3. Under **Accounting**, select "Accrual" for Accounting method
4. Click **Save**, then **Done**

**WHY ACCRUAL IS ESSENTIAL FOR CONSTRUCTION:**

> **GAAP Principle**: The **Matching Principle** requires that expenses be recognized in the same period as the revenues they help generate.

| Scenario | Cash Basis | Accrual Basis |
|----------|------------|---------------|
| You buy $50K materials in January | January: $50K expense | January: $50K asset (inventory/WIP) |
| You bill customer $200K in March | March: $200K income | March: $200K income & matched expenses |
| **Result** | January shows huge loss, March shows huge profit | Both months show accurate profit |

**For Tax Purposes**: You can still file taxes on cash basis (if you qualify), but your internal books should be accrual for accurate job costing.

---

## Step 3: Create Your Project/Job Structure

### Naming Convention (Critical!)

Establish a consistent naming convention **before** creating projects. This decision affects reporting for years to come.

**Recommended Format:**
```
[Year]-[Job Number]-[Client Last Name/Company]-[Short Description]
```

**Examples:**
- `2024-001-SmithResidence-Kitchen-Remodel`
- `2024-002-ABCCorp-Office-Buildout`
- `2024-003-Johnson-NewConstruction`

**WHY THIS FORMAT:**
1. **Year prefix**: Jobs sort chronologically
2. **Sequential number**: Prevents duplicates
3. **Client name**: Easy identification
4. **Description**: Distinguishes multiple jobs for same client

### Creating Your First Project

**HOW:**
1. Go to **Projects** (left navigation)
2. Click **Start a project** (or **+ New project** if you have existing projects)
3. Fill in:
   - **Project name**: Use your naming convention
   - **Customer**: Select existing or create new
   - **Status**: Set to appropriate status
4. Click **Save**

**Optional but Valuable Fields:**
- **Start date / End date**: Helps with timeline tracking
- **Notes**: Contract number, site address, project manager

---

## Step 4: Understand QBO's Job Costing Hierarchy

```
                    ┌───────────────┐
                    │    COMPANY    │
                    │   (All Jobs)  │
                    └───────┬───────┘
                            │
            ┌───────────────┼───────────────┐
            │               │               │
      ┌─────▼─────┐   ┌─────▼─────┐   ┌─────▼─────┐
      │ Customer 1│   │ Customer 2│   │ Customer 3│
      │  (Client) │   │  (Client) │   │  (Client) │
      └─────┬─────┘   └─────┬─────┘   └─────┬─────┘
            │               │               │
      ┌─────▼─────┐   ┌─────▼─────┐   ┌─────▼─────┐
      │ Project A │   │ Project C │   │ Project E │
      │   (Job)   │   │   (Job)   │   │   (Job)   │
      └─────┬─────┘   └─────┬─────┘   └─────┬─────┘
            │               │               │
    ┌───────┼───────┐       │         ┌─────┴─────┐
    │       │       │       │         │           │
┌───▼──┐┌───▼──┐┌───▼──┐┌───▼──┐ ┌────▼───┐ ┌────▼───┐
│Sub-  ││Sub-  ││Sub-  ││ All  │ │Phase 1 │ │Phase 2 │
│Project││Project││Project││Trans │ │(Optional││(Optional│
│ 1    ││ 2    ││ 3    ││      │ │  Sub)  │ │  Sub)  │
└──────┘└──────┘└──────┘└──────┘ └────────┘ └────────┘
```

**KEY INSIGHT:** QBO uses "Sub-customers" and "Sub-projects" for hierarchy. For construction:
- **Customer** = The legal entity paying you (homeowner, GC, developer)
- **Project** = The specific job/contract
- **Sub-project** = Phases or cost divisions within a job (optional)

---

## Step 5: Configure Products and Services for Construction

### Why Products/Services Matter for Job Costing

Every time you create an invoice or bill, you select a Product/Service. This determines:
- Which **income account** is credited (invoices)
- Which **expense account** is debited (bills)
- How transactions are **categorized** in reports

### Essential Service Items to Create

**HOW:**
1. Go to **Settings ⚙️** → **Products and Services**
2. Click **New** → **Service** (for most construction items)
3. Fill in details for each item below

**Income Items (for Invoicing):**

| Name | Income Account | Description |
|------|----------------|-------------|
| Labor - General | 40000 Labor Income | Billable labor hours |
| Labor - Overtime | 40000 Labor Income | OT labor at premium rate |
| Materials | 40100 Materials Income | Pass-through materials |
| Materials - Markup | 40100 Materials Income | Materials with markup |
| Subcontractor | 40200 Subcontractor Income | Sub work billed to customer |
| Equipment Rental | 40300 Equipment Income | Equipment charges to customer |
| Permits & Fees | 40400 Other Income | Reimbursable permits |
| Change Order | 40500 Change Order Income | Approved changes |

**Expense Items (for Bills):**

| Name | Expense Account | Description |
|------|-----------------|-------------|
| Materials Purchase | 50000 Materials Cost | Direct material costs |
| Subcontractor Cost | 50100 Subcontractor Cost | Sub invoices |
| Equipment Rental Exp | 50200 Equipment Cost | Rented equipment |
| Permits Expense | 50300 Permits & Fees | Permit costs |

**WHY MATCHING ITEMS MATTER:**

When you invoice "Materials" at $10,000 and your bill shows "Materials Purchase" at $7,000:
- Report shows Materials Income: $10,000
- Report shows Materials Cost: $7,000
- **Gross Profit on Materials: $3,000 (30% margin)**

Without proper items, everything lumps into "Services" and you lose this visibility.

---

## Step 6: Set Up Billable Expenses

### Enable Billable Expense Tracking

**HOW:**
1. Go to **Settings ⚙️** → **Account and Settings**
2. Select **Expenses** tab
3. Under **Bills and expenses**, turn on:
   - "Show Items table on expense and purchase forms"
   - "Track expenses and items by customer"
   - "Make expenses and items billable"
4. Set default markup percentage (optional, e.g., 15%)
5. Click **Save**, then **Done**

**WHY:**
Billable expenses allow you to:
1. Enter a cost (bill/expense) assigned to a project
2. Mark it as "Billable"
3. When invoicing, add billable items with one click
4. Track which costs have been billed vs. unbilled

**This is crucial for:**
- Material pass-throughs
- Subcontractor invoices
- Permit reimbursements
- Any cost that gets invoiced to the customer

---

## Step 7: Configure Invoice Settings

### Customize Invoice Template for Construction

**HOW:**
1. Go to **Settings ⚙️** → **Custom form styles**
2. Click **New style** → **Invoice**
3. Under **Content**, add:
   - Project/Job name field
   - Service dates
   - Quantity and Rate columns
4. Under **Footer**, add:
   - Payment terms
   - Retention notice (if applicable)

**Sample Retention Notice Text:**
```
Payment terms: Net 30. Retention of 10% will be held until 
project completion and release of lien waivers.
```

---

## Step 8: Initial Data Entry Strategy

### For New Construction Companies

Start fresh! Don't try to import years of old data. Instead:
1. Set a "go-live" date (e.g., start of month/quarter/year)
2. Enter opening balances as of that date
3. Only enter active projects going forward

### For Converting from Another System

**Minimum Data to Migrate:**
- [ ] Chart of Accounts (modified for construction)
- [ ] Customer list with open balances
- [ ] Vendor list with open balances  
- [ ] Active project list with:
  - Contract value
  - Costs incurred to date
  - Billings to date
  - Retention held

**Don't Migrate:**
- Closed projects (unless needed for warranty tracking)
- Transaction-level detail from old system
- Old invoices (enter as opening balances instead)

---

## Verification Checklist

Before proceeding to Job Costing Setup, verify:

- [ ] QBO Plus or Advanced subscription active
- [ ] Projects feature enabled
- [ ] Class tracking enabled  
- [ ] Accrual accounting method set
- [ ] Fiscal year configured
- [ ] Naming convention documented
- [ ] At least one test project created
- [ ] Products/Services for income items created
- [ ] Products/Services for expense items created
- [ ] Billable expense tracking enabled

---

## Common Setup Mistakes

| Mistake | Consequence | Solution |
|---------|-------------|----------|
| Using Classes instead of Projects | Lose project dashboard features | Enable Projects, use Classes for job types |
| Cash basis accounting | Inaccurate job profitability | Switch to accrual |
| No naming convention | Chaos as job count grows | Establish convention NOW |
| Generic products/services | No cost category visibility | Create detailed items |
| Skipping billable expense setup | Manual tracking of pass-throughs | Enable feature |

---

## Next Steps

Your QBO is now configured for construction accounting basics. In the next chapter, we'll build on this foundation with [Job Costing Setup](./tutorials/03-job-costing-setup.md), where you'll learn to track labor, materials, and subcontractor costs by project.

---

*[← Previous: Introduction](./01-introduction.md) | [Next: Job Costing Setup →](./tutorials/03-job-costing-setup.md)*
