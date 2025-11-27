# Classes, Locations, and Tracking Protocols for Construction

## Overview

QuickBooks Online provides powerful tracking dimensions that are **essential** for construction accounting. Understanding when and how to use Classes, Locations, and Custom Fields is the difference between having a general ledger and having a true job costing system.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Consult with a qualified CPA before implementing. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Understanding QBO Tracking Dimensions](#understanding-qbo-tracking-dimensions)
2. [Classes: The Foundation of Job Costing](#classes-the-foundation-of-job-costing)
3. [Locations: Multi-Site Operations](#locations-multi-site-operations)
4. [Custom Fields: Extending Your Tracking](#custom-fields-extending-your-tracking)
5. [Project Tracking (QBO Plus/Advanced)](#project-tracking-qbo-plusadvanced)
6. [Tracking Protocol Decision Framework](#tracking-protocol-decision-framework)
7. [Implementation Walkthroughs](#implementation-walkthroughs)
8. [Best Practices and Common Mistakes](#best-practices-and-common-mistakes)

---

## Understanding QBO Tracking Dimensions

### What Are Tracking Dimensions?

Tracking dimensions allow you to categorize transactions beyond the basic chart of accounts. Think of them as additional "tags" you can apply to transactions.

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                        TRANSACTION ANATOMY                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   BILL #4521 - ABC Lumber Supply                                            │
│   ┌─────────────────────────────────────────────────────────────────────┐   │
│   │  LINE 1: 2x4 Framing Lumber                   $2,450.00              │   │
│   │  ├── Account: 50100 - Materials                                      │   │
│   │  ├── Class: Smith Residence (JOB)                                    │   │
│   │  ├── Location: North Region                                          │   │
│   │  └── Project: Smith Residence                                        │   │
│   ├─────────────────────────────────────────────────────────────────────┤   │
│   │  LINE 2: Trim Package                         $1,800.00              │   │
│   │  ├── Account: 50100 - Materials                                      │   │
│   │  ├── Class: Johnson Remodel (JOB)                                    │   │
│   │  ├── Location: North Region                                          │   │
│   │  └── Project: Johnson Remodel                                        │   │
│   └─────────────────────────────────────────────────────────────────────┘   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Available Tracking Options

| Feature | QBO Simple Start | QBO Essentials | QBO Plus | QBO Advanced |
|---------|-----------------|----------------|----------|--------------|
| Classes | ❌ | ❌ | ✅ | ✅ |
| Locations | ❌ | ❌ | ✅ | ✅ |
| Projects | ❌ | ❌ | ✅ | ✅ (Enhanced) |
| Custom Fields | Limited | Limited | 3 fields | Unlimited |
| Tags | ✅ | ✅ | ✅ | ✅ |

### Why This Matters for Construction

```
┌─────────────────────────────────────────────────────────────────────────────┐
│              WITHOUT TRACKING          │          WITH TRACKING             │
├────────────────────────────────────────┼────────────────────────────────────┤
│                                        │                                    │
│  P&L Shows:                            │  P&L by CLASS Shows:               │
│  ─────────                             │  ────────────────                  │
│  Revenue: $1,500,000                   │  Smith Residence:                  │
│  Materials: $400,000                   │    Revenue: $450,000               │
│  Labor: $350,000                       │    Materials: $120,000             │
│  Subs: $250,000                        │    Labor: $105,000                 │
│  ─────────────                         │    Gross Profit: $225,000 (50%)    │
│  Gross Profit: $500,000                │                                    │
│                                        │  Johnson Remodel:                  │
│  ❓ Which jobs are profitable?         │    Revenue: $280,000               │
│  ❓ Where are we losing money?         │    Materials: $95,000              │
│  ❓ What's our margin by job type?     │    Labor: $78,000                  │
│                                        │    Gross Profit: $107,000 (38%)    │
│                                        │                                    │
│                                        │  ✅ Clear job profitability        │
│                                        │  ✅ Identifies problem jobs        │
│                                        │  ✅ Supports WIP calculations      │
│                                        │                                    │
└────────────────────────────────────────┴────────────────────────────────────┘
```

---

## Classes: The Foundation of Job Costing

### What Are Classes?

Classes are the primary tracking dimension in QBO. For contractors, **Classes = Jobs/Projects**.

### WHY Classes Are Critical (GAAP Connection)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    GAAP PRINCIPLE: MATCHING                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Under GAAP and ASC 606, revenue must be matched with the costs incurred    │
│  to generate that revenue. For construction companies:                       │
│                                                                              │
│  • Revenue is recognized on a PROJECT-BY-PROJECT basis                      │
│  • Costs must be tracked at the PROJECT level to calculate:                 │
│    - Percentage of completion                                                │
│    - Over/under billing                                                      │
│    - Job profitability                                                       │
│                                                                              │
│  Classes provide the PROJECT-LEVEL tracking required for proper revenue     │
│  recognition and cost matching.                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Enabling Classes in QBO

**Step-by-Step:**

1. **Navigate to Settings**
   ```
   ⚙️ Gear Icon → Account and Settings
   ```

2. **Go to Advanced Tab**
   ```
   Account and Settings → Advanced → Categories
   ```

3. **Enable Class Tracking**
   ```
   Toggle ON: "Track classes"
   Optional: "Warn me when a transaction isn't assigned a class"
   ```

4. **Configure Class Assignment**
   ```
   Select: "One to each row in transaction"
   (This allows different lines to have different classes)
   ```

5. **Save and Close**

### Class Structure for Construction

#### Option 1: Flat Structure (Small Contractors)

```
CLASSES (All at same level):
├── 2024-001 Smith Residence
├── 2024-002 Johnson Kitchen Remodel
├── 2024-003 ABC Commercial Buildout
├── 2024-004 City Park Pavilion
├── OVERHEAD (Non-job expenses)
└── EQUIPMENT (Equipment costs to allocate)
```

**Best For:**
- Companies with < 20 active jobs
- Simple project structures
- Easy reporting needs

#### Option 2: Hierarchical Structure (Mid-Size Contractors)

```
CLASSES (Parent/Child):
├── ACTIVE JOBS
│   ├── RESIDENTIAL
│   │   ├── 2024-001 Smith Residence
│   │   ├── 2024-002 Johnson Remodel
│   │   └── 2024-003 Brown Addition
│   ├── COMMERCIAL
│   │   ├── 2024-010 ABC Office Buildout
│   │   └── 2024-011 XYZ Restaurant
│   └── GOVERNMENT
│       └── 2024-020 City Park Pavilion
├── COMPLETED JOBS
│   └── (Move jobs here when complete)
├── OVERHEAD
│   ├── General & Administrative
│   ├── Marketing
│   └── Shop/Yard
└── EQUIPMENT
    ├── Equipment Pool
    └── Small Tools
```

**Best For:**
- Companies with 20-100 jobs per year
- Multiple project types
- Need for rollup reporting

#### Option 3: Phase-Based Structure (Large Projects)

```
CLASSES:
├── 2024-001 Smith Residence
│   ├── 2024-001-PRE Preconstruction
│   ├── 2024-001-SITE Site Work
│   ├── 2024-001-FND Foundation
│   ├── 2024-001-FRM Framing
│   ├── 2024-001-MEP Mechanical/Electrical/Plumbing
│   ├── 2024-001-FIN Finishes
│   ├── 2024-001-CO Change Orders
│   └── 2024-001-CLOSE Closeout
├── 2024-002 Johnson Remodel
│   └── (Same phase structure)
└── OVERHEAD
```

**Best For:**
- Large projects ($500K+)
- Phased billing requirements
- Detailed cost tracking needs

### Creating Classes: Step-by-Step

**Method 1: Manual Creation**

1. Navigate to Lists
   ```
   ⚙️ Gear Icon → All Lists → Classes
   ```

2. Click "New"

3. Enter Class Details:
   ```
   Name: 2024-001 Smith Residence
   Parent Class: ACTIVE JOBS > RESIDENTIAL (if using hierarchy)
   ```

4. Save

**Method 2: Import via CSV**

1. Prepare CSV file:
   ```csv
   Name,Parent
   "2024-001 Smith Residence","ACTIVE JOBS:RESIDENTIAL"
   "2024-002 Johnson Remodel","ACTIVE JOBS:RESIDENTIAL"
   "2024-010 ABC Buildout","ACTIVE JOBS:COMMERCIAL"
   ```

2. Navigate to Import:
   ```
   ⚙️ Gear Icon → Import Data → Classes
   ```

3. Upload and map columns

4. Import

### Class Naming Conventions

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    RECOMMENDED NAMING CONVENTION                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Format: YYYY-NNN Description                                                │
│                                                                              │
│  Examples:                                                                   │
│  • 2024-001 Smith Residence                                                  │
│  • 2024-002 Johnson Kitchen Remodel                                          │
│  • 2024-010 ABC Corp Office TI                                               │
│                                                                              │
│  WHY THIS FORMAT:                                                            │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │  YYYY    → Year started (helps with archiving)                         │  │
│  │  NNN     → Sequential number (ensures uniqueness)                      │  │
│  │  Desc    → Human-readable name (for quick identification)              │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
│                                                                              │
│  ALTERNATIVE FORMATS:                                                        │
│  • Customer-based: SMITH-2024-01                                             │
│  • Address-based: 123-MAIN-ST                                                │
│  • Contract-based: CONTRACT-45678                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Assigning Classes to Transactions

**On Bills (AP):**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  BILL #4521 - ABC Lumber Supply                        [Save] [Cancel]      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Vendor: ABC Lumber Supply           Terms: Net 30                           │
│  Bill Date: 03/15/2024               Due Date: 04/14/2024                    │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │ Category Details                                                    │    │
│  ├──────────────┬──────────────────────┬──────────────┬───────────────┤    │
│  │ CATEGORY     │ DESCRIPTION          │ AMOUNT       │ CLASS         │    │
│  ├──────────────┼──────────────────────┼──────────────┼───────────────┤    │
│  │ 50100 Matls  │ 2x4 Framing Lumber   │ $2,450.00    │ 2024-001 ▼   │    │
│  │ 50100 Matls  │ Trim Package         │ $1,800.00    │ 2024-002 ▼   │    │
│  │ 50100 Matls  │ Misc Hardware        │ $245.00      │ 2024-001 ▼   │    │
│  └──────────────┴──────────────────────┴──────────────┴───────────────┘    │
│                                                                              │
│  ⚠️ IMPORTANT: Each line can have a DIFFERENT class!                        │
│     This allows split billing across multiple jobs.                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

**On Invoices (AR):**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  INVOICE #1001 - Smith Family Trust                    [Save] [Send]        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Customer: Smith Family Trust        Terms: Net 30                           │
│  Invoice Date: 03/20/2024            Due Date: 04/19/2024                    │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │ Product/Service Details                                             │    │
│  ├────────────────────┬──────────────────┬───────────────┬────────────┤    │
│  │ PRODUCT/SERVICE    │ DESCRIPTION      │ AMOUNT        │ CLASS      │    │
│  ├────────────────────┼──────────────────┼───────────────┼────────────┤    │
│  │ Progress Billing   │ Draw #3          │ $45,000.00    │ 2024-001 ▼│    │
│  │ Retainage Held     │ 10% Retainage    │ ($4,500.00)   │ 2024-001 ▼│    │
│  └────────────────────┴──────────────────┴───────────────┴────────────┘    │
│                                                                              │
│  Total: $40,500.00                                                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Locations: Multi-Site Operations

### What Are Locations?

Locations are a second tracking dimension, independent of Classes. They're typically used for:
- Geographic regions
- Branch offices
- Divisions
- Profit centers

### When to Use Locations (vs. Classes)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LOCATION VS CLASS DECISION                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Use CLASSES for: JOBS/PROJECTS                                              │
│  Use LOCATIONS for: ORGANIZATIONAL STRUCTURE                                 │
│                                                                              │
│  Example: Multi-Branch Contractor                                            │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │                                                                        │  │
│  │  LOCATIONS              CLASSES                                        │  │
│  │  ─────────              ───────                                        │  │
│  │  • North Region         • 2024-001 Smith Residence (North)             │  │
│  │  • South Region         • 2024-002 Johnson Remodel (North)             │  │
│  │  • West Region          • 2024-010 ABC Buildout (South)                │  │
│  │  • Corporate            • 2024-011 XYZ Restaurant (West)               │  │
│  │                                                                        │  │
│  │  This allows reports like:                                             │  │
│  │  • P&L by Job (Class)                                                  │  │
│  │  • P&L by Region (Location)                                            │  │
│  │  • P&L by Job WITHIN a Region (both)                                   │  │
│  │                                                                        │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Location Use Cases for Contractors

| Use Case | Location Structure |
|----------|-------------------|
| Multi-State Operations | States (TX, OK, NM) |
| Regional Branches | North, South, East, West |
| Service Lines | New Construction, Renovations, Service |
| Divisions | Residential, Commercial, Industrial |
| Cost Centers | Field Operations, Shop, Office |

### Enabling Locations

**Step-by-Step:**

1. Navigate to Settings
   ```
   ⚙️ Gear Icon → Account and Settings
   ```

2. Go to Advanced Tab
   ```
   Account and Settings → Advanced → Categories
   ```

3. Enable Location Tracking
   ```
   Toggle ON: "Track locations"
   Label locations as: [Locations/Divisions/Regions - choose your label]
   ```

4. Configure Assignment
   ```
   Select: "One to each row in transaction"
   ```

5. Save

### Location Structure Example

```
LOCATIONS:
├── NORTH REGION
│   ├── Dallas Office
│   └── Fort Worth Office
├── SOUTH REGION
│   ├── Houston Office
│   └── San Antonio Office
├── CORPORATE
│   ├── Main Office
│   └── Equipment Yard
└── UNASSIGNED
    └── (Catch-all for misc)
```

---

## Custom Fields: Extending Your Tracking

### What Are Custom Fields?

Custom fields add additional data points to transactions and lists. QBO Plus allows 3 custom fields; Advanced allows unlimited.

### Custom Field Ideas for Construction

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    RECOMMENDED CUSTOM FIELDS                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ON CUSTOMERS:                                                               │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │  • Project Manager: [Dropdown: PM Names]                               │  │
│  │  • Job Type: [Dropdown: Residential/Commercial/Industrial]             │  │
│  │  • Contract Type: [Dropdown: Fixed Price/T&M/Cost Plus]                │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
│                                                                              │
│  ON VENDORS:                                                                 │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │  • Trade: [Dropdown: Electrical/Plumbing/HVAC/etc]                     │  │
│  │  • Insurance Expiration: [Date]                                        │  │
│  │  • Bonding Limit: [Text]                                               │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
│                                                                              │
│  ON INVOICES:                                                                │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │  • Pay App Number: [Text: "Pay App #3"]                                │  │
│  │  • AIA Document: [Dropdown: G702/G703]                                 │  │
│  │  • Certified: [Yes/No]                                                 │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Creating Custom Fields

**Step-by-Step:**

1. Navigate to Custom Fields
   ```
   ⚙️ Gear Icon → Custom Fields (or Lists → Custom Fields)
   ```

2. Click "Add Field"

3. Configure Field:
   ```
   Name: Project Manager
   Data Type: Dropdown
   Categories: Customer
   Values: John Smith, Jane Doe, Mike Johnson
   ```

4. Set Visibility:
   ```
   ☑️ Show on forms (if applicable)
   ☑️ Show in reports
   ```

5. Save

---

## Project Tracking (QBO Plus/Advanced)

### Projects vs. Classes

QBO Plus and Advanced have a dedicated "Projects" feature. Here's how it compares:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PROJECTS VS CLASSES                                       │
├──────────────────────────────┬──────────────────────────────────────────────┤
│         CLASSES              │              PROJECTS                         │
├──────────────────────────────┼──────────────────────────────────────────────┤
│ • Tracking dimension only    │ • Full project management                    │
│ • Manual reporting           │ • Built-in project dashboard                 │
│ • No time tracking link      │ • Integrates with time tracking              │
│ • No estimates link          │ • Links to estimates                         │
│ • Works on all transaction   │ • Limited transaction types                  │
│   types                      │                                               │
│ • More flexible              │ • More structured                            │
│ • Better for complex WIP     │ • Better for simple job tracking             │
├──────────────────────────────┴──────────────────────────────────────────────┤
│                                                                              │
│  RECOMMENDATION: Use BOTH                                                    │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Create a PROJECT for each job (get dashboard, time tracking)             │
│  • Create a matching CLASS for each job (get flexible reporting, WIP)       │
│  • Keep naming consistent: "2024-001 Smith Residence" for both              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Creating a Project

**Step-by-Step:**

1. Navigate to Projects
   ```
   Left Menu → Projects
   ```

2. Click "New Project"

3. Enter Project Details:
   ```
   Project Name: 2024-001 Smith Residence
   Customer: Smith Family Trust
   ```

4. Add Project Details:
   ```
   Notes: Single-family residence, 3,200 sq ft
   Start Date: 03/01/2024
   End Date: 09/30/2024
   ```

5. Save

### Linking Projects to Transactions

When creating a transaction, select both:
- **Customer**: Smith Family Trust
- **Project**: 2024-001 Smith Residence

This links the transaction to the project dashboard.

---

## Tracking Protocol Decision Framework

### Decision Tree

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TRACKING DECISION FRAMEWORK                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  START: What do you need to track?                                           │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │                                                                      │    │
│  │  JOBS/PROJECTS?                                                      │    │
│  │       │                                                              │    │
│  │       ├── YES → Use CLASSES (Primary job tracking)                   │    │
│  │       │         └── Also use PROJECTS if QBO Plus/Advanced           │    │
│  │       │              (for dashboard/time tracking)                   │    │
│  │       │                                                              │    │
│  │  ORGANIZATIONAL STRUCTURE?                                           │    │
│  │       │                                                              │    │
│  │       ├── Multi-location/region? → Use LOCATIONS                     │    │
│  │       ├── Multiple divisions? → Use LOCATIONS                        │    │
│  │       └── Single location? → Skip LOCATIONS                          │    │
│  │                                                                      │    │
│  │  ADDITIONAL DATA POINTS?                                             │    │
│  │       │                                                              │    │
│  │       ├── Project Manager? → CUSTOM FIELD                            │    │
│  │       ├── Job Type? → CUSTOM FIELD (or Class hierarchy)              │    │
│  │       ├── Insurance expiration? → CUSTOM FIELD                       │    │
│  │       └── Informal grouping? → TAGS                                  │    │
│  │                                                                      │    │
│  └─────────────────────────────────────────────────────────────────────┘    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Recommended Configurations by Company Size

#### Small Contractor (< 20 jobs/year, 1 location)

```
TRACKING SETUP:
├── Classes: YES (flat list of jobs + OVERHEAD)
├── Locations: NO
├── Projects: Optional
└── Custom Fields: Optional

Example Classes:
- 2024-001 Smith Residence
- 2024-002 Johnson Remodel
- OVERHEAD
```

#### Mid-Size Contractor (20-100 jobs/year, multiple locations)

```
TRACKING SETUP:
├── Classes: YES (hierarchical by job type)
├── Locations: YES (by region/branch)
├── Projects: YES (linked to classes)
└── Custom Fields: YES (PM, job type, contract type)

Example:
- Classes: ACTIVE > RESIDENTIAL > 2024-001 Smith
- Locations: North Region > Dallas Office
- Project: 2024-001 Smith Residence
```

#### Large Contractor (100+ jobs/year, complex structure)

```
TRACKING SETUP:
├── Classes: YES (hierarchical with phases)
├── Locations: YES (by division/region)
├── Projects: YES (with full time tracking)
└── Custom Fields: YES (multiple)

Example:
- Classes: 2024-001 Smith > 2024-001-FND Foundation
- Locations: Residential Division > North Region
- Project: 2024-001 Smith Residence (with time entries)
```

---

## Implementation Walkthroughs

### Walkthrough 1: Setting Up a New Job

**Scenario:** You've won a new project "2024-015 Martinez Custom Home" and need to set up tracking.

**Step 1: Create the Customer (if new)**

```
1. Go to: Sales → Customers → New Customer
2. Enter:
   - Display Name: Martinez Family
   - Company: Martinez Custom Home LLC
   - Address: 456 New Build Lane
   - Payment Terms: Net 30
3. Save
```

**Step 2: Create the Class**

```
1. Go to: ⚙️ → All Lists → Classes
2. Click: New
3. Enter:
   - Name: 2024-015 Martinez Custom Home
   - Parent Class: ACTIVE JOBS > RESIDENTIAL
4. Save
```

**Step 3: Create the Project (QBO Plus/Advanced)**

```
1. Go to: Left Menu → Projects
2. Click: New Project
3. Enter:
   - Project Name: 2024-015 Martinez Custom Home
   - Customer: Martinez Family
   - Notes: 4,500 sq ft custom home
4. Save
```

**Step 4: Create Sub-Customer for Job (Alternative to Project)**

```
1. Go to: Sales → Customers
2. Select: Martinez Family
3. Click: Add sub-customer
4. Enter:
   - Display Name: 2024-015 Martinez Custom Home
   - ☑️ Bill with parent: NO (if separate billing)
5. Save
```

### Walkthrough 2: Recording a Multi-Job Bill

**Scenario:** You receive a bill from ABC Lumber for materials going to three different jobs.

**Step 1: Create the Bill**

```
1. Go to: + New → Bill
2. Select Vendor: ABC Lumber Supply
3. Enter Header:
   - Bill Date: 03/15/2024
   - Due Date: 04/14/2024
   - Bill No: 78451
```

**Step 2: Enter Line Items with Classes**

```
Line 1:
- Category: 50100 - Materials
- Description: 2x4 Studs (Smith job)
- Amount: $2,450.00
- Class: 2024-001 Smith Residence

Line 2:
- Category: 50100 - Materials
- Description: Trim Package (Johnson job)
- Amount: $1,800.00
- Class: 2024-002 Johnson Remodel

Line 3:
- Category: 50100 - Materials
- Description: Deck Lumber (Martinez job)
- Amount: $3,200.00
- Class: 2024-015 Martinez Custom Home
```

**Step 3: Verify and Save**

```
Total: $7,450.00
- Smith: $2,450.00
- Johnson: $1,800.00
- Martinez: $3,200.00

Click: Save and Close
```

### Walkthrough 3: Running a P&L by Job

**Step 1: Navigate to Reports**

```
1. Go to: Left Menu → Reports
2. Search: "Profit and Loss by Class"
3. Click: Profit and Loss by Class
```

**Step 2: Customize Report**

```
1. Click: Customize
2. Set Date Range: This Fiscal Year
3. Rows/Columns:
   - Show: Active Classes only
   - Sort by: Total
4. Click: Run Report
```

**Step 3: Interpret Results**

```
                          Smith      Johnson    Martinez    OVERHEAD    TOTAL
                        Residence    Remodel     Custom
─────────────────────────────────────────────────────────────────────────────
Revenue                 $450,000    $280,000    $125,000           -   $855,000
  Contract Revenue       450,000     280,000     125,000           -    855,000

Cost of Revenue
  Materials              120,000      95,000      45,000           -    260,000
  Labor                  105,000      78,000      32,000           -    215,000
  Subcontractors          75,000      55,000      25,000           -    155,000
  Equipment               15,000       8,000       5,000           -     28,000
─────────────────────────────────────────────────────────────────────────────
Gross Profit            $135,000     $44,000     $18,000           -   $197,000
Gross Margin              30.0%       15.7%       14.4%            -      23.0%
```

---

## Best Practices and Common Mistakes

### Best Practices

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         BEST PRACTICES                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. CONSISTENCY IS KEY                                                       │
│     • Use same class naming convention for all jobs                         │
│     • Assign class on EVERY transaction (enable warnings)                   │
│     • Review unclassified transactions weekly                               │
│                                                                              │
│  2. KEEP IT SIMPLE                                                           │
│     • Start with flat class structure, add hierarchy later                  │
│     • Don't create more tracking than you'll use                            │
│     • Focus on what helps decision-making                                   │
│                                                                              │
│  3. ARCHIVE COMPLETED JOBS                                                   │
│     • Move completed jobs to "COMPLETED" parent class                       │
│     • Don't delete classes (breaks historical reporting)                    │
│     • Make inactive after final retention release                           │
│                                                                              │
│  4. SEPARATE OVERHEAD                                                        │
│     • Always have an OVERHEAD class for non-job expenses                    │
│     • Review overhead regularly for misclassified items                     │
│     • Allocate equipment costs monthly                                      │
│                                                                              │
│  5. TRAIN YOUR TEAM                                                          │
│     • Create class selection guide for common scenarios                     │
│     • Review new employee entries for first month                           │
│     • Run "Unclassified" report weekly                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Mistakes

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         COMMON MISTAKES                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ❌ MISTAKE 1: Not assigning classes to ALL transactions                    │
│     Fix: Enable "Warn me when transaction isn't assigned a class"           │
│     Run weekly report: Profit and Loss by Class (look for unclassified)     │
│                                                                              │
│  ❌ MISTAKE 2: Using classes for non-job tracking                           │
│     Fix: Use classes ONLY for jobs; use locations/custom fields for rest   │
│     Classes should = Jobs for clean job costing reports                     │
│                                                                              │
│  ❌ MISTAKE 3: Deleting classes instead of archiving                        │
│     Fix: Make class inactive or move to "COMPLETED" parent                  │
│     Deleting removes class from historical transactions                     │
│                                                                              │
│  ❌ MISTAKE 4: Inconsistent naming conventions                              │
│     Fix: Establish naming standard: "YYYY-NNN Description"                  │
│     Document in procedures manual                                           │
│                                                                              │
│  ❌ MISTAKE 5: Not using parent classes for rollup reporting                │
│     Fix: Structure classes hierarchically by job type                       │
│     Enables summary reports by category (Residential, Commercial)           │
│                                                                              │
│  ❌ MISTAKE 6: Confusing Projects with Classes                              │
│     Fix: Use BOTH - Projects for dashboard, Classes for reporting           │
│     Keep names identical for easy cross-reference                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick Reference Card

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TRACKING QUICK REFERENCE                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  CLASSES                                                                     │
│  • Purpose: Job/Project tracking                                             │
│  • Enable: Settings → Advanced → Track classes                              │
│  • Location: ⚙️ → All Lists → Classes                                       │
│  • Use: On EVERY transaction line                                           │
│                                                                              │
│  LOCATIONS                                                                   │
│  • Purpose: Branch/Region/Division tracking                                  │
│  • Enable: Settings → Advanced → Track locations                            │
│  • Location: ⚙️ → All Lists → Locations                                     │
│  • Use: If multi-site operations                                            │
│                                                                              │
│  PROJECTS                                                                    │
│  • Purpose: Project management dashboard                                     │
│  • Available: QBO Plus and Advanced                                          │
│  • Location: Left Menu → Projects                                            │
│  • Use: With Classes for full tracking                                       │
│                                                                              │
│  CUSTOM FIELDS                                                               │
│  • Purpose: Additional data points                                           │
│  • Available: 3 (Plus), Unlimited (Advanced)                                 │
│  • Location: ⚙️ → Custom Fields                                             │
│  • Use: PM, job type, contract type, etc.                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

Now that you understand tracking protocols, continue to:
- [Company Settings](./02-company-settings.md) - Configure QBO for construction
- [Job Costing Setup](../tutorials/03-job-costing-setup.md) - Implement full job costing
- [Chart of Accounts](../templates/09-chart-of-accounts.md) - Set up your COA

---

*[Back to Main Guide](../../README.md)*
