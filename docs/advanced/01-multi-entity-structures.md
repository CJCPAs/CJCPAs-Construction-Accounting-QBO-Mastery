# Multi-Entity Structures for Construction Companies

## Overview

Many construction companies operate through multiple legal entities for liability protection, tax optimization, and operational flexibility. This chapter covers common multi-entity structures, their accounting treatment, and how to manage them in QuickBooks Online.

> **Disclaimer**: This guide is for informational purposes only. Entity structuring has significant legal and tax implications. Consult with a qualified attorney and CPA before establishing or modifying entity structures. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Why Multi-Entity Structures](#why-multi-entity-structures)
2. [Common Construction Entity Structures](#common-construction-entity-structures)
3. [Operating Company + Equipment Company](#operating-company--equipment-company)
4. [Intercompany Transactions](#intercompany-transactions)
5. [Management Fees](#management-fees)
6. [QBO Setup for Multiple Entities](#qbo-setup-for-multiple-entities)
7. [Intercompany Accounting in QBO](#intercompany-accounting-in-qbo)
8. [Consolidated Reporting](#consolidated-reporting)
9. [Common Mistakes and Pitfalls](#common-mistakes-and-pitfalls)

---

## Why Multi-Entity Structures

### Reasons Contractors Use Multiple Entities

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    WHY MULTIPLE ENTITIES?                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. LIABILITY PROTECTION                                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Equipment in separate entity = protected from operating lawsuits        │
│  • Each project in separate entity = isolates project risk                 │
│  • Real estate separate = protected from business creditors                │
│                                                                              │
│  2. TAX OPTIMIZATION                                                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Equipment company can use different depreciation strategies             │
│  • Income splitting between entities (with limitations)                    │
│  • Different entity types (S-Corp, LLC, C-Corp) for different purposes    │
│  • State tax planning for multi-state operations                          │
│                                                                              │
│  3. OPERATIONAL FLEXIBILITY                                                  │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Different ownership for different ventures                              │
│  • Easier to bring in partners on specific projects                       │
│  • Cleaner exit strategy (sell one entity, keep others)                   │
│  • Separate bonding for different types of work                           │
│                                                                              │
│  4. REGULATORY COMPLIANCE                                                    │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Different licenses for different trades                                 │
│  • Prevailing wage isolation                                               │
│  • Union vs. non-union operations                                          │
│                                                                              │
│  5. SUCCESSION PLANNING                                                      │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Easier to transfer ownership incrementally                              │
│  • Can gift interests in non-operating entities                           │
│  • Buy-sell agreements more flexible                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Potential Downsides

```
CONSIDERATIONS BEFORE MULTI-ENTITY STRUCTURE:

COMPLEXITY:
• More tax returns to file
• More financial statements to prepare
• More bank accounts to manage
• More compliance requirements

COST:
• Additional accounting fees
• Additional legal fees
• Multiple state registrations
• Potentially multiple insurance policies

ADMINISTRATIVE BURDEN:
• Intercompany agreements required
• Arms-length transactions must be documented
• Separate books and records
• More audit complexity

PIERCING THE CORPORATE VEIL:
• Must maintain separation
• Adequate capitalization required
• Proper formalities must be followed
• Commingling funds = lost protection

THE BOTTOM LINE:
• Small contractors: Usually one entity is sufficient
• Mid-size ($5M+): May benefit from equipment separation
• Larger contractors: Often have multiple entities
• Always: Consult professionals before structuring
```

---

## Common Construction Entity Structures

### Structure 1: Single Entity

```
SINGLE ENTITY STRUCTURE

┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│                         ┌──────────────────────┐                            │
│                         │       OWNER(S)       │                            │
│                         └──────────┬───────────┘                            │
│                                    │ 100%                                   │
│                                    ▼                                        │
│                         ┌──────────────────────┐                            │
│                         │  ABC Construction    │                            │
│                         │       LLC            │                            │
│                         │                      │                            │
│                         │  • Operations        │                            │
│                         │  • Equipment         │                            │
│                         │  • All Projects      │                            │
│                         └──────────────────────┘                            │
│                                                                              │
│  PROS:                           CONS:                                      │
│  • Simple administration         • All eggs in one basket                   │
│  • One tax return               • Equipment exposed to lawsuits            │
│  • One set of books             • Can't optimize for different purposes    │
│  • Lower compliance cost        • Less flexibility                         │
│                                                                              │
│  BEST FOR: Smaller contractors, simple operations                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Structure 2: OpCo + Equipment Co

```
OPERATING COMPANY + EQUIPMENT COMPANY

┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│                         ┌──────────────────────┐                            │
│                         │       OWNER(S)       │                            │
│                         └──────────┬───────────┘                            │
│                           ┌───────┴───────┐                                 │
│                           │               │                                 │
│                     100%  ▼               ▼  100%                           │
│            ┌──────────────────┐    ┌──────────────────┐                    │
│            │ ABC Construction │    │   ABC Equipment  │                    │
│            │      LLC         │    │       LLC        │                    │
│            │   (Operating)    │    │   (Holding)      │                    │
│            │                  │    │                  │                    │
│            │ • All operations │    │ • Owns equipment │                    │
│            │ • Labor          │    │ • Leases to OpCo │                    │
│            │ • Contracts      │    │ • May own shop   │                    │
│            │ • Licenses       │    │                  │                    │
│            └────────┬─────────┘    └────────┬─────────┘                    │
│                     │                       │                               │
│                     │    Equipment Lease    │                               │
│                     └───────────────────────┘                               │
│                                                                              │
│  Equipment Co leases equipment to Operating Co at fair market rates        │
│                                                                              │
│  PROS:                           CONS:                                      │
│  • Equipment protected           • More complexity                         │
│  • Potential tax benefits        • Intercompany agreements needed          │
│  • Clear asset separation        • Must maintain arm's length              │
│  • Flexible depreciation         • Two sets of books                       │
│                                                                              │
│  BEST FOR: Contractors with significant equipment ($500K+)                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Structure 3: Holding Company Structure

```
HOLDING COMPANY STRUCTURE

┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│                         ┌──────────────────────┐                            │
│                         │       OWNER(S)       │                            │
│                         └──────────┬───────────┘                            │
│                                    │ 100%                                   │
│                                    ▼                                        │
│                         ┌──────────────────────┐                            │
│                         │   ABC Holdings LLC   │                            │
│                         │   (Parent/Holding)   │                            │
│                         └──────────┬───────────┘                            │
│                    ┌───────────────┼───────────────┐                        │
│                    │               │               │                        │
│              100%  ▼         100%  ▼         100%  ▼                        │
│     ┌──────────────────┐ ┌──────────────┐ ┌──────────────────┐             │
│     │ABC Construction  │ │ABC Equipment │ │ ABC Real Estate  │             │
│     │     LLC          │ │    LLC       │ │      LLC         │             │
│     │                  │ │              │ │                  │             │
│     │ • Operations     │ │ • Equipment  │ │ • Office/Shop    │             │
│     │ • Labor          │ │ • Vehicles   │ │ • Yard           │             │
│     │ • Projects       │ │              │ │ • Investment RE  │             │
│     └──────────────────┘ └──────────────┘ └──────────────────┘             │
│                                                                              │
│  Intercompany flows:                                                        │
│  • Equipment Co → OpCo: Equipment lease                                    │
│  • Real Estate → OpCo: Facility rent                                       │
│  • Holding → Subs: Management fees (if applicable)                         │
│                                                                              │
│  BEST FOR: Larger contractors with multiple asset types                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Structure 4: Project-Specific Entities

```
PROJECT-SPECIFIC ENTITIES (Joint Ventures / SPEs)

┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│                         ┌──────────────────────┐                            │
│                         │  ABC Construction    │                            │
│                         │       LLC            │                            │
│                         └──────────┬───────────┘                            │
│                    ┌───────────────┼───────────────┐                        │
│                    │               │               │                        │
│               50%  ▼          100% ▼          60%  ▼                        │
│     ┌──────────────────┐ ┌──────────────┐ ┌──────────────────┐             │
│     │ Project Alpha JV │ │Project Beta  │ │ Project Gamma JV │             │
│     │    LLC           │ │    LLC       │ │      LLC         │             │
│     │                  │ │              │ │                  │             │
│     │ JV with XYZ Co   │ │ Wholly owned │ │ JV with 123 Co   │             │
│     │ $50M Hospital    │ │ $15M Office  │ │ $80M Highway     │             │
│     └──────────────────┘ └──────────────┘ └──────────────────┘             │
│                                                                              │
│  WHY PROJECT ENTITIES:                                                      │
│  • Required by owner/contract                                              │
│  • Joint venture with another contractor                                   │
│  • Limit liability to project                                              │
│  • Separate bonding/insurance                                              │
│                                                                              │
│  ACCOUNTING TREATMENT:                                                      │
│  • Wholly owned: Consolidate with parent                                   │
│  • JV (control): Consolidate                                               │
│  • JV (no control): Equity method                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Operating Company + Equipment Company

### Setting Up the Equipment Company

```
EQUIPMENT COMPANY SETUP:

ENTITY FORMATION:
• Typically LLC (flexibility, simplicity)
• Same state as operating company usually
• Separate EIN required
• May need state business registration

INITIAL CAPITALIZATION:
Option 1: Purchase equipment directly
  • Equipment Co buys new equipment
  • Financed or cash purchase

Option 2: Transfer from OpCo
  • Operating Co sells equipment to Equipment Co
  • At fair market value
  • Creates gain/loss in Operating Co
  • Equipment Co may finance purchase

BANK ACCOUNT:
• Separate bank account required
• Equipment Co receives rent payments
• Equipment Co pays its own expenses
• Never comingle with Operating Co

AGREEMENTS NEEDED:
• Operating Agreement (LLC)
• Equipment Lease Agreement
• Possibly promissory note (if seller financing)
```

### Equipment Lease Terms

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    EQUIPMENT LEASE AGREEMENT TERMS                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  LESSOR: ABC Equipment, LLC                                                 │
│  LESSEE: ABC Construction, LLC                                              │
│                                                                              │
│  EQUIPMENT COVERED:                                                          │
│  List all equipment with descriptions and values                            │
│                                                                              │
│  LEASE RATE DETERMINATION:                                                   │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Must be at ARM'S LENGTH (fair market rate)                                │
│                                                                              │
│  Methods to determine rate:                                                 │
│  1. Comparable rental rates (what rental companies charge)                 │
│  2. Cost recovery approach:                                                │
│     (Depreciation + Insurance + Maint + Return on Investment) / Hours      │
│  3. Industry guidelines (AED Green Book, etc.)                             │
│                                                                              │
│  EXAMPLE CALCULATION:                                                        │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Excavator Value: $200,000                                                  │
│  Annual Depreciation: $28,571 (7-year)                                     │
│  Annual Insurance: $3,000                                                   │
│  Annual Maintenance Reserve: $5,000                                         │
│  Target Return (10%): $20,000                                               │
│  Total Annual Cost: $56,571                                                 │
│  Expected Hours: 1,500                                                      │
│  Hourly Rate: $37.71                                                        │
│                                                                              │
│  Compare to rental market: $450-550/day (8 hours) = $56-69/hour            │
│  Internal rate at $37.71 is reasonable (below market)                      │
│                                                                              │
│  PAYMENT TERMS:                                                              │
│  • Monthly lease payment                                                    │
│  • Based on usage or fixed monthly amount                                  │
│  • Net 30 from invoice                                                      │
│                                                                              │
│  MAINTENANCE:                                                                │
│  • Typically Lessee responsible for day-to-day                             │
│  • Major repairs may be Lessor's responsibility                           │
│  • Define clearly in agreement                                              │
│                                                                              │
│  INSURANCE:                                                                  │
│  • Who carries? Usually Lessee (Operating Co)                              │
│  • Lessor listed as loss payee/additional insured                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Equipment Co Financials

```
EQUIPMENT COMPANY FINANCIAL STATEMENTS:

BALANCE SHEET:
─────────────
Assets:
  Cash                          $50,000
  Equipment (net of depr.)     $800,000
  Vehicles (net of depr.)      $150,000
                              ──────────
  Total Assets                 $1,000,000

Liabilities:
  Equipment Loans               $400,000
  Intercompany Payable           $25,000
                              ──────────
  Total Liabilities             $425,000

Equity:
  Member Capital                $500,000
  Retained Earnings              $75,000
                              ──────────
  Total Equity                  $575,000

Total Liab. + Equity          $1,000,000


INCOME STATEMENT:
─────────────────
Revenue:
  Equipment Rental Income       $200,000

Expenses:
  Depreciation                  $120,000
  Insurance                      $15,000
  Repairs & Maintenance          $25,000
  Interest Expense               $20,000
  Property Tax                    $5,000
                              ──────────
  Total Expenses                $185,000

Net Income                       $15,000


KEY POINTS:
• Equipment Co should be profitable (proves arm's length)
• Depreciation is major expense
• Rental income should cover costs + reasonable return
• May show small profit or break-even
```

---

## Intercompany Transactions

### Types of Intercompany Transactions

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COMMON INTERCOMPANY TRANSACTIONS                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. EQUIPMENT RENTALS                                                        │
│     Equipment Co → Operating Co                                             │
│     Rate: Fair market rental rate                                           │
│     Frequency: Monthly                                                       │
│                                                                              │
│  2. FACILITY RENT                                                            │
│     Real Estate Co → Operating Co                                           │
│     Rate: Fair market rent (or triple-net)                                 │
│     Frequency: Monthly                                                       │
│                                                                              │
│  3. MANAGEMENT FEES                                                          │
│     Holding Co → Operating Entities                                         │
│     Rate: Cost-plus or percentage of revenue                               │
│     Frequency: Monthly                                                       │
│                                                                              │
│  4. LOANS / ADVANCES                                                         │
│     Any entity → Any entity                                                 │
│     Rate: At least AFR (Applicable Federal Rate)                           │
│     Terms: Documented promissory note                                       │
│                                                                              │
│  5. COST SHARING                                                             │
│     Shared employees, insurance, etc.                                       │
│     Allocation: By usage, revenue, or other reasonable method              │
│     Frequency: Monthly                                                       │
│                                                                              │
│  6. ASSET SALES/PURCHASES                                                    │
│     Between entities                                                        │
│     Rate: Fair market value                                                 │
│     Documentation: Bill of sale, appraisal if significant                  │
│                                                                              │
│  ⚠️ ALL TRANSACTIONS MUST BE AT ARM'S LENGTH AND DOCUMENTED!              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Arm's Length Requirement

```
ARM'S LENGTH STANDARD:

DEFINITION:
Transactions must be priced as if the parties were unrelated,
dealing at arm's length in the open market.

WHY IT MATTERS:
• IRS can re-characterize transactions if not arm's length
• State tax authorities also scrutinize
• Excessive payments can be disallowed
• May create additional tax liabilities

HOW TO DEMONSTRATE ARM'S LENGTH:

For Equipment Rentals:
• Get quotes from rental companies
• Document comparable rates
• Use industry rate guides
• Update annually

For Real Estate Rent:
• Get market rent comparables
• Consider broker opinion
• Match lease terms to market

For Management Fees:
• Document services provided
• Cost-plus methodology
• Time records if applicable
• Benchmark to third-party rates

For Loans:
• Use at least AFR rate
• Document with promissory note
• Make actual payments
• Treat as real debt

DOCUMENTATION TO MAINTAIN:
• Written agreements
• Market rate support
• Invoices and payments
• Board minutes approving arrangements
```

---

## Management Fees

### Setting Up Management Fees

```
MANAGEMENT FEE ARRANGEMENTS:

WHEN USED:
• Holding company provides services to subsidiaries
• Shared services (accounting, HR, admin)
• Centralized management

FEE STRUCTURES:

1. COST-PLUS:
   Holding Co costs: $200,000
   Plus markup (10%): $20,000
   Total fee: $220,000

   Allocated to subs based on:
   • Revenue percentage
   • Employee count
   • Project count
   • Or other reasonable basis

2. PERCENTAGE OF REVENUE:
   Operating Co revenue: $10,000,000
   Management fee rate: 2%
   Annual fee: $200,000

   Must be reasonable for services provided

3. FLAT FEE:
   Fixed monthly amount
   Based on estimated services
   Adjusted annually

SERVICES THAT SUPPORT MANAGEMENT FEES:
• Executive management and oversight
• Accounting and bookkeeping
• Payroll processing
• HR administration
• IT support
• Insurance administration
• Banking relationship management
• Legal coordination
```

### Management Fee Documentation

```
DOCUMENTING MANAGEMENT FEES:

MANAGEMENT SERVICES AGREEMENT:
────────────────────────────
Must include:
□ Parties (Holding Co and each Operating Entity)
□ Services to be provided (detailed list)
□ Fee calculation method
□ Payment terms
□ Term and termination
□ Allocation methodology (if multiple subs)

SERVICES DESCRIPTION EXAMPLE:
────────────────────────────
ABC Holdings, LLC shall provide the following services
to ABC Construction, LLC:

1. Executive Management
   • Strategic planning and oversight
   • Contract review and approval
   • Banking and surety relationships

2. Financial Services
   • Bookkeeping and accounting
   • Financial statement preparation
   • Tax compliance coordination
   • Budgeting and forecasting

3. Administrative Services
   • Payroll processing
   • HR administration
   • Benefits management
   • Insurance coordination

4. IT Services
   • Computer systems maintenance
   • Software licensing
   • Technical support

ANNUAL DOCUMENTATION:
• Time records (if cost-based)
• Calculation of fee
• Board minutes approving fee
• Invoices and payments
```

---

## QBO Setup for Multiple Entities

### Separate QBO Companies

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QBO MULTI-ENTITY OPTIONS                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  OPTION 1: SEPARATE QBO SUBSCRIPTIONS (RECOMMENDED)                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Each entity has own QBO company file                                    │
│  • Truly separate books                                                     │
│  • Intercompany tracked through Due To/Due From accounts                   │
│  • Can use QBO Accountant to access all companies                          │
│                                                                              │
│  PROS:                           CONS:                                      │
│  • Clean separation             • Multiple subscriptions                    │
│  • Easy to understand           • Must reconcile intercompany              │
│  • Standard approach            • No auto-consolidation                    │
│                                                                              │
│  OPTION 2: CLASS TRACKING (LIMITED USE)                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Single QBO company                                                       │
│  • Use Classes for different "entities"                                    │
│  • Not truly separate (not recommended for legal entities)                 │
│                                                                              │
│  PROS:                           CONS:                                      │
│  • One subscription             • Not really separate books                │
│  • Simpler management           • Tax/legal issues                         │
│                                                                              │
│  ⚠️ RECOMMENDATION: Use separate QBO files for each legal entity          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Chart of Accounts for Intercompany

```
INTERCOMPANY ACCOUNTS (Add to each entity's COA):

IN OPERATING COMPANY:
─────────────────────
Assets:
12800  Due From Equipment Co (Other Current Asset)
12810  Due From Holdings (Other Current Asset)

Liabilities:
23800  Due To Equipment Co (Other Current Liability)
23810  Due To Holdings (Other Current Liability)

Expenses:
60800  Equipment Rental - Related Party
61800  Facility Rent - Related Party
63800  Management Fee - Related Party

IN EQUIPMENT COMPANY:
─────────────────────
Assets:
12800  Due From Operating Co (Other Current Asset)

Liabilities:
23800  Due To Operating Co (Other Current Liability)

Income:
45000  Equipment Rental Income - Related Party

IN HOLDING COMPANY:
───────────────────
Assets:
12800  Due From Operating Co (Other Current Asset)
12810  Due From Equipment Co (Other Current Asset)

Liabilities:
23800  Due To Operating Co (Other Current Liability)
23810  Due To Equipment Co (Other Current Liability)

Income:
45000  Management Fee Income
```

---

## Intercompany Accounting in QBO

### Recording Intercompany Transactions

```
EXAMPLE: MONTHLY EQUIPMENT RENTAL

SCENARIO:
Equipment Co bills Operating Co $15,000 for monthly equipment rental

IN EQUIPMENT COMPANY (Lessor):
─────────────────────────────
Create Invoice:
  Customer: ABC Construction, LLC
  Item: Equipment Rental
  Amount: $15,000
  Account: 45000 Equipment Rental Income

When payment received:
  Record Payment or Journal Entry:
  Dr. 12800 Due From Operating Co    $15,000
    Cr. Accounts Receivable                    $15,000

IN OPERATING COMPANY (Lessee):
──────────────────────────────
Create Bill:
  Vendor: ABC Equipment, LLC
  Item: Equipment Rental
  Amount: $15,000
  Account: 60800 Equipment Rental - Related Party
  Class: [Allocate to jobs or overhead]

When payment made:
  Pay Bill or Journal Entry:
  Dr. Accounts Payable              $15,000
    Cr. 23800 Due To Equipment Co            $15,000

MONTHLY SETTLEMENT:
───────────────────
Operating Co writes check to Equipment Co:

In Operating Co:
  Dr. 23800 Due To Equipment Co    $15,000
    Cr. 10000 Checking                       $15,000

In Equipment Co:
  Dr. 10000 Checking               $15,000
    Cr. 12800 Due From Operating Co          $15,000
```

### Intercompany Reconciliation

```
MONTHLY INTERCOMPANY RECONCILIATION:

Step 1: Run Balance Reports
───────────────────────────
In each company, run Balance Sheet
Note the Due To/Due From balances

Step 2: Compare Balances
────────────────────────
Operating Co "Due To Equipment Co": $15,000
Equipment Co "Due From Operating Co": $15,000
MATCH ✓

If they don't match:
• Review transactions for errors
• Check for timing differences
• Look for missing entries
• Reconcile and adjust

Step 3: Document Reconciliation
───────────────────────────────
Create reconciliation worksheet:

INTERCOMPANY RECONCILIATION
As of: March 31, 2024

Entity A (Operating) owes Entity B (Equipment):
Per Operating Co books:     $15,000
Per Equipment Co books:     $15,000
Difference:                 $0 ✓

Entity A (Operating) owes Entity C (Holdings):
Per Operating Co books:     $8,500
Per Holdings Co books:      $8,500
Difference:                 $0 ✓

Prepared by: _______  Date: _______
Reviewed by: _______  Date: _______
```

---

## Consolidated Reporting

### When Consolidation is Needed

```
CONSOLIDATION REQUIREMENTS:

FOR GAAP FINANCIAL STATEMENTS:
• Parent company must consolidate controlled subsidiaries
• Control typically means > 50% ownership
• Eliminates intercompany transactions
• Shows combined financial position

FOR BONDING:
• Sureties often want consolidated financials
• Shows total financial strength
• May also want separate entity statements

FOR BANKING:
• Banks may require consolidated statements
• Especially if guarantees are cross-company
• Used to assess overall creditworthiness

FOR TAX:
• Separate returns typically required for each entity
• Some elections allow consolidated returns (C-Corps)
• Pass-through entities report on owner returns

FOR INTERNAL MANAGEMENT:
• Consolidated view helpful for decision-making
• See total company performance
• Identify intercompany issues
```

### Manual Consolidation Process

```
CONSOLIDATION STEPS:

Step 1: Gather Financial Statements
───────────────────────────────────
• Balance Sheet for each entity
• Income Statement for each entity
• All as of same date

Step 2: Create Consolidation Worksheet
──────────────────────────────────────
Export to Excel, create columns for:
• Entity A
• Entity B
• Entity C
• Eliminations
• Consolidated

Step 3: Eliminate Intercompany Balances
───────────────────────────────────────
Due To/Due From accounts net to zero:

Operating Co Due To Equipment Co:     ($15,000)
Equipment Co Due From Operating Co:    $15,000
Net:                                        $0

Elimination entry:
Dr. Due From Operating Co (Equip)    $15,000
  Cr. Due To Equipment Co (OpCo)              $15,000

Step 4: Eliminate Intercompany Revenue/Expense
──────────────────────────────────────────────
Equipment Rental Income (Equip Co):    $180,000
Equipment Rental Expense (Op Co):     ($180,000)
Net:                                        $0

Elimination entry:
Dr. Equipment Rental Income          $180,000
  Cr. Equipment Rental Expense                $180,000

Step 5: Eliminate Investment Accounts
─────────────────────────────────────
If parent records investment in subs:
Dr. Subsidiary Equity
  Cr. Investment in Subsidiary

Step 6: Verify and Finalize
───────────────────────────
• Consolidated Balance Sheet balances
• No remaining intercompany balances
• Review for reasonableness
```

---

## Common Mistakes and Pitfalls

### Multi-Entity Mistakes

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COMMON MULTI-ENTITY MISTAKES                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. COMMINGLING FUNDS                                                        │
│     Mistake: Using one bank account for multiple entities                  │
│     Risk: Pierces corporate veil, loses liability protection               │
│     Fix: Separate bank accounts, proper cash management                    │
│                                                                              │
│  2. NO WRITTEN AGREEMENTS                                                    │
│     Mistake: Intercompany transactions without contracts                   │
│     Risk: IRS challenge, not arm's length                                  │
│     Fix: Document all arrangements in writing                              │
│                                                                              │
│  3. ABOVE-MARKET RATES                                                       │
│     Mistake: Equipment rent at $500/day when market is $300/day           │
│     Risk: IRS recharacterization, constructive distribution                │
│     Fix: Document market rates, stay reasonable                            │
│                                                                              │
│  4. BELOW-MARKET RATES                                                       │
│     Mistake: Rent at $100/day when market is $300/day                     │
│     Risk: IRS imputes income, gift tax issues                              │
│     Fix: Use fair market rates                                              │
│                                                                              │
│  5. NOT ACTUALLY MAKING PAYMENTS                                             │
│     Mistake: Recording transactions but never settling                     │
│     Risk: IRS views as sham transaction                                    │
│     Fix: Actually transfer funds, settle monthly                           │
│                                                                              │
│  6. INCONSISTENT TREATMENT                                                   │
│     Mistake: Different rates for same equipment, no pattern               │
│     Risk: Raises audit red flags                                           │
│     Fix: Consistent, documented methodology                                │
│                                                                              │
│  7. INADEQUATE CAPITALIZATION                                                │
│     Mistake: Entity has no real assets or capital                         │
│     Risk: Piercing corporate veil                                          │
│     Fix: Adequate capital for business purpose                             │
│                                                                              │
│  8. IGNORING FORMALITIES                                                     │
│     Mistake: No separate meetings, minutes, resolutions                   │
│     Risk: Entities treated as one (alter ego)                              │
│     Fix: Maintain corporate formalities for each entity                    │
│                                                                              │
│  9. FORGETTING STATE COMPLIANCE                                              │
│     Mistake: Not maintaining state registrations                          │
│     Risk: Lost good standing, penalties                                    │
│     Fix: Annual reports, registered agents, fees                           │
│                                                                              │
│  10. TAX FILING ERRORS                                                       │
│      Mistake: Missing returns, wrong entity type on returns               │
│      Risk: Penalties, interest, audit triggers                             │
│      Fix: Professional tax preparation, timely filing                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MULTI-ENTITY QUICK REFERENCE                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  COMMON STRUCTURES:                                                          │
│  • Single Entity: Simple, all in one                                       │
│  • OpCo + Equipment Co: Protects equipment from operating liability        │
│  • Holding + Subs: Maximum flexibility and protection                      │
│                                                                              │
│  KEY REQUIREMENTS:                                                           │
│  • Separate bank accounts for each entity                                  │
│  • Written intercompany agreements                                         │
│  • Arm's length pricing (fair market rates)                               │
│  • Actual payment of intercompany charges                                  │
│  • Maintain corporate formalities                                          │
│                                                                              │
│  QBO SETUP:                                                                  │
│  • Separate QBO file for each legal entity                                 │
│  • Due To/Due From accounts for intercompany                               │
│  • Monthly intercompany reconciliation                                     │
│                                                                              │
│  DOCUMENTATION NEEDED:                                                       │
│  • Operating agreements / bylaws                                           │
│  • Intercompany service agreements                                         │
│  • Equipment lease agreements                                              │
│  • Promissory notes for loans                                              │
│  • Board minutes/resolutions                                               │
│  • Market rate documentation                                               │
│                                                                              │
│  WARNING SIGNS:                                                              │
│  • One bank account for multiple entities                                  │
│  • No written agreements                                                    │
│  • Prices significantly different from market                              │
│  • No actual cash settlement                                               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With multi-entity structures understood:
- [Equipment Allocation](../tutorials/07-equipment-allocation.md) - Internal equipment costing
- [Bonding Requirements](../compliance/02-bonding-requirements.md) - Surety considerations
- [GAAP Principles](../reference/12-gaap-principles.md) - Consolidation standards

---

*[Back to Main Guide](../../README.md)*
