# Equipment and Materials: Capitalization vs. Expensing

## Overview

Understanding when to capitalize versus expense equipment and materials is crucial for accurate construction accounting. This guide covers the decision framework, IRS rules, GAAP requirements, and practical QBO implementation.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Tax rules change frequently and vary by situation. Consult with a qualified CPA before making capitalization decisions. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Capitalize vs. Expense: The Basics](#capitalize-vs-expense-the-basics)
2. [Capitalization Thresholds](#capitalization-thresholds)
3. [Equipment Capitalization](#equipment-capitalization)
4. [Materials Handling](#materials-handling)
5. [IRS Safe Harbors](#irs-safe-harbors)
6. [Recording in QBO](#recording-in-qbo)
7. [Depreciation Methods](#depreciation-methods)
8. [Job Cost Allocation](#job-cost-allocation)
9. [Best Practices and Common Mistakes](#best-practices-and-common-mistakes)

---

## Capitalize vs. Expense: The Basics

### What's the Difference?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CAPITALIZE VS EXPENSE                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  EXPENSE (Deduct Immediately)                                                │
│  ────────────────────────────                                                │
│  • Full cost reduces income in current period                               │
│  • Affects P&L immediately                                                   │
│  • Appropriate for:                                                          │
│    - Small tools and supplies                                               │
│    - Items with short useful life (< 1 year)                                │
│    - Routine repairs and maintenance                                        │
│    - Items below capitalization threshold                                   │
│                                                                              │
│  Example: $500 drill purchased in March                                      │
│  Result: $500 expense in March, reduces March profit by $500                │
│                                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  CAPITALIZE (Add to Balance Sheet)                                           │
│  ─────────────────────────────────                                           │
│  • Cost recorded as asset                                                    │
│  • Depreciated over useful life                                              │
│  • Appropriate for:                                                          │
│    - Major equipment                                                         │
│    - Vehicles                                                                │
│    - Items with useful life > 1 year                                        │
│    - Items above capitalization threshold                                   │
│                                                                              │
│  Example: $75,000 backhoe purchased in March                                │
│  Result: $75,000 asset on balance sheet                                     │
│          Depreciated over 5-7 years                                         │
│          ~$10,700-$15,000/year expense                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Why It Matters

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    IMPACT OF DECISION                                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  FINANCIAL STATEMENT IMPACT:                                                 │
│  ───────────────────────────                                                 │
│                                                                              │
│  $50,000 Equipment Purchase                                                  │
│                                                                              │
│  IF EXPENSED:                        │  IF CAPITALIZED (5-yr):              │
│  ─────────────                       │  ─────────────────────               │
│  Year 1 P&L: ($50,000)               │  Year 1 P&L: ($10,000)               │
│  Year 2 P&L: $0                      │  Year 2 P&L: ($10,000)               │
│  Year 3 P&L: $0                      │  Year 3 P&L: ($10,000)               │
│  Year 4 P&L: $0                      │  Year 4 P&L: ($10,000)               │
│  Year 5 P&L: $0                      │  Year 5 P&L: ($10,000)               │
│  ──────────────────────              │  ──────────────────────              │
│  Total: ($50,000)                    │  Total: ($50,000)                    │
│                                      │                                       │
│  Balance Sheet: No asset             │  Balance Sheet: Asset (declining)    │
│                                                                              │
│  TAX IMPACT:                                                                 │
│  ───────────                                                                 │
│  Expensing provides LARGER tax deduction in Year 1                          │
│  Capitalizing spreads deduction over multiple years                         │
│                                                                              │
│  BONDING IMPACT:                                                             │
│  ──────────────                                                              │
│  Capitalizing shows HIGHER net income in Year 1                             │
│  Bonding companies prefer consistent, profitable financials                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Capitalization Thresholds

### Setting Your Threshold

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CAPITALIZATION THRESHOLD POLICY                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT IS A THRESHOLD?                                                        │
│  ────────────────────                                                        │
│  A dollar amount above which items must be capitalized.                     │
│  Items below threshold are expensed.                                        │
│                                                                              │
│  COMMON THRESHOLDS:                                                          │
│  ───────────────────                                                         │
│  Small Contractor:    $500 - $1,000                                         │
│  Mid-Size Contractor: $1,000 - $2,500                                       │
│  Large Contractor:    $2,500 - $5,000                                       │
│                                                                              │
│  IRS DE MINIMIS SAFE HARBOR:                                                 │
│  ────────────────────────────                                                │
│  • With audited financials: Up to $5,000 per item                           │
│  • Without audited financials: Up to $2,500 per item                        │
│  • Must have written policy                                                  │
│  • Must apply consistently                                                   │
│                                                                              │
│  EXAMPLE POLICY:                                                             │
│  ─────────────────────────────────────────────────────────────────────────  │
│  "All equipment, tools, and furniture with a cost of $2,500 or more         │
│   and a useful life greater than one year shall be capitalized.             │
│   Items below $2,500 or with useful life of one year or less shall          │
│   be expensed in the period of purchase."                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Threshold Decision Framework

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CAPITALIZE OR EXPENSE DECISION TREE                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│                      ┌───────────────┐                                       │
│                      │  Purchase or  │                                       │
│                      │  Expenditure  │                                       │
│                      └───────┬───────┘                                       │
│                              │                                               │
│                              ▼                                               │
│                 ┌────────────────────────┐                                   │
│                 │  Useful life > 1 year? │                                   │
│                 └───────────┬────────────┘                                   │
│                     │               │                                        │
│                   YES              NO                                        │
│                     │               │                                        │
│                     ▼               ▼                                        │
│         ┌────────────────┐   ┌─────────────┐                                │
│         │ Cost > your    │   │  EXPENSE    │                                │
│         │ threshold?     │   └─────────────┘                                │
│         └───────┬────────┘                                                  │
│             │         │                                                      │
│           YES        NO                                                      │
│             │         │                                                      │
│             ▼         ▼                                                      │
│     ┌─────────────┐  ┌─────────────┐                                        │
│     │ CAPITALIZE  │  │  EXPENSE    │                                        │
│     │ as Fixed    │  │  (De minimis│                                        │
│     │ Asset       │  │  safe harbor│                                        │
│     └─────────────┘  └─────────────┘                                        │
│                                                                              │
│  ADDITIONAL CONSIDERATIONS:                                                  │
│  • Land is ALWAYS capitalized (never depreciated)                           │
│  • Land improvements are capitalized and depreciated                        │
│  • Vehicles almost always exceed threshold                                  │
│  • Repairs/maintenance generally expensed                                   │
│  • Improvements/betterments generally capitalized                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Equipment Capitalization

### Types of Construction Equipment

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    EQUIPMENT CLASSIFICATION                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  HEAVY EQUIPMENT (Almost always capitalize)                                  │
│  ────────────────────────────────────────                                    │
│  • Excavators, backhoes, loaders                                            │
│  • Cranes, forklifts                                                        │
│  • Bulldozers, graders                                                       │
│  • Concrete pumps, mixers                                                   │
│  • Scaffolding systems                                                       │
│  Typical cost: $25,000 - $500,000+                                          │
│  Useful life: 5-15 years                                                    │
│                                                                              │
│  VEHICLES (Almost always capitalize)                                         │
│  ──────────────────────────────────                                          │
│  • Trucks, vans                                                              │
│  • Trailers                                                                  │
│  • Service vehicles                                                          │
│  Typical cost: $25,000 - $100,000+                                          │
│  Useful life: 5-7 years                                                     │
│                                                                              │
│  POWER TOOLS (May capitalize or expense)                                     │
│  ───────────────────────────────────────                                     │
│  • Table saws, miter saws                                                   │
│  • Compressors                                                               │
│  • Generators                                                                │
│  • Laser levels, total stations                                             │
│  Typical cost: $500 - $5,000                                                │
│  Decision: Compare to threshold                                              │
│                                                                              │
│  HAND TOOLS (Usually expense)                                                │
│  ────────────────────────────                                                │
│  • Drills, drivers, saws                                                    │
│  • Hand tools, levels                                                        │
│  • Safety equipment                                                          │
│  Typical cost: Under $500 each                                              │
│  Decision: Expense as small tools                                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### What to Include in Capitalized Cost

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CAPITALIZED EQUIPMENT COST                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  INCLUDE IN CAPITALIZED COST:                                                │
│  ─────────────────────────────                                               │
│  ✅ Purchase price                                                          │
│  ✅ Sales tax                                                                │
│  ✅ Delivery/freight                                                        │
│  ✅ Installation                                                             │
│  ✅ Initial setup/testing                                                   │
│  ✅ Modifications needed to put in service                                  │
│  ✅ Permits/fees required for purchase                                      │
│                                                                              │
│  DO NOT INCLUDE (Expense separately):                                        │
│  ─────────────────────────────────────                                       │
│  ❌ Extended warranties (may capitalize separately)                         │
│  ❌ Training                                                                 │
│  ❌ Insurance                                                                │
│  ❌ Fuel/operating costs                                                    │
│  ❌ Regular maintenance                                                      │
│                                                                              │
│  EXAMPLE:                                                                    │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Backhoe Purchase:                                                           │
│  Purchase price:              $65,000                                       │
│  Sales tax (8%):               $5,200                                       │
│  Delivery:                       $800                                       │
│  Quick-attach bucket:          $2,500                                       │
│  ─────────────────────────────────────                                       │
│  TOTAL CAPITALIZED COST:      $73,500                                       │
│                                                                              │
│  Expenses (not capitalized):                                                │
│  Extended warranty:            $1,500 (expense or amortize)                 │
│  Operator training:              $500 (expense)                             │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Materials Handling

### Job Materials vs. Inventory

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MATERIALS ACCOUNTING                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  OPTION 1: DIRECT JOB COSTING (Most Contractors)                            │
│  ────────────────────────────────────────────────                            │
│  Materials purchased for specific job → Expense to job immediately          │
│                                                                              │
│  Example: Buy $5,000 lumber for Smith job                                   │
│  Entry: Debit Materials Expense (50100) / Class: Smith                      │
│         Credit Accounts Payable                                              │
│                                                                              │
│  Pros: Simple, matches cost to job, no inventory tracking                   │
│  Cons: May overstate expenses if material not yet used                      │
│                                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  OPTION 2: INVENTORY SYSTEM                                                  │
│  ────────────────────────────                                                │
│  Materials purchased → Inventory asset → Expense when used                  │
│                                                                              │
│  Example: Buy $5,000 lumber into inventory                                  │
│  Entry 1: Debit Inventory Asset / Credit AP                                 │
│  Entry 2: When used on job: Debit Material Expense / Credit Inventory       │
│                                                                              │
│  Pros: Accurate WIP, tracks material on hand                                │
│  Cons: More complex, requires inventory management                          │
│                                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  RECOMMENDATION FOR MOST CONTRACTORS:                                        │
│  Use Direct Job Costing unless you:                                          │
│  • Maintain significant material inventory                                   │
│  • Need precise WIP calculations                                            │
│  • Have staff to manage inventory system                                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Work in Progress Materials

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    WIP MATERIALS CONSIDERATION                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ISSUE: Materials on job site not yet installed                             │
│                                                                              │
│  Scenario:                                                                   │
│  • $50,000 of windows delivered to job site                                 │
│  • Windows sitting on site, not yet installed                               │
│  • Job is 40% complete                                                       │
│                                                                              │
│  GAAP TREATMENT:                                                             │
│  Materials stored at job site ARE typically included in cost to date        │
│  for percentage-of-completion if:                                            │
│  • Purchased specifically for this job                                      │
│  • Delivered to job site or specifically stored                             │
│  • Non-returnable or would be costly to return                              │
│                                                                              │
│  PRACTICAL APPROACH FOR QBO:                                                 │
│  ─────────────────────────────────────────────────────────────────────────  │
│  1. Expense materials to job when bill received                             │
│  2. For WIP calculation, materials ON SITE count as cost incurred           │
│  3. Track "materials in place" vs "materials on hand" if needed             │
│                                                                              │
│  Exception: Significant stored materials may need separate tracking         │
│  for accurate WIP (especially on large commercial projects)                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## IRS Safe Harbors

### De Minimis Safe Harbor

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DE MINIMIS SAFE HARBOR ELECTION                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT IT IS:                                                                 │
│  ───────────                                                                 │
│  IRS allows immediate expensing of items below certain thresholds           │
│  instead of capitalizing and depreciating.                                  │
│                                                                              │
│  THRESHOLDS:                                                                 │
│  ───────────                                                                 │
│  • WITH audited or reviewed financials: $5,000 per item/invoice             │
│  • WITHOUT audited financials: $2,500 per item/invoice                      │
│                                                                              │
│  REQUIREMENTS:                                                               │
│  ─────────────                                                               │
│  1. Written accounting policy in place at beginning of year                 │
│  2. Policy states threshold amount                                          │
│  3. Apply policy consistently to all items                                  │
│  4. Treat same for books and tax                                            │
│                                                                              │
│  HOW TO ELECT:                                                               │
│  ─────────────                                                               │
│  Attach statement to tax return:                                            │
│  "Under Treas. Reg. 1.263(a)-1(f), [Company Name] elects to apply          │
│   the de minimis safe harbor for the taxable year [Year]."                 │
│                                                                              │
│  EXAMPLE POLICY:                                                             │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  ABC Construction, LLC                                                       │
│  Capitalization Policy                                                       │
│  Effective: January 1, 2024                                                  │
│                                                                              │
│  "ABC Construction, LLC has established a policy to expense amounts         │
│   paid for the acquisition or production of property when the amount        │
│   paid per item does not exceed $2,500. This policy applies to all          │
│   property including materials, supplies, equipment, and tools.             │
│   Property with a cost exceeding $2,500 and a useful life of more           │
│   than 12 months shall be capitalized and depreciated."                     │
│                                                                              │
│  Approved: _____________ Date: __________                                   │
│            (Owner/Officer)                                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Section 179 Deduction

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SECTION 179 DEDUCTION                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT IT IS:                                                                 │
│  ───────────                                                                 │
│  Allows immediate deduction of cost of qualifying property instead          │
│  of depreciating over multiple years.                                       │
│                                                                              │
│  2024 LIMITS (verify annually):                                              │
│  ──────────────────────────────                                              │
│  • Maximum deduction: $1,220,000                                            │
│  • Phase-out starts at: $3,050,000 in purchases                             │
│  • Must have taxable income (can't create loss)                             │
│                                                                              │
│  QUALIFYING PROPERTY:                                                        │
│  ────────────────────                                                        │
│  ✅ Tangible personal property (equipment, vehicles, furniture)             │
│  ✅ Certain computer software                                               │
│  ✅ Qualified improvement property                                          │
│  ❌ Land                                                                     │
│  ❌ Buildings (most)                                                         │
│  ❌ Inventory                                                                │
│                                                                              │
│  CONSTRUCTION EXAMPLE:                                                       │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  ABC Construction buys:                                                      │
│  Backhoe:      $75,000                                                      │
│  Truck:        $55,000                                                      │
│  Trailer:      $15,000                                                      │
│  Total:       $145,000                                                      │
│                                                                              │
│  Without 179: Depreciate over 5-7 years                                     │
│  With 179: Deduct full $145,000 in year 1 (if income allows)                │
│                                                                              │
│  ⚠️ BOOK VS TAX:                                                            │
│  For financial statements, you may still need to depreciate                 │
│  (especially if bonding or banking requires GAAP)                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Bonus Depreciation

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BONUS DEPRECIATION                                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT IT IS:                                                                 │
│  ───────────                                                                 │
│  Additional first-year depreciation deduction on qualifying property.       │
│                                                                              │
│  CURRENT RATES (phasing down):                                               │
│  ─────────────────────────────                                               │
│  2023: 80%                                                                   │
│  2024: 60%                                                                   │
│  2025: 40%                                                                   │
│  2026: 20%                                                                   │
│  2027+: 0% (unless Congress extends)                                        │
│                                                                              │
│  KEY DIFFERENCES FROM 179:                                                   │
│  ──────────────────────────                                                  │
│  • No income limitation (can create tax loss)                               │
│  • No dollar cap                                                             │
│  • Applies automatically (can elect out)                                    │
│  • Can be used on new AND used property                                     │
│                                                                              │
│  EXAMPLE (2024):                                                             │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Equipment cost: $100,000                                                    │
│  5-year property, half-year convention                                       │
│                                                                              │
│  Bonus depreciation (60%):   $60,000                                        │
│  Regular depreciation:       $8,000 (20% of $40,000)                        │
│  Year 1 total deduction:     $68,000                                        │
│                                                                              │
│  Remaining to depreciate:    $32,000 over years 2-6                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Recording in QBO

### Capitalizing Equipment

**Step-by-Step:**

```
1. Create Fixed Asset Account (if needed)
   Navigation: ⚙️ → Chart of Accounts → New

   Account Type: Fixed Assets
   Detail Type: Machinery & Equipment
   Name: 15100 - Construction Equipment
   
   (Also create accumulated depreciation account)
   Account Type: Fixed Assets
   Detail Type: Accumulated Depreciation
   Name: 15150 - Accum Depr - Equipment

2. Record Equipment Purchase

   OPTION A: Paid by Check
   Navigation: + New → Check
   
   Pay to: Equipment Vendor
   Account: 15100 Construction Equipment
   Amount: $73,500 (full capitalized cost)
   Memo: 2024 CAT 420 Backhoe SN: ABC123
   
   OPTION B: Financed/Note
   Navigation: + New → Journal Entry
   
   Debit: 15100 Construction Equipment  $73,500
   Credit: 27000 Equipment Loans Payable $73,500
   Memo: 2024 CAT 420 Backhoe, financed through CAT Financial

3. Set Up Depreciation
   Navigation: Use recurring journal entry or manual monthly entry
   
   Debit: 60400 Depreciation Expense   $1,225
   Credit: 15150 Accum Depr Equipment  $1,225
   Memo: Monthly depreciation - 2024 Backhoe
```

### Recording Small Tools (Expense)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  BILL - Tool Supplier                                     [Save] [Cancel]   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Vendor: ABC Tool Supply                                                     │
│  Bill date: 03/15/2024           Due date: 04/14/2024                       │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │ Category Details                                                    │    │
│  ├─────────────────┬─────────────────────────────┬────────────────────┤    │
│  │ ACCOUNT         │ DESCRIPTION                 │ AMOUNT             │    │
│  ├─────────────────┼─────────────────────────────┼────────────────────┤    │
│  │ 50600 Small     │ Dewalt 20V Drill Kit       │ $299.00            │    │
│  │ Tools & Supplies│                             │                    │    │
│  │ Class: OVERHEAD │                             │                    │    │
│  ├─────────────────┼─────────────────────────────┼────────────────────┤    │
│  │ 50600 Small     │ Circular Saw               │ $189.00            │    │
│  │ Tools & Supplies│                             │                    │    │
│  │ Class: OVERHEAD │                             │                    │    │
│  ├─────────────────┴─────────────────────────────┼────────────────────┤    │
│  │                                       TOTAL:  │ $488.00            │    │
│  └───────────────────────────────────────────────┴────────────────────┘    │
│                                                                              │
│  Note: Items under $2,500 threshold - expensed per de minimis policy       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Fixed Asset Sub-Register

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FIXED ASSET TRACKING                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  QBO doesn't have built-in fixed asset management.                          │
│  Options for tracking details:                                               │
│                                                                              │
│  OPTION 1: SPREADSHEET SUB-REGISTER                                          │
│  ───────────────────────────────────                                         │
│  Maintain Excel/Sheets with:                                                │
│  • Asset description                                                         │
│  • Serial number                                                             │
│  • Purchase date                                                             │
│  • Cost                                                                      │
│  • Depreciation method                                                       │
│  • Useful life                                                               │
│  • Monthly depreciation                                                      │
│  • Accumulated depreciation                                                  │
│  • Net book value                                                            │
│                                                                              │
│  OPTION 2: QBO ADVANCED CUSTOM FIELDS                                        │
│  ─────────────────────────────────────                                       │
│  Add custom fields to transactions:                                          │
│  • Asset ID                                                                  │
│  • Serial Number                                                             │
│                                                                              │
│  OPTION 3: THIRD-PARTY APP                                                   │
│  ────────────────────────                                                    │
│  • Asset Panda                                                               │
│  • Asset Tiger                                                               │
│  • Integrate with QBO                                                        │
│                                                                              │
│  Sample spreadsheet columns:                                                 │
│  ─────────────────────────────────────────────────────────────────────────  │
│  ID    │Description        │Purchase│ Cost   │Life│Mo Depr│Accum   │NBV    │
│  ──────┼───────────────────┼────────┼────────┼────┼───────┼────────┼───────│
│  EQ001 │2024 CAT 420       │01/15/24│$73,500 │84  │$875   │$2,625  │$70,875│
│  EQ002 │2022 Ford F-250    │03/10/22│$55,000 │60  │$917   │$22,008 │$32,992│
│  EQ003 │Trailer 20ft       │06/01/23│$8,500  │84  │$101   │$909    │$7,591 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Depreciation Methods

### Common Methods for Construction

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DEPRECIATION METHODS                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  STRAIGHT-LINE (Most Common for Books)                                       │
│  ─────────────────────────────────────                                       │
│  Formula: (Cost - Salvage) / Useful Life                                    │
│                                                                              │
│  Example: $73,500 backhoe, 7-year life, $5,000 salvage                      │
│  Annual: ($73,500 - $5,000) / 7 = $9,786/year                               │
│  Monthly: $815.50                                                            │
│                                                                              │
│  MACRS (Required for Tax)                                                    │
│  ────────────────────────                                                    │
│  Modified Accelerated Cost Recovery System                                   │
│  IRS specified rates by asset class                                          │
│                                                                              │
│  5-Year Property (vehicles, computers, equipment):                           │
│  Year 1: 20% (half-year convention)                                         │
│  Year 2: 32%                                                                 │
│  Year 3: 19.2%                                                               │
│  Year 4: 11.52%                                                              │
│  Year 5: 11.52%                                                              │
│  Year 6: 5.76%                                                               │
│                                                                              │
│  7-Year Property (furniture, some equipment):                                │
│  Year 1: 14.29%                                                              │
│  Year 2: 24.49%                                                              │
│  Year 3: 17.49%                                                              │
│  Year 4: 12.49%                                                              │
│  Year 5: 8.93%                                                               │
│  Year 6: 8.92%                                                               │
│  Year 7: 8.93%                                                               │
│  Year 8: 4.46%                                                               │
│                                                                              │
│  BOOK VS TAX DEPRECIATION:                                                   │
│  ─────────────────────────                                                   │
│  Many contractors use:                                                       │
│  • Straight-line for financial statements (bonding, banking)                │
│  • MACRS + 179/Bonus for tax returns                                        │
│  This creates book-tax differences requiring tracking                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Recording Monthly Depreciation

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  JOURNAL ENTRY - Monthly Depreciation                                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Date: 03/31/2024              Entry No: JE-2024-0045                       │
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │ ACCOUNT                        │ DEBIT      │ CREDIT     │ CLASS   │    │
│  ├────────────────────────────────┼────────────┼────────────┼─────────┤    │
│  │ 60400 Depreciation Expense     │ $2,500.00  │            │ EQUIP   │    │
│  │ 15150 Accum Depr - Equipment   │            │ $2,500.00  │         │    │
│  └────────────────────────────────┴────────────┴────────────┴─────────┘    │
│                                                                              │
│  Memo: March 2024 depreciation - all equipment per schedule                 │
│                                                                              │
│  Attachments: [March Depreciation Schedule.xlsx]                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

TIP: Create as RECURRING JOURNAL ENTRY
Navigation: ⚙️ → Recurring Transactions → New → Journal Entry
Set to Monthly, automatic posting
```

---

## Job Cost Allocation

### Allocating Equipment to Jobs

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    EQUIPMENT COST ALLOCATION TO JOBS                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  CHALLENGE:                                                                  │
│  You own equipment that works on multiple jobs.                             │
│  How do you charge jobs for equipment use?                                  │
│                                                                              │
│  METHOD 1: INTERNAL EQUIPMENT RATE                                           │
│  ──────────────────────────────────                                          │
│  Calculate hourly/daily rate and charge jobs                                │
│                                                                              │
│  Rate Calculation:                                                           │
│  Annual ownership cost: $15,000 (depr + insurance + major repairs)          │
│  Annual operating cost: $8,000 (fuel + maintenance)                         │
│  Total annual cost: $23,000                                                  │
│  Estimated annual hours: 1,200                                               │
│  Internal rate: $23,000 / 1,200 = $19.17/hour                               │
│                                                                              │
│  Job Usage: Backhoe on Smith job for 40 hours                               │
│  Charge to job: 40 × $19.17 = $766.80                                       │
│                                                                              │
│  Journal Entry:                                                              │
│  Debit: 50300 Equipment Costs    $766.80  Class: Smith                      │
│  Credit: 50300 Equipment Costs   $766.80  Class: EQUIPMENT                  │
│  (Or use Equipment Revenue account for credit)                              │
│                                                                              │
│  METHOD 2: PRO-RATA BY REVENUE                                               │
│  ─────────────────────────────                                               │
│  Allocate depreciation based on job revenue percentage                      │
│                                                                              │
│  Total depreciation: $2,500/month                                           │
│  Smith revenue: 40% of month                                                │
│  Smith charge: $1,000                                                        │
│                                                                              │
│  METHOD 3: ACTUAL TRACKING                                                   │
│  ──────────────────────────                                                  │
│  Track actual fuel, maintenance by job                                       │
│  Depreciation allocated by hours                                             │
│                                                                              │
│  See: [Equipment Allocation Tutorial](../tutorials/07-equipment-allocation.md)
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Best Practices and Common Mistakes

### Best Practices

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CAPITALIZATION BEST PRACTICES                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. DOCUMENT YOUR POLICY                                                     │
│     • Written capitalization threshold policy                               │
│     • Signed by owner/officer                                               │
│     • Dated at beginning of tax year                                        │
│     • Apply consistently                                                     │
│                                                                              │
│  2. TRACK ASSETS SYSTEMATICALLY                                              │
│     • Maintain fixed asset register (spreadsheet or software)               │
│     • Record serial numbers, locations                                      │
│     • Update for additions and disposals                                    │
│                                                                              │
│  3. RECONCILE REGULARLY                                                      │
│     • Monthly: Depreciation posting                                          │
│     • Annually: Physical inventory of assets                                │
│     • Match register to QBO balance                                         │
│                                                                              │
│  4. CONSIDER BOOK VS TAX                                                     │
│     • Understand when they differ                                           │
│     • Track differences for tax prep                                        │
│     • Bonding/banking may require GAAP books                                │
│                                                                              │
│  5. INCLUDE ALL COSTS                                                        │
│     • Don't forget sales tax, freight, installation                         │
│     • Document cost components                                              │
│                                                                              │
│  6. REVIEW ANNUALLY                                                          │
│     • Check threshold appropriateness                                       │
│     • Update for inflation                                                  │
│     • Verify IRS limits                                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Mistakes

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COMMON MISTAKES TO AVOID                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ❌ MISTAKE 1: Inconsistent threshold application                           │
│     Example: Capitalize $1,500 saw but expense $2,000 tool                  │
│     Fix: Apply threshold consistently to all purchases                      │
│                                                                              │
│  ❌ MISTAKE 2: No written policy                                            │
│     Risk: Can't use de minimis safe harbor                                 │
│     Fix: Create and date policy before year-end                            │
│                                                                              │
│  ❌ MISTAKE 3: Forgetting sales tax/freight in cost                        │
│     Example: Capitalize $50,000 but ignore $4,500 sales tax                │
│     Fix: Include ALL costs to acquire and put in service                   │
│                                                                              │
│  ❌ MISTAKE 4: Not tracking asset details                                   │
│     Problem: Can't identify assets for sale, insurance, or disposal        │
│     Fix: Maintain register with descriptions, serial numbers               │
│                                                                              │
│  ❌ MISTAKE 5: Mixing repair and improvement                                │
│     Example: Engine rebuild expensed when it should be capitalized         │
│     Rule: Repairs (maintain) = expense; Improvements (better) = capitalize │
│                                                                              │
│  ❌ MISTAKE 6: Forgetting depreciation entries                              │
│     Problem: Assets on books but no depreciation recorded                  │
│     Fix: Set up recurring monthly depreciation entry                       │
│                                                                              │
│  ❌ MISTAKE 7: Not disposing sold/scrapped assets                           │
│     Problem: Balance sheet shows assets you no longer own                  │
│     Fix: Record disposal entry removing cost and accumulated depr          │
│                                                                              │
│  ❌ MISTAKE 8: Expensing everything for "tax benefit"                       │
│     Problem: Understates assets, overstates expenses                       │
│     Risk: Bonding/banking issues, audit problems                           │
│     Fix: Follow proper capitalization rules                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CAPITALIZATION QUICK REFERENCE                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  THRESHOLD (without audited financials): $2,500                             │
│                                                                              │
│  CAPITALIZE IF:                                                              │
│  • Cost > $2,500 AND                                                        │
│  • Useful life > 1 year                                                     │
│                                                                              │
│  EXPENSE IF:                                                                 │
│  • Cost ≤ $2,500 OR                                                         │
│  • Useful life ≤ 1 year                                                     │
│                                                                              │
│  INCLUDE IN CAPITALIZED COST:                                                │
│  ✅ Purchase price                                                          │
│  ✅ Sales tax                                                                │
│  ✅ Delivery/freight                                                        │
│  ✅ Installation                                                             │
│                                                                              │
│  TAX ACCELERATION OPTIONS:                                                   │
│  • Section 179: Immediate deduction up to $1,220,000 (2024)                │
│  • Bonus Depreciation: 60% first year (2024)                               │
│                                                                              │
│  TYPICAL DEPRECIATION LIVES:                                                 │
│  • Vehicles: 5 years                                                        │
│  • Equipment: 5-7 years                                                     │
│  • Buildings: 39 years (commercial)                                         │
│                                                                              │
│  REQUIRED DOCUMENTATION:                                                     │
│  • Written capitalization policy                                            │
│  • Fixed asset register                                                     │
│  • Monthly depreciation schedule                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With capitalization understanding:
- [Equipment Allocation Tutorial](../tutorials/07-equipment-allocation.md) - Job cost allocation
- [Chart of Accounts](../templates/09-chart-of-accounts.md) - Asset account setup
- [GAAP Principles](../reference/12-gaap-principles.md) - Accounting standards

---

*[Back to Main Guide](../../README.md)*
