# Sales and Use Tax for Construction Contractors

## Overview

Construction sales and use tax is one of the most complex areas of tax compliance. Rules vary dramatically by state, and the distinction between "real property contractors" and "retailers" can mean the difference between owing tax and not.

> **Disclaimer**: This guide is for informational purposes only. Sales and use tax laws are extremely complex and vary by state, county, and municipality. Consult with a qualified tax professional before making tax decisions. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Understanding Construction Sales Tax](#understanding-construction-sales-tax)
2. [Contractor Classification](#contractor-classification)
3. [Taxability by Transaction Type](#taxability-by-transaction-type)
4. [Use Tax Obligations](#use-tax-obligations)
5. [Exemption Certificates](#exemption-certificates)
6. [State-by-State Overview](#state-by-state-overview)
7. [QBO Setup for Sales Tax](#qbo-setup-for-sales-tax)
8. [Common Compliance Mistakes](#common-compliance-mistakes)
9. [Audit Preparation](#audit-preparation)

---

## Understanding Construction Sales Tax

### The Fundamental Question

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    THE CONSTRUCTION TAX QUESTION                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  In most states, the key question is:                                       │
│                                                                              │
│  "Is the contractor the CONSUMER of materials,                              │
│   or a RESELLER of materials?"                                              │
│                                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  IF CONSUMER (most common for construction):                                │
│  • Contractor pays sales tax when BUYING materials                          │
│  • Does NOT charge customer sales tax on contract                          │
│  • Materials become part of real property                                   │
│                                                                              │
│  IF RESELLER:                                                               │
│  • Contractor buys materials TAX-FREE (resale certificate)                 │
│  • CHARGES customer sales tax on materials sold                            │
│  • Typically applies to retail-type sales, not installation                │
│                                                                              │
│  THE COMPLICATION:                                                          │
│  Some states treat contractors as resellers                                 │
│  Some have different rules for different contract types                     │
│  Some tax labor, some don't                                                 │
│  Some have special rules for certain industries                             │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Real Property vs. Tangible Personal Property

```
REAL PROPERTY IMPROVEMENT:
─────────────────────────
Materials permanently attached to land or buildings
• Contractor is typically CONSUMER of materials
• Pays tax on purchases
• Does not charge tax on contract (in most states)

Examples:
• Installing a roof
• Building an addition
• Pouring a foundation
• Installing HVAC system
• Permanent electrical work

TANGIBLE PERSONAL PROPERTY:
───────────────────────────
Items that remain movable/removable
• Contractor may be RESELLER
• May charge tax on these items
• Or may be subject to other rules

Examples:
• Appliances (often taxable sale)
• Furniture
• Window treatments (varies)
• Portable equipment

THE GRAY AREAS:
───────────────
• Carpeting (attached but removable)
• Light fixtures (depends on type)
• Kitchen cabinets (permanently installed?)
• Security systems (depends on components)
```

---

## Contractor Classification

### Types of Contractor Tax Treatment

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CONTRACTOR TAX CLASSIFICATIONS                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TYPE 1: REAL PROPERTY CONTRACTOR (Most Common)                             │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Treatment: Consumer of materials                                            │
│  Tax on purchases: YES                                                       │
│  Tax on billings: NO (or limited)                                           │
│  Common in: Most states for most contractors                                │
│                                                                              │
│  TYPE 2: RETAILER-CONTRACTOR                                                 │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Treatment: Reseller of materials                                           │
│  Tax on purchases: NO (resale certificate)                                  │
│  Tax on billings: YES (on materials, possibly labor)                        │
│  Common in: Arizona, New Mexico, Hawaii (on all)                            │
│                                                                              │
│  TYPE 3: HYBRID                                                              │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Treatment: Depends on contract type                                        │
│  Lump sum contracts: Consumer treatment                                     │
│  T&M contracts: May have different treatment                                │
│  Common in: Several states have this distinction                            │
│                                                                              │
│  TYPE 4: EXEMPT WORK                                                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Treatment: Work for exempt entities                                        │
│  Government projects: Often exempt                                          │
│  Non-profit: May be exempt                                                  │
│  Must have proper exemption certificates                                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Determining Your Classification

```
CLASSIFICATION FLOWCHART:

START: What type of work are you doing?
       │
       ├─► Installing materials into real property?
       │   │
       │   └─► YES: Are you in AZ, NM, HI, or similar?
       │         │
       │         ├─► YES: You're likely a retailer, charge tax
       │         │
       │         └─► NO: You're likely a consumer, pay tax on purchases
       │
       ├─► Selling items separately (not installed)?
       │   │
       │   └─► YES: You're a retailer for those items, charge tax
       │
       ├─► Repair vs. new construction?
       │   │
       │   └─► CHECK: Some states have different rules for repair
       │
       └─► Working for government/exempt entity?
           │
           └─► CHECK: Different rules may apply

⚠️ CRITICAL: This is simplified! Verify with your state's tax authority
              or a qualified tax professional.
```

---

## Taxability by Transaction Type

### Common Scenarios

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TAXABILITY BY SCENARIO                                    │
│                    (Typical State - Verify Your State!)                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  SCENARIO                         │ PAY TAX ON │ CHARGE TAX │               │
│                                   │ PURCHASES  │ TO CUSTOMER│               │
│  ─────────────────────────────────┼────────────┼────────────┤               │
│  New construction - lump sum      │ YES        │ NO         │ Typical       │
│  New construction - T&M           │ YES*       │ NO*        │ Varies        │
│  Remodel - lump sum               │ YES        │ NO         │ Typical       │
│  Remodel - T&M                    │ YES*       │ NO*        │ Varies        │
│  Repair only (no materials)       │ N/A        │ NO*        │ Usually no    │
│  Repair with materials            │ YES        │ NO         │ Typical       │
│  Maintenance contract             │ YES        │ MAYBE      │ Varies        │
│  Equipment installation (perm.)   │ YES        │ NO         │ Typical       │
│  Appliance sale + delivery        │ RESALE     │ YES        │ Retail sale   │
│  Appliance sale + installation    │ YES/RESALE │ VARIES     │ Complex!      │
│  Fabrication (custom millwork)    │ YES*       │ NO*        │ Varies        │
│  Prefab items installed           │ YES        │ NO         │ Typical       │
│                                                                              │
│  * Rules vary significantly by state                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### The Labor Question

```
IS LABOR TAXABLE?

Most states: Labor for real property improvement is NOT taxable
Some states: Tax applies to TOTAL contract (materials + labor)

TAX-ON-TOTAL STATES (as of 2024):
• Arizona - Tax on gross receipts (TPT)
• Hawaii - GET on gross receipts
• New Mexico - Gross receipts tax
• Washington - Some B&O tax implications

LABOR-EXEMPT STATES (most others):
• Texas - Labor exempt, materials taxed at purchase
• California - Labor exempt, tax on materials at purchase
• Florida - Labor exempt for real property
• (Most states follow this pattern)

⚠️ EVEN IN LABOR-EXEMPT STATES:
• Fabrication labor may be taxable
• Repair labor (vs. improvement) may differ
• Some services ancillary to construction may be taxable
```

---

## Use Tax Obligations

### What is Use Tax?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    USE TAX EXPLAINED                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  DEFINITION:                                                                 │
│  A tax on the USE of tangible personal property when sales tax wasn't      │
│  paid at the time of purchase.                                              │
│                                                                              │
│  WHEN IT APPLIES:                                                            │
│  • Purchases from out-of-state vendors (no sales tax collected)            │
│  • Items withdrawn from inventory for business use                         │
│  • Items purchased tax-free but used in a taxable manner                   │
│  • Internet purchases where no sales tax was charged                       │
│                                                                              │
│  RATE:                                                                       │
│  Usually the same as sales tax rate in your location                        │
│                                                                              │
│  EXAMPLE:                                                                    │
│  ─────────────────────────────────────────────────────────────────────────  │
│  You buy specialty materials online from out-of-state vendor                │
│  Purchase price: $5,000                                                     │
│  Sales tax charged: $0 (vendor has no nexus in your state)                 │
│  Your state sales/use tax rate: 8.25%                                       │
│  Use tax you owe: $5,000 × 8.25% = $412.50                                 │
│                                                                              │
│  YOU are responsible for remitting this to your state!                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Tracking and Remitting Use Tax

```
USE TAX TRACKING PROCESS:

Step 1: Identify Use Tax Purchases
─────────────────────────────────
Review all purchases for:
• No sales tax on invoice
• Out-of-state vendor
• Items that will be used in your state

Step 2: Calculate Use Tax Due
─────────────────────────────
Purchase Amount × State/Local Rate = Use Tax

Step 3: Record in QBO
──────────────────────
Option A: Add to purchase
  Debit: Expense/Asset Account (full amount)
  Debit: Use Tax Expense (or track as liability)
  Credit: Cash/AP

Option B: Accrue monthly
  Debit: Use Tax Expense
  Credit: Use Tax Payable

Step 4: Remit to State
──────────────────────
• File with sales tax return (most common)
• Or separate use tax return
• Frequency depends on state requirements
```

### QBO Use Tax Recording

```
RECORDING USE TAX IN QBO:

Method 1: At Time of Purchase
─────────────────────────────
When entering bill from out-of-state vendor:

Line 1: Materials                    $5,000.00
Line 2: Use Tax Payable               ($412.50)   ← Negative line
Line 3: Use Tax Expense (or COGS)      $412.50

Net AP: $5,000.00 to vendor
Use tax accrued: $412.50

Method 2: Monthly Journal Entry
───────────────────────────────
At month-end, review all out-of-state/untaxed purchases:

Dr. Use Tax Expense (or COGS)         $XXX.XX
  Cr. Use Tax Payable                          $XXX.XX

Memo: Use tax accrual - January 2024

Method 3: QBO Automated Sales Tax
─────────────────────────────────
If using QBO's automated sales tax:
• Some versions can track use tax
• Check Settings → Sales Tax → Use Tax
• May auto-calculate on qualifying purchases
```

---

## Exemption Certificates

### Types of Exemption Certificates

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    EXEMPTION CERTIFICATE TYPES                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. RESALE CERTIFICATE                                                       │
│     Purpose: Buy items tax-free that you will resell                        │
│     Use: Only for items actually resold                                     │
│     Risk: Using for items you consume = tax + penalties                     │
│     Form: State-specific (some accept multi-state forms)                    │
│                                                                              │
│  2. DIRECT PAY PERMIT                                                        │
│     Purpose: Pay tax directly to state, not to vendor                       │
│     Use: Large purchasers who self-report                                   │
│     Benefit: Better control, fewer vendor issues                            │
│     Availability: Not all states offer this                                 │
│                                                                              │
│  3. EXEMPTION CERTIFICATE (Customer Provides)                               │
│     Purpose: Customer claims exemption from tax                             │
│     Types:                                                                   │
│     • Government exemption                                                  │
│     • Non-profit exemption                                                  │
│     • Manufacturing exemption                                               │
│     • Agricultural exemption                                                │
│     Your role: Collect and retain certificate                               │
│                                                                              │
│  4. CONTRACTOR EXEMPTION                                                     │
│     Purpose: Some states have contractor-specific exemptions                │
│     Example: Texas has exemption for "new construction" materials          │
│     Risk: Must meet specific criteria                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Managing Exemption Certificates

```
EXEMPTION CERTIFICATE MANAGEMENT:

RECEIVING FROM VENDORS (When you're buying):
────────────────────────────────────────────
Most contractors should NOT give resale certificates to vendors
because you're the consumer, not reseller.

Exception: Items you actually resell (e.g., appliances, fixtures
sold separately from installation)

RECEIVING FROM CUSTOMERS (When you're selling):
───────────────────────────────────────────────
If customer claims exemption:
1. Get certificate BEFORE or at time of sale
2. Verify certificate is:
   • Complete (all fields filled)
   • Valid (not expired)
   • Appropriate for transaction
   • From authorized representative
3. Retain for audit (typically 4+ years)
4. Organize by customer

COMMON EXEMPT CUSTOMERS:
• Federal government (always exempt)
• State/local government (usually exempt)
• Schools and universities (often exempt)
• Non-profits 501(c)(3) (varies by state/purchase type)
• Religious organizations (varies)
• Manufacturers (for manufacturing equipment/materials)

QBO STORAGE:
• Attach certificates to customer record
• Note exemption status in customer profile
• Set tax-exempt status in QBO
```

---

## State-by-State Overview

### Major State Categories

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    STATE TAX TREATMENT CATEGORIES                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  CATEGORY 1: CONTRACTOR AS CONSUMER (Most States)                           │
│  ─────────────────────────────────────────────────────────────────────────  │
│  States: TX, CA, FL, NY, IL, PA, OH, MI, GA, NC, and most others           │
│  Treatment:                                                                  │
│  • Pay tax when you buy materials                                           │
│  • Don't charge tax on contracts (real property)                           │
│  • May charge tax on some retail items                                     │
│                                                                              │
│  CATEGORY 2: GROSS RECEIPTS TAX (Tax on Everything)                         │
│  ─────────────────────────────────────────────────────────────────────────  │
│  States: AZ, HI, NM                                                         │
│  Treatment:                                                                  │
│  • Tax on total contract amount (or gross receipts)                        │
│  • May buy materials tax-free (for resale)                                 │
│  • Very different from sales tax model                                     │
│                                                                              │
│  CATEGORY 3: MIXED/COMPLEX RULES                                            │
│  ─────────────────────────────────────────────────────────────────────────  │
│  States: Many have nuances                                                  │
│  Examples:                                                                   │
│  • Some tax repair but not new construction                                │
│  • Some have different rules for residential vs. commercial                │
│  • Some have contractor-specific exemptions                                │
│                                                                              │
│  CATEGORY 4: NO SALES TAX                                                    │
│  ─────────────────────────────────────────────────────────────────────────  │
│  States: OR, MT, NH, DE, AK (no state tax, some local)                     │
│  Treatment:                                                                  │
│  • No state sales tax to pay or collect                                    │
│  • May still have gross receipts, B&O, or local taxes                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Selected State Details

```
TEXAS:
──────
• Contractors are consumers
• Pay tax on materials when purchased
• Don't charge tax on real property contracts
• Exemptions: Manufacturing, certain new construction
• Rate: 6.25% state + up to 2% local

CALIFORNIA:
───────────
• Contractors are consumers
• Pay tax on materials at purchase
• "Fixtures" vs. "materials" distinction matters
• Fabrication has special rules
• Rate: 7.25% state + local (up to ~10.75%)

FLORIDA:
────────
• Contractors are consumers
• Pay tax on materials
• Real property contracts not taxable
• Repair vs. improvement distinction exists
• Rate: 6% state + local discretionary

ARIZONA:
────────
• Transaction Privilege Tax (TPT) - gross receipts
• Prime contractors taxed on total contract
• May deduct subcontractor payments
• Complex local (city) taxes
• State rate: 5.6% + local varies significantly

NEW YORK:
─────────
• Contractors are consumers
• Capital improvement exemption available
• Must give customer Form ST-124
• Installation of TPP may be taxable
• Rate: 4% state + local (NYC = 8.875% total)

⚠️ THESE ARE SUMMARIES ONLY - Consult state-specific guidance!
```

---

## QBO Setup for Sales Tax

### Configuring Sales Tax in QBO

```
QBO SALES TAX SETUP FOR CONTRACTORS:

Step 1: Enable Sales Tax
────────────────────────
Navigation: Settings ⚙️ → Sales Tax → Set up sales tax
• Enter business address
• QBO will determine your rates

Step 2: Configure Tax Rates
───────────────────────────
QBO will auto-populate rates based on location
You may need to add:
• Use tax rate (if not automatic)
• Specific local rates
• Special rates for certain transactions

Step 3: Create Tax-Exempt Customers
────────────────────────────────────
For government/exempt customers:
1. Edit customer record
2. Set "Tax exempt" to Yes
3. Enter exemption reason
4. Attach exemption certificate

Step 4: Configure Products/Services
────────────────────────────────────
For items you sell:
• Taxable items: Enable "Taxable" flag
• Non-taxable labor: Disable "Taxable" flag
• Materials in lump-sum contracts: Usually non-taxable to customer
```

### Recording Tax on Purchases

```
TRACKING TAX PAID ON PURCHASES:

Option 1: Track Through Vendor Bills
────────────────────────────────────
Enter full invoice amount including tax
• Materials: $1,000.00
• Sales Tax: $82.50
• Total Bill: $1,082.50

This approach:
• Simple to enter
• Tax is part of COGS
• No separate tax tracking needed

Option 2: Separate Tax Account
──────────────────────────────
Create account: "Sales Tax Paid on Purchases"
Enter as separate line on bills

Benefits:
• See total tax paid
• Useful for analysis
• May help with exemption claims

Option 3: Use QBO's Expense Tax Feature
───────────────────────────────────────
If available in your QBO version:
• Settings → Expenses → Track sales tax
• QBO will track tax on expense transactions
```

### Sales Tax Reporting

```
QBO SALES TAX REPORTS:

For Contractors (Tax Paid on Purchases):
───────────────────────────────────────
• Transaction List by Vendor - see tax paid
• Expense by Vendor - total purchases
• Custom report on sales tax expense account

For Contractors Who Collect Tax:
───────────────────────────────
Navigation: Taxes → Sales Tax
• See tax collected
• See tax owed
• File returns (if using QBO filing)

Sales Tax Liability Report:
• Reports → Sales Tax Liability
• Shows tax collected by jurisdiction
• Used to prepare tax returns

Use Tax Tracking:
• If tracking use tax in liability account
• Run balance sheet for Use Tax Payable
• Shows amount due to state
```

---

## Common Compliance Mistakes

### Top Contractor Tax Mistakes

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COMMON SALES TAX MISTAKES                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. USING RESALE CERTIFICATES INCORRECTLY                                   │
│     Mistake: Buying materials tax-free when you're the consumer            │
│     Result: Tax due plus penalties and interest on audit                   │
│     Fix: Only use resale cert for items actually resold                    │
│                                                                              │
│  2. IGNORING USE TAX                                                         │
│     Mistake: Not paying use tax on out-of-state purchases                  │
│     Result: Tax due, penalties, and interest                               │
│     Fix: Track and remit use tax monthly/quarterly                         │
│                                                                              │
│  3. WRONG TREATMENT IN GROSS RECEIPTS STATES                                │
│     Mistake: Treating AZ/HI/NM like consumer states                        │
│     Result: Significant tax liability                                      │
│     Fix: Understand your state's system                                    │
│                                                                              │
│  4. NOT COLLECTING EXEMPTION CERTIFICATES                                   │
│     Mistake: Not charging tax without valid certificate                    │
│     Result: You're liable if customer wasn't exempt                        │
│     Fix: Get certificate before or at sale                                 │
│                                                                              │
│  5. CHARGING TAX ON NON-TAXABLE ITEMS                                       │
│     Mistake: Charging customers tax when you shouldn't                     │
│     Result: Customer complaints, refund liability                          │
│     Fix: Understand what's taxable in your state                           │
│                                                                              │
│  6. INVENTORY WITHDRAWALS                                                    │
│     Mistake: Taking inventory for business use, no tax paid               │
│     Result: Use tax due                                                     │
│     Fix: Pay use tax on withdrawn inventory                                │
│                                                                              │
│  7. MULTI-STATE CONFUSION                                                    │
│     Mistake: Applying home state rules in other states                     │
│     Result: Non-compliance in work states                                  │
│     Fix: Research each state's rules                                       │
│                                                                              │
│  8. POOR RECORD KEEPING                                                      │
│     Mistake: Can't document tax paid or exemptions                         │
│     Result: Assumed liable on audit                                        │
│     Fix: Retain invoices, certificates, records                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Audit Preparation

### What Auditors Look For

```
SALES TAX AUDIT FOCUS AREAS:

1. RESALE CERTIFICATE USAGE
   • Do you have certificates on file?
   • Are they valid and complete?
   • Do purchases match certificate claims?

2. USE TAX COMPLIANCE
   • Out-of-state purchases identified?
   • Use tax accrued and paid?
   • Matching use tax to purchases?

3. EXEMPTION CERTIFICATE COLLECTION
   • Certificates on file for exempt sales?
   • Certificates valid at time of sale?
   • Appropriate for transaction type?

4. PROPER CLASSIFICATION
   • Taxable vs. non-taxable items?
   • Real property vs. personal property?
   • Labor correctly treated?

5. TIMING AND REPORTING
   • Tax paid in correct period?
   • Returns filed on time?
   • Amounts match records?
```

### Audit Defense Best Practices

```
AUDIT PREPARATION CHECKLIST:

DOCUMENTATION TO MAINTAIN:
□ All vendor invoices showing tax paid
□ Out-of-state purchase records
□ Use tax calculation worksheets
□ Exemption certificates from customers
□ Resale certificates given (and justification)
□ Tax returns filed
□ Payment confirmations
□ Contracts (to show lump sum vs. T&M)

ORGANIZE BY:
• Year
• Vendor/Customer
• Project (if relevant)
• Tax type (sales vs. use)

RETENTION PERIOD:
• Minimum 4 years (some states require longer)
• Longer for open audits
• Indefinite for major transactions

IF AUDITED:
• Respond promptly to requests
• Provide only what's requested
• Keep copies of everything provided
• Consider professional representation
• Know your appeal rights
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SALES TAX QUICK REFERENCE                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  GENERAL RULE (Most States):                                                │
│  • Pay tax when you BUY materials                                           │
│  • Don't charge tax on contracts for real property improvement             │
│  • May charge tax on items sold separately                                  │
│                                                                              │
│  USE TAX:                                                                    │
│  • Owe when no sales tax was charged                                        │
│  • Rate = your local sales tax rate                                         │
│  • Report on sales tax return or separately                                │
│                                                                              │
│  EXEMPTION CERTIFICATES:                                                     │
│  • Get from exempt customers BEFORE sale                                    │
│  • Retain for 4+ years                                                      │
│  • Verify completeness and validity                                         │
│                                                                              │
│  WARNING STATES (Different Rules):                                          │
│  • Arizona - Transaction Privilege Tax                                      │
│  • Hawaii - General Excise Tax                                              │
│  • New Mexico - Gross Receipts Tax                                          │
│  • Washington - B&O Tax considerations                                      │
│                                                                              │
│  WHEN IN DOUBT:                                                              │
│  • Consult your state's tax authority website                              │
│  • Get written guidance if possible                                         │
│  • Consult a qualified tax professional                                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With sales and use tax understood:
- [Prevailing Wage & Certified Payroll](../workflows/05-prevailing-wage-certified-payroll.md) - Government project compliance
- [Bonding Requirements](./02-bonding-requirements.md) - Surety and bonding
- [GAAP Principles](../reference/12-gaap-principles.md) - Accounting standards

---

*[Back to Main Guide](../../README.md)*
