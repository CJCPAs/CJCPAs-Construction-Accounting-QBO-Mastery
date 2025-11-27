# Company Settings for Construction Contractors

## Overview

Properly configuring QuickBooks Online settings is **critical** for construction accounting. This guide walks through every setting that matters for contractors, explaining what each does and why it matters.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Consult with a qualified CPA before implementing. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Accessing Account Settings](#accessing-account-settings)
2. [Company Tab Settings](#company-tab-settings)
3. [Sales Tab Settings](#sales-tab-settings)
4. [Expenses Tab Settings](#expenses-tab-settings)
5. [Payments Tab Settings](#payments-tab-settings)
6. [Advanced Tab Settings](#advanced-tab-settings)
7. [Construction-Specific Configurations](#construction-specific-configurations)
8. [Settings Checklist](#settings-checklist)

---

## Accessing Account Settings

**Navigation Path:**
```
⚙️ Gear Icon (upper right) → Account and Settings
```

The Account and Settings panel has five main tabs:
1. Company
2. Sales
3. Expenses
4. Payments
5. Advanced

---

## Company Tab Settings

### Company Name Section

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  COMPANY NAME SETTINGS                                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Company name: [Your legal business name]                                    │
│  └── Use your exact legal name as registered                                 │
│      Example: "Smith Construction, LLC"                                      │
│                                                                              │
│  Legal name: [If different from company name]                                │
│  └── Often same as company name                                              │
│      Used on official tax documents                                          │
│                                                                              │
│  EIN: [XX-XXXXXXX]                                                           │
│  └── Federal Employer Identification Number                                  │
│      Required for W-9/1099 reporting                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Company Type

**Recommended for Contractors:**
```
Company type: [Select your legal structure]
Options:
- Sole Proprietor
- Partnership
- LLC - Single Member
- LLC - Multi Member
- S Corporation
- C Corporation
- Other/None

Tax form: [Auto-selected based on type]
```

**WHY THIS MATTERS:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│  TAX IMPLICATIONS                                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Your company type affects:                                                  │
│  • How QBO categorizes owner transactions                                    │
│  • Which tax reports are available                                           │
│  • Default equity account structure                                          │
│  • 1099 vendor reporting requirements                                        │
│                                                                              │
│  Example: S-Corp vs LLC                                                      │
│  ─────────────────────────────────────────────────────────────────────────  │
│  S-Corp: Owner payments → Payroll (reasonable salary)                       │
│          Distributions → Shareholder distributions                          │
│                                                                              │
│  LLC:    Owner payments → Owner's draw                                      │
│          No payroll requirement (but may still do payroll)                  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Contact Info

```
Company email: [office@yourcompany.com]
└── Used for customer communications

Customer-facing email: [billing@yourcompany.com]
└── Appears on invoices and statements

Phone: [Main office number]

Website: [www.yourcompany.com]
```

### Address

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  ADDRESS SETTINGS                                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Company address: [Physical office address]                                  │
│  └── Appears on invoices, estimates, purchase orders                        │
│                                                                              │
│  Legal address: [Registered agent address if different]                      │
│  └── Used for official/legal correspondence                                  │
│                                                                              │
│  FOR CONTRACTORS:                                                            │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Use professional address (avoid P.O. boxes on customer-facing docs)      │
│  • Include contractor's license number in address block if required         │
│  • Consider separate billing address for payment processing                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Sales Tab Settings

### Customize Look and Feel

**Step-by-Step Setup:**

1. **Logo Upload**
   ```
   Upload: Your company logo
   Format: PNG or JPG
   Size: 500KB max, at least 500x500 pixels recommended
   ```

2. **Invoice Template**
   ```
   Style: Modern, Classic, or Airy
   Color: Match your brand colors
   Font: Professional, readable
   ```

3. **Custom Fields Display**
   ```
   Show custom fields on forms: ✅ Yes
   Position: Below header
   ```

### Sales Form Content

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  SALES FORM CONTENT SETTINGS                                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Preferred invoice terms: Net 30                                             │
│  └── CONSTRUCTION NOTE: Many contracts specify payment terms;                │
│      verify against your contract before defaulting                          │
│                                                                              │
│  Preferred delivery method: Email                                            │
│  └── Primary method for sending invoices                                     │
│                                                                              │
│  Shipping: OFF                                                               │
│  └── Typically not needed for construction                                   │
│                                                                              │
│  Custom fields on forms:                                                     │
│  └── ☑️ Project                                                              │
│  └── ☑️ Pay App Number                                                       │
│  └── ☑️ Contract Number                                                      │
│                                                                              │
│  Custom transaction numbers: ON                                              │
│  └── Allows manual invoice numbering                                        │
│      Use: PAY-2024-001-03 (Job-Year-Draw#)                                  │
│                                                                              │
│  Service date: ON                                                            │
│  └── Critical for construction - shows work period                          │
│                                                                              │
│  Discount: ON                                                                │
│  └── Needed for retainage calculations                                      │
│                                                                              │
│  Deposit: ON                                                                 │
│  └── For recording deposits received                                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Products and Services

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PRODUCTS AND SERVICES SETTINGS                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Show Product/Service column on sales forms: ON                              │
│  └── Required for line-item billing                                          │
│                                                                              │
│  Show SKU column: OFF                                                        │
│  └── Not typically needed for construction                                   │
│                                                                              │
│  Track quantity and price/rate: ON                                           │
│  └── Essential for progress billing                                          │
│                                                                              │
│  Track inventory quantity on hand: OFF                                       │
│  └── Most contractors don't track materials inventory                        │
│      Exception: If you stock common materials                                │
│                                                                              │
│  CONSTRUCTION PRODUCTS TO CREATE:                                            │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Progress Billing (Service) → Income:Contract Revenue                     │
│  • Change Order (Service) → Income:Contract Revenue                         │
│  • Retainage Held (Service) → Liability:Retainage Payable                   │
│  • Retainage Released (Service) → Liability:Retainage Payable               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Messages

**Default Invoice Message:**
```
Thank you for your business. Payment is due within 30 days.
Please reference Invoice #{number} with your payment.

Questions? Contact [Your Name] at [Phone] or [Email].
```

**Default Estimate Message:**
```
This estimate is valid for 30 days from the date shown above.
Please contact us to schedule your project.
```

### Statements

```
Show aging table at bottom of statement: ON
└── Shows 0-30, 31-60, 61-90, 90+ day aging

Statement type: Balance Forward
└── Shows running balance (preferred for construction)
```

### Reminders

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  REMINDER SETTINGS                                                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Automatic invoice reminders: ON (with caution)                             │
│                                                                              │
│  First reminder: 3 days before due                                           │
│  Second reminder: On due date                                                │
│  Third reminder: 7 days after due                                            │
│                                                                              │
│  ⚠️ CONSTRUCTION CAUTION:                                                   │
│  Many construction projects have specific billing cycles tied to            │
│  pay application schedules. Generic reminders may not align with            │
│  contract terms. Review your contracts before enabling auto-reminders.      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Online Delivery

```
Email delivery options:
☑️ Email invoices as PDFs
☑️ Email estimates as PDFs
☑️ Include a summary of amounts

PDF options:
☑️ Attach invoice PDF
File naming: Invoice_{number}_{customer}
```

---

## Expenses Tab Settings

### Bills and Expenses

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  EXPENSE SETTINGS                                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Show Items table on expense and purchase forms: ON                          │
│  └── Allows item-based expense tracking                                      │
│                                                                              │
│  Track expenses and items by customer: ON ✅ (CRITICAL)                      │
│  └── ESSENTIAL for job costing!                                              │
│      Allows assigning costs to jobs/customers                                │
│                                                                              │
│  Make expenses and items billable: ON                                        │
│  └── Mark costs as billable to customers                                     │
│      Used for T&M and cost-plus contracts                                    │
│                                                                              │
│  Default bill payment terms: Net 30                                          │
│  └── Can override per vendor                                                 │
│                                                                              │
│  Use purchase orders: ON ✅                                                   │
│  └── Essential for construction cost control                                 │
│      Links POs to bills for verification                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Purchase Orders

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PURCHASE ORDER SETTINGS                                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Use purchase orders: ON                                                     │
│                                                                              │
│  Custom transaction numbers: ON                                              │
│  └── Format: PO-2024-001-015 (PO-Year-Job-Sequence)                         │
│                                                                              │
│  Custom fields:                                                              │
│  └── ☑️ Job/Project Name                                                    │
│  └── ☑️ Requested By                                                        │
│  └── ☑️ Ship To (Job Site Address)                                          │
│                                                                              │
│  Default message:                                                            │
│  "This Purchase Order is subject to the terms and conditions of             │
│   our subcontract/purchase agreement. Please confirm receipt."              │
│                                                                              │
│  WHY POs MATTER FOR CONSTRUCTION:                                            │
│  ─────────────────────────────────────────────────────────────────────────  │
│  • Controls spending before it happens                                       │
│  • Documents authorization for job costs                                     │
│  • Enables three-way matching (PO → Receipt → Bill)                         │
│  • Provides audit trail for cost overruns                                   │
│  • Required by many contracts and bonding companies                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Payments Tab Settings

### Payment Settings

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PAYMENT PROCESSING                                                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Accept payments online:                                                     │
│  ☑️ Bank transfer (ACH): ON                                                 │
│  ☑️ Credit cards: ON (consider fees)                                        │
│  ☑️ PayPal: Optional                                                        │
│                                                                              │
│  CONSTRUCTION CONSIDERATIONS:                                                │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Credit Card Fees:                                                           │
│  • Typical: 2.9% + $0.25 per transaction                                    │
│  • On $50,000 draw: $1,475 in fees!                                         │
│  • Many contractors don't accept CC for large draws                         │
│  • Some add surcharge (where legal)                                         │
│                                                                              │
│  ACH (Bank Transfer):                                                        │
│  • Lower fees: ~1% or flat fee                                              │
│  • Preferred for large payments                                              │
│  • Longer clearing time (3-5 days)                                          │
│                                                                              │
│  Recommended Setup:                                                          │
│  • ACH: Yes (primary for draws)                                              │
│  • Credit Card: Yes (for small change orders, service)                      │
│  • Set threshold: "Credit cards accepted for amounts under $5,000"          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Advanced Tab Settings

### Accounting

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  ACCOUNTING SETTINGS                                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  First month of fiscal year: January                                         │
│  └── Most contractors use calendar year                                      │
│      Verify with your tax preparer                                           │
│                                                                              │
│  First month of income tax year: January                                     │
│  └── Usually matches fiscal year                                             │
│                                                                              │
│  Accounting method: Accrual ✅                                               │
│  └── CRITICAL for construction!                                              │
│                                                                              │
│  Close the books: ON                                                         │
│  └── Password protect closed periods                                         │
│      Prevents accidental changes to prior periods                            │
│                                                                              │
│  Tax form: Based on company type                                             │
│  └── C-Corp: Form 1120                                                       │
│      S-Corp: Form 1120-S                                                     │
│      Partnership/LLC: Form 1065                                              │
│      Sole Prop: Schedule C                                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### WHY Accrual Method for Construction

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CASH VS ACCRUAL FOR CONSTRUCTION                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  CASH BASIS:                                                                 │
│  • Revenue recorded when payment received                                    │
│  • Expenses recorded when payment made                                       │
│  • ❌ Does NOT show true job profitability                                   │
│  • ❌ Cannot calculate WIP or overbilling                                    │
│                                                                              │
│  ACCRUAL BASIS:                                                              │
│  • Revenue recorded when earned (billed)                                     │
│  • Expenses recorded when incurred (bill received)                          │
│  • ✅ Shows accurate job profitability                                      │
│  • ✅ Required for WIP schedules                                            │
│  • ✅ Required for percentage-of-completion                                 │
│  • ✅ Required for bonding/bank financing                                   │
│                                                                              │
│  GAAP REQUIREMENT:                                                           │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Contractors over certain thresholds MUST use accrual accounting            │
│  under ASC 606 for financial reporting.                                      │
│                                                                              │
│  Note: You can maintain books on accrual and file taxes on cash             │
│  (with CPA guidance) for eligible contractors.                               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Categories (Classes and Locations)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  CATEGORIES SETTINGS                                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Track classes: ON ✅ (ESSENTIAL)                                            │
│  └── Used for job/project tracking                                           │
│                                                                              │
│  Assign classes:                                                             │
│  └── ○ One to entire transaction                                            │
│  └── ● One to each row in transaction ✅                                    │
│      (Allows split billing across jobs)                                      │
│                                                                              │
│  Warn me when a transaction isn't assigned a class: ON ✅                   │
│  └── Prevents unclassified transactions                                      │
│                                                                              │
│  Track locations: ON (if multi-site)                                         │
│  └── Label as: Locations / Business / Divisions                             │
│                                                                              │
│  See: [Classes and Locations Guide](./01-classes-locations-tracking.md)     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Automation

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  AUTOMATION SETTINGS                                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Pre-fill forms with previously entered content: ON                          │
│  └── Auto-fills based on past entries                                        │
│                                                                              │
│  Automatically apply credits: OFF                                            │
│  └── For construction, manually control credit application                   │
│      Prevents incorrect credit application across jobs                       │
│                                                                              │
│  Automatically invoice unbilled activity: OFF                                │
│  └── Don't auto-generate invoices                                            │
│      Control billing cycle manually                                          │
│                                                                              │
│  Automatically apply bill payments: ON                                       │
│  └── Matches payments to bills automatically                                 │
│                                                                              │
│  Copy estimates to invoices: ON                                              │
│  └── Enables creating invoice from estimate                                  │
│      Useful for fixed-price contracts                                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Projects

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PROJECT SETTINGS (QBO Plus/Advanced)                                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Organize all job-related activity in one place: ON ✅                      │
│  └── Enables Project feature                                                 │
│                                                                              │
│  Sub-customers:                                                              │
│  └── ● Bill with parent                                                     │
│  └── ○ Bill separately                                                      │
│      (Choose based on your billing structure)                                │
│                                                                              │
│  CONSTRUCTION USE:                                                           │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Projects provide:                                                           │
│  • Project dashboard with P&L                                               │
│  • Time tracking by project                                                  │
│  • Task management                                                           │
│  • All transactions in one view                                              │
│                                                                              │
│  RECOMMENDATION: Use Projects AND Classes                                    │
│  • Projects: For dashboard and time tracking                                 │
│  • Classes: For detailed financial reporting and WIP                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Time Tracking

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  TIME TRACKING SETTINGS                                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Add Service field to timesheets: ON                                         │
│  └── Specify service type for each time entry                               │
│                                                                              │
│  Make Single-Time Activity Billable: ON                                      │
│  └── For T&M contracts                                                       │
│                                                                              │
│  First day of work week: Monday                                              │
│  └── Matches typical construction schedules                                  │
│                                                                              │
│  CONSTRUCTION TIME TRACKING:                                                 │
│  ─────────────────────────────────────────────────────────────────────────  │
│  Time entries should capture:                                                │
│  • Employee                                                                  │
│  • Customer/Job                                                              │
│  • Service type (Labor category)                                             │
│  • Hours worked                                                              │
│  • Billable status                                                           │
│  • Description                                                               │
│                                                                              │
│  Integrates with: QBO Workforce, TSheets, Clockify                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Currency

```
Home currency: USD (United States Dollar)
Multi-currency: OFF (unless doing international work)
```

### Other Preferences

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  OTHER SETTINGS                                                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Date format: MM/DD/YYYY (US standard)                                       │
│                                                                              │
│  Number format: 123,456.00 (US standard)                                     │
│                                                                              │
│  Customer label: Customers (or "Clients")                                    │
│                                                                              │
│  Warn if duplicate check number: ON ✅                                       │
│  └── Prevents duplicate check numbers                                        │
│                                                                              │
│  Warn if duplicate bill number: ON ✅                                        │
│  └── Catches duplicate vendor bills                                          │
│                                                                              │
│  Sign me out if inactive for: 1 hour                                         │
│  └── Security setting                                                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Construction-Specific Configurations

### Sales Tax Settings

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  SALES TAX FOR CONSTRUCTION                                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Navigate: Taxes → Sales Tax → Sales Tax Settings                           │
│                                                                              │
│  CONSTRUCTION TAX RULES (Vary by State):                                     │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Model 1: Tax on Materials, Exempt Labor                                     │
│  • Contractor pays sales tax on materials purchased                         │
│  • Labor is not taxable                                                      │
│  • Setup: Don't charge sales tax on invoices                                │
│  • States: Texas, Florida, many others                                       │
│                                                                              │
│  Model 2: Tax on Completed Contract                                          │
│  • Contractor charges sales tax on total contract                           │
│  • Materials purchased with resale certificate                              │
│  • Setup: Charge sales tax on invoices                                      │
│  • States: Hawaii, New Mexico, some others                                   │
│                                                                              │
│  Model 3: Mixed/Complex                                                      │
│  • Different rules for residential vs commercial                             │
│  • Different rules for new construction vs repair                            │
│  • States: California, New York, others                                      │
│                                                                              │
│  ⚠️ CRITICAL: Consult with a tax professional for your specific state!     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Default Accounts Setup

**Products/Services Default Accounts:**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PRODUCT/SERVICE → ACCOUNT MAPPING                                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  REVENUE ITEMS:                                                              │
│  Product/Service Name        │  Income Account                              │
│  ────────────────────────────┼────────────────────────────────────────────  │
│  Progress Billing            │  40000 Contract Revenue                      │
│  Change Order Revenue        │  40000 Contract Revenue (or separate)        │
│  T&M Labor                   │  40100 T&M Revenue                           │
│  Service/Repairs             │  40200 Service Revenue                       │
│                                                                              │
│  RETAINAGE ITEMS:                                                            │
│  Product/Service Name        │  Account                                     │
│  ────────────────────────────┼────────────────────────────────────────────  │
│  Retainage Withheld          │  23000 Retainage Payable (Liability)         │
│  Retainage Released          │  23000 Retainage Payable (Liability)         │
│                                                                              │
│  COST ITEMS (for bill entry):                                                │
│  Category                    │  Expense Account                             │
│  ────────────────────────────┼────────────────────────────────────────────  │
│  Materials                   │  50100 Materials                             │
│  Subcontractor               │  50200 Subcontractor Costs                   │
│  Equipment Rental            │  50300 Equipment Costs                       │
│  Labor (if not payroll)      │  50400 Direct Labor                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### User Roles Setup

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  USER ROLES FOR CONSTRUCTION COMPANY                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Navigate: ⚙️ → Manage Users                                                │
│                                                                              │
│  RECOMMENDED ROLES:                                                          │
│  ─────────────────────────────────────────────────────────────────────────  │
│                                                                              │
│  Owner/Controller: Master Admin                                              │
│  • Full access to all features                                               │
│  • Can manage users and settings                                             │
│  • Can close books                                                           │
│                                                                              │
│  Bookkeeper/Accountant: Standard User - All Access                          │
│  • Full access to transactions and reports                                   │
│  • No user management                                                        │
│  • No settings changes                                                       │
│                                                                              │
│  AP Clerk: Custom - Bills Only                                               │
│  • Enter and edit bills                                                      │
│  • Create purchase orders                                                    │
│  • View vendors                                                              │
│  • No check writing                                                          │
│  • No report access                                                          │
│                                                                              │
│  Project Manager: Custom - View + Time                                       │
│  • View job reports                                                          │
│  • Enter time                                                                │
│  • View expenses by job                                                      │
│  • No transaction entry                                                      │
│                                                                              │
│  See: [User Roles Guide](../security/01-user-roles-permissions.md)          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Settings Checklist

Use this checklist when setting up QBO for a new construction company:

### Company Settings

- [ ] Company name and legal name correct
- [ ] EIN entered
- [ ] Company type selected
- [ ] Fiscal year start month set
- [ ] Address and contact info complete

### Sales Settings

- [ ] Logo uploaded
- [ ] Invoice template customized
- [ ] Default terms set (Net 30)
- [ ] Custom transaction numbers ON
- [ ] Service date field ON
- [ ] Discount field ON
- [ ] Products and services created:
  - [ ] Progress Billing
  - [ ] Change Order
  - [ ] Retainage Held
  - [ ] Retainage Released

### Expense Settings

- [ ] Track expenses by customer ON
- [ ] Make expenses billable ON
- [ ] Use purchase orders ON
- [ ] Default bill payment terms set

### Advanced Settings

- [ ] Accounting method: Accrual
- [ ] Track classes ON
- [ ] Class assignment: One per row
- [ ] Class warning ON
- [ ] Projects enabled (Plus/Advanced)
- [ ] Time tracking configured
- [ ] Close the books enabled

### Sales Tax

- [ ] Sales tax settings reviewed
- [ ] Tax rates configured per jurisdiction
- [ ] Products marked taxable/non-taxable correctly

### User Management

- [ ] User roles defined
- [ ] Users invited with appropriate access
- [ ] Accountant invited (if applicable)

---

## Next Steps

With settings configured, proceed to:
- [Chart of Accounts Setup](../templates/09-chart-of-accounts.md)
- [Job Costing Setup](../tutorials/03-job-costing-setup.md)
- [Connecting Bank Accounts](../basics/01-connecting-bank-accounts.md)

---

*[Back to Main Guide](../../README.md)*
