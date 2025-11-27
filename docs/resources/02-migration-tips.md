# Migration Tips: Desktop to QuickBooks Online

## Overview

Migrating from QuickBooks Desktop (or other accounting systems) to QuickBooks Online requires careful planning. This guide covers the migration process, common pitfalls, and construction-specific considerations.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Migration involves risk to your financial data. Consider engaging a QuickBooks ProAdvisor for complex migrations. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Pre-Migration Planning](#pre-migration-planning)
2. [Migration Methods](#migration-methods)
3. [Data That Migrates (and Doesn't)](#data-that-migrates-and-doesnt)
4. [Construction-Specific Considerations](#construction-specific-considerations)
5. [Step-by-Step Migration Process](#step-by-step-migration-process)
6. [Post-Migration Verification](#post-migration-verification)
7. [Common Problems and Solutions](#common-problems-and-solutions)
8. [Running Parallel Systems](#running-parallel-systems)

---

## Pre-Migration Planning

### Migration Readiness Checklist

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BEFORE YOU START                                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ASSESS YOUR CURRENT SYSTEM:                                                 │
│  □ Which QuickBooks version are you migrating FROM?                         │
│    • Desktop Pro, Premier, Enterprise?                                      │
│    • Year/version?                                                           │
│  □ How many years of data do you have?                                      │
│  □ What features do you use?                                                │
│    • Job costing/classes?                                                   │
│    • Progress invoicing?                                                    │
│    • Custom fields?                                                          │
│    • Memorized reports?                                                     │
│  □ How large is your file?                                                  │
│    • Number of customers                                                    │
│    • Number of vendors                                                      │
│    • Number of transactions                                                 │
│                                                                              │
│  CLEAN UP DESKTOP FILE FIRST:                                                │
│  □ Run Verify/Rebuild utility                                               │
│  □ Merge duplicate customers/vendors                                        │
│  □ Make inactive unused items                                               │
│  □ Clear undeposited funds                                                  │
│  □ Complete bank reconciliations                                            │
│  □ Delete old memorized transactions no longer needed                       │
│                                                                              │
│  TIMING CONSIDERATIONS:                                                      │
│  □ Plan for month-end or year-end cutover                                  │
│  □ Allow 1-2 weeks for verification                                        │
│  □ Avoid busy billing periods                                               │
│  □ Schedule during slower project phases                                    │
│                                                                              │
│  BACKUP:                                                                     │
│  □ Create verified backup of Desktop file                                   │
│  □ Store backup in multiple locations                                       │
│  □ Keep Desktop accessible for reference                                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Choose the Right Time

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BEST TIMES TO MIGRATE                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  BEST: Start of New Fiscal Year                                              │
│  ─────────────────────────────                                               │
│  • Clean break between systems                                               │
│  • Begin fresh with opening balances                                        │
│  • No mid-year complications                                                │
│                                                                              │
│  GOOD: Start of Quarter                                                      │
│  ─────────────────────────                                                   │
│  • Natural reporting break                                                   │
│  • Less historical data to verify                                           │
│                                                                              │
│  ACCEPTABLE: Start of Month                                                  │
│  ───────────────────────────                                                 │
│  • Complete month-end close in Desktop                                      │
│  • Begin new month in QBO                                                   │
│                                                                              │
│  AVOID:                                                                      │
│  ─────────                                                                   │
│  • Mid-month (reconciliation issues)                                        │
│  • During major project billing cycles                                      │
│  • Tax season (Jan-Apr for most)                                            │
│  • Year-end close period                                                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Migration Methods

### Method 1: Automated Migration Tool

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    AUTOMATED MIGRATION                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Intuit provides a migration tool for Desktop to Online conversion.         │
│                                                                              │
│  PROCESS:                                                                    │
│  1. In Desktop: File → Export → Company File to QuickBooks Online           │
│  2. Sign in to QBO account                                                   │
│  3. Tool converts and uploads data                                          │
│  4. Review in QBO                                                            │
│                                                                              │
│  PROS:                                                                       │
│  ✅ Transfers most data automatically                                       │
│  ✅ Maintains transaction history                                           │
│  ✅ Preserves account balances                                              │
│                                                                              │
│  CONS:                                                                       │
│  ❌ Some features don't convert                                             │
│  ❌ Large files may have issues                                             │
│  ❌ Custom fields may not transfer                                          │
│  ❌ Job costing structure may change                                        │
│                                                                              │
│  FILE SIZE LIMITS:                                                           │
│  • QBO Plus: Files with target count < 750,000                              │
│  • QBO Advanced: Larger files supported                                     │
│  • "Target count" = customers + vendors + employees + chart of accounts     │
│                     + items + transactions                                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Method 2: Manual/Clean Start

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CLEAN START MIGRATION                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Start fresh in QBO with opening balances only.                             │
│                                                                              │
│  PROCESS:                                                                    │
│  1. Set up new QBO company                                                   │
│  2. Configure chart of accounts                                              │
│  3. Import customer/vendor lists                                            │
│  4. Enter opening balance journal entry                                     │
│  5. Enter individual open invoices/bills                                    │
│                                                                              │
│  PROS:                                                                       │
│  ✅ Clean data in new system                                                │
│  ✅ Opportunity to improve structure                                        │
│  ✅ No conversion errors                                                    │
│  ✅ Works for any source system                                             │
│                                                                              │
│  CONS:                                                                       │
│  ❌ More manual work                                                        │
│  ❌ No transaction history                                                  │
│  ❌ Must reference old system for history                                   │
│                                                                              │
│  BEST FOR:                                                                   │
│  • Very old/messy data                                                       │
│  • Non-QuickBooks systems                                                    │
│  • When you want to restructure                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Method 3: Third-Party Migration Services

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    THIRD-PARTY SERVICES                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PROFESSIONAL MIGRATION SERVICES:                                            │
│  ─────────────────────────────────                                           │
│  • QuickBooks ProAdvisors                                                    │
│  • Specialized migration companies                                          │
│  • Accounting firms                                                          │
│                                                                              │
│  WHAT THEY PROVIDE:                                                          │
│  • Data cleanup pre-migration                                               │
│  • Conversion execution                                                      │
│  • Verification and testing                                                  │
│  • Training on new system                                                    │
│  • Support during transition                                                 │
│                                                                              │
│  COST: $500 - $5,000+ depending on complexity                               │
│                                                                              │
│  RECOMMENDED FOR:                                                            │
│  • Large or complex files                                                    │
│  • Multiple company files                                                    │
│  • Limited internal capacity                                                 │
│  • Critical need for accuracy                                               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Data That Migrates (and Doesn't)

### What Typically Transfers

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MIGRATION DATA STATUS                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TRANSFERS WELL:                                                             │
│  ✅ Chart of accounts                                                       │
│  ✅ Customer list (basic info)                                              │
│  ✅ Vendor list (basic info)                                                │
│  ✅ Item/service list                                                       │
│  ✅ Transactions (invoices, bills, checks, etc.)                            │
│  ✅ Account balances                                                         │
│  ✅ Basic class list                                                        │
│                                                                              │
│  TRANSFERS WITH ISSUES:                                                      │
│  ⚠️ Customer/Sub-customer hierarchy (may flatten)                          │
│  ⚠️ Job costing structure                                                  │
│  ⚠️ Custom fields (may not transfer)                                       │
│  ⚠️ Notes and attachments                                                   │
│  ⚠️ Estimates (may not link properly)                                      │
│  ⚠️ Progress invoicing history                                             │
│                                                                              │
│  DOES NOT TRANSFER:                                                          │
│  ❌ Memorized reports (recreate in QBO)                                     │
│  ❌ Memorized transactions                                                  │
│  ❌ Credit card downloads rules                                             │
│  ❌ Bank feed connections                                                    │
│  ❌ User permissions (re-setup)                                              │
│  ❌ Multi-currency settings                                                 │
│  ❌ Price levels                                                             │
│  ❌ Sales orders                                                             │
│  ❌ Purchase orders (may convert to bills)                                  │
│  ❌ Audit trail                                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Desktop-Only Features Not in QBO

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FEATURES NOT IN QBO                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ENTERPRISE FEATURES NOT IN QBO:                                             │
│  • Advanced inventory                                                        │
│  • FIFO costing                                                              │
│  • Serial/lot tracking                                                       │
│  • Bin location tracking                                                     │
│  • Advanced pricing                                                          │
│  • Barcode scanning                                                          │
│                                                                              │
│  CONTRACTOR EDITION FEATURES:                                                │
│  • Built-in job costing reports (recreate as custom)                        │
│  • Progress invoicing (works differently in QBO)                            │
│  • WIP reports (manual in QBO)                                              │
│  • Unit cost reports                                                         │
│                                                                              │
│  WORKAROUNDS:                                                                │
│  • Use QBO's Projects feature                                               │
│  • Use Classes for job tracking                                              │
│  • Create custom reports                                                     │
│  • Use third-party apps for specialty needs                                 │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Construction-Specific Considerations

### Job/Project Structure

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    JOB STRUCTURE MIGRATION                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  DESKTOP STRUCTURE:                                                          │
│  Customer → Job → Sub-job                                                    │
│  Example:                                                                    │
│  Smith Family (Customer)                                                     │
│    └── 2024-001 Smith Residence (Job)                                       │
│          ├── Phase 1: Foundation                                            │
│          ├── Phase 2: Framing                                               │
│          └── Phase 3: Finishes                                              │
│                                                                              │
│  QBO OPTIONS:                                                                │
│                                                                              │
│  OPTION 1: Sub-Customers                                                     │
│  ─────────────────────────                                                   │
│  Smith Family (Customer)                                                     │
│    └── 2024-001 Smith Residence (Sub-customer)                             │
│                                                                              │
│  • Similar to Desktop structure                                              │
│  • Limited to 4 levels                                                       │
│  • Works for simple structures                                               │
│                                                                              │
│  OPTION 2: Projects (QBO Plus/Advanced)                                      │
│  ─────────────────────────────────────                                       │
│  Customer: Smith Family                                                      │
│  Project: 2024-001 Smith Residence                                          │
│                                                                              │
│  • Better dashboard and reporting                                           │
│  • Time tracking integration                                                 │
│  • Recommended for QBO                                                       │
│                                                                              │
│  OPTION 3: Classes for Jobs                                                  │
│  ────────────────────────────                                                │
│  Customer: Smith Family                                                      │
│  Class: 2024-001 Smith Residence                                            │
│                                                                              │
│  • Most flexible for reporting                                              │
│  • Works across all transaction types                                       │
│  • Can use hierarchical classes                                             │
│                                                                              │
│  RECOMMENDATION: Use Projects + Classes for best tracking                   │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Progress Invoicing Migration

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PROGRESS INVOICING CHANGES                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  IN DESKTOP:                                                                 │
│  • Create estimate                                                           │
│  • Invoice against estimate (% or amount)                                   │
│  • System tracks billed vs remaining                                        │
│                                                                              │
│  IN QBO:                                                                     │
│  • Create estimate                                                           │
│  • "Create invoice" from estimate                                           │
│  • Select which items/amounts to bill                                       │
│  • Similar but different interface                                          │
│                                                                              │
│  MIGRATION CHALLENGE:                                                        │
│  ─────────────────────                                                       │
│  Partially-billed estimates may not migrate cleanly.                        │
│                                                                              │
│  SOLUTION:                                                                   │
│  1. Document all open estimates and billing status                          │
│  2. After migration, verify estimate balances                               │
│  3. Manually adjust QBO estimates if needed                                 │
│  4. Or start fresh with new estimates post-migration                        │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Retainage Handling

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    RETAINAGE MIGRATION                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  QBO doesn't have built-in retainage tracking like Desktop Contractor.      │
│                                                                              │
│  MIGRATION APPROACH:                                                         │
│                                                                              │
│  1. DOCUMENT CURRENT RETAINAGE                                               │
│     Before migration, list:                                                  │
│     • Retainage receivable by job/customer                                  │
│     • Retainage payable by job/vendor                                       │
│                                                                              │
│  2. SET UP ACCOUNTS IN QBO                                                   │
│     • Retainage Receivable (Asset)                                          │
│     • Retainage Payable (Liability)                                         │
│                                                                              │
│  3. ENTER OPENING BALANCES                                                   │
│     Journal entry or individual transactions                                │
│     to establish retainage balances                                         │
│                                                                              │
│  4. SET UP WORKFLOW                                                          │
│     See: [Retention Tracking Guide](../tutorials/06-retention-tracking.md)  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Step-by-Step Migration Process

### Phase 1: Preparation (1-2 weeks before)

```
□ Complete all bank reconciliations in Desktop
□ Clear undeposited funds
□ Clean up lists (merge duplicates, make inactive)
□ Document custom fields and their usage
□ Export memorized reports (for recreation)
□ Create full backup
□ Document open estimates and progress billing status
□ Document retainage balances by job
□ Choose migration date (month-end recommended)
```

### Phase 2: Migration Day

```
□ Complete month-end close in Desktop
□ Create final backup
□ Run migration tool (or begin manual setup)
□ Wait for conversion to complete
□ Do NOT enter transactions in Desktop after this point
```

### Phase 3: Verification (1-2 weeks after)

```
□ Compare account balances (TB to TB)
□ Verify customer balances (AR aging)
□ Verify vendor balances (AP aging)
□ Check open estimates/progress billing
□ Verify retainage balances
□ Run P&L and compare
□ Run Balance Sheet and compare
□ Test job cost reports
□ Verify class assignments
□ Check for missing transactions
```

### Phase 4: Go-Live

```
□ Connect bank feeds
□ Set up user accounts and permissions
□ Configure recurring transactions
□ Set up invoicing templates
□ Train team on QBO
□ Begin entering new transactions
□ Close the books on converted period
```

---

## Post-Migration Verification

### Critical Checks

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    VERIFICATION CHECKLIST                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  TRIAL BALANCE:                                                              │
│  □ Total assets match                                                        │
│  □ Total liabilities match                                                   │
│  □ Equity matches                                                            │
│  □ Debits = Credits                                                          │
│                                                                              │
│  ACCOUNTS RECEIVABLE:                                                        │
│  □ AR aging total matches                                                   │
│  □ Spot check 5-10 customer balances                                        │
│  □ Verify open invoices                                                      │
│  □ Check retainage receivable separately                                    │
│                                                                              │
│  ACCOUNTS PAYABLE:                                                           │
│  □ AP aging total matches                                                   │
│  □ Spot check 5-10 vendor balances                                          │
│  □ Verify open bills                                                         │
│  □ Check retainage payable separately                                       │
│                                                                              │
│  BANK ACCOUNTS:                                                              │
│  □ Each bank balance matches                                                │
│  □ Reconciled dates correct                                                  │
│                                                                              │
│  JOB COSTS:                                                                  │
│  □ P&L by job matches (sample jobs)                                         │
│  □ Class assignments correct                                                 │
│  □ Revenue by job matches                                                    │
│  □ Costs by job match                                                        │
│                                                                              │
│  LISTS:                                                                      │
│  □ Customer count correct                                                   │
│  □ Vendor count correct                                                     │
│  □ Item/service list complete                                               │
│  □ Chart of accounts complete                                               │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Variance Investigation

```
If balances don't match:

1. Identify the difference amount
2. Check common issues:
   • Uncleared transactions
   • Pending transactions not converted
   • Rounding differences
   • Date cutoff issues
3. Search for transaction matching the difference
4. Make adjusting entry if needed (with documentation)
```

---

## Common Problems and Solutions

### Problem: Balances Don't Match

```
SYMPTOMS:
• AR total different between systems
• AP total different
• Bank account off

SOLUTIONS:
1. Check date range (ensure same cutoff)
2. Look for pending/uncleared transactions
3. Verify all transactions converted
4. Check for transactions on cutoff date
5. Make adjusting JE if small difference
```

### Problem: Jobs Not Structured Correctly

```
SYMPTOMS:
• Jobs show as customers
• Sub-jobs not linked
• Can't run job reports

SOLUTIONS:
1. Edit customers to make sub-customers
2. Assign to correct parent
3. Use Classes for job tracking
4. Set up Projects for better tracking
```

### Problem: Progress Invoicing History Lost

```
SYMPTOMS:
• Estimates show wrong billed amount
• Can't see prior invoices against estimate
• Progress billing confusing

SOLUTIONS:
1. Keep Desktop available for history reference
2. Document billing history separately
3. Manually adjust estimate balances in QBO
4. Start fresh estimates for new billing
```

### Problem: Retainage Not Tracked

```
SYMPTOMS:
• No retainage accounts
• Balances not separated
• Can't identify retainage by job

SOLUTIONS:
1. Create retainage accounts
2. Enter opening balance JE
3. Set up new workflow per retention guide
4. Track going forward
```

---

## Running Parallel Systems

### Parallel Period Recommendations

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PARALLEL OPERATIONS                                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  OPTION 1: No Parallel (Cutover)                                             │
│  ───────────────────────────────                                             │
│  • Pick a date, switch completely                                           │
│  • Keep Desktop read-only for reference                                     │
│  • Risk: Problems discovered too late                                       │
│  • Best for: Small, simple operations                                       │
│                                                                              │
│  OPTION 2: Short Parallel (1-2 weeks)                                        │
│  ────────────────────────────────────                                        │
│  • Enter transactions in both systems                                       │
│  • Compare results                                                           │
│  • Catch issues quickly                                                      │
│  • Best for: Most contractors                                               │
│                                                                              │
│  OPTION 3: Extended Parallel (1 month)                                       │
│  ─────────────────────────────────────                                       │
│  • Full month in both systems                                               │
│  • Complete month-end in both                                               │
│  • Compare all reports                                                       │
│  • Best for: Complex operations, first migration                            │
│                                                                              │
│  PARALLEL PERIOD TASKS:                                                      │
│  ─────────────────────                                                       │
│  □ Enter all transactions in both systems                                   │
│  □ Compare weekly totals                                                    │
│  □ Investigate differences immediately                                      │
│  □ Make same adjustments in both                                            │
│  □ At end of parallel: Final comparison                                     │
│  □ Document any acceptable differences                                      │
│  □ Cut over to QBO only                                                     │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### When to Abandon Desktop

```
After successful migration:

KEEP DESKTOP FOR:
• Historical reference (keep read-only)
• Looking up old transactions
• Answering audit questions
• Backup for emergency

DO NOT:
• Enter new transactions in Desktop
• Change historical data
• Keep two books going indefinitely

TIMELINE:
• 3 months: Occasional reference
• 6 months: Rare reference
• 1 year: Archive Desktop file
• 3 years: Maintain archive for audit support
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MIGRATION QUICK REFERENCE                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  BEFORE MIGRATION:                                                           │
│  • Clean up Desktop file                                                    │
│  • Document custom setups                                                   │
│  • Complete reconciliations                                                 │
│  • Create backup                                                             │
│                                                                              │
│  MIGRATION:                                                                  │
│  • Use official migration tool OR                                           │
│  • Start fresh with opening balances                                        │
│                                                                              │
│  AFTER MIGRATION:                                                            │
│  • Compare Trial Balance                                                    │
│  • Verify AR and AP                                                         │
│  • Check job structure                                                      │
│  • Set up bank feeds                                                        │
│  • Configure users                                                           │
│  • Train team                                                                │
│                                                                              │
│  CONSTRUCTION FOCUS:                                                         │
│  • Jobs → Sub-customers or Projects + Classes                               │
│  • Retainage → Manual setup required                                        │
│  • Progress invoicing → Test workflow                                       │
│  • Job costs → Verify by class                                              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

After successful migration:
- [Getting Started](../02-getting-started.md) - QBO basics
- [Job Costing Setup](../tutorials/03-job-costing-setup.md) - Configure job tracking
- [Chart of Accounts](../templates/09-chart-of-accounts.md) - Review/optimize COA

---

*[Back to Main Guide](../../README.md)*
