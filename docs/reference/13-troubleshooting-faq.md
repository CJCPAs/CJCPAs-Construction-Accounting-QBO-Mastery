# Troubleshooting & FAQ for Construction Accounting in QBO

## Overview

This guide addresses the most common problems, questions, and "how do I fix this?" scenarios that construction bookkeepers and accountants encounter in QuickBooks Online.

Organized by category, use this as your go-to reference when something goes wrong or you're not sure how to handle a situation.

---

## Quick Problem Finder

| Problem | Jump To |
|---------|---------|
| Bank feed not downloading | [Bank Connection Issues](#bank-connection-issues) |
| Transaction categorized wrong | [Transaction Corrections](#transaction-corrections) |
| Reconciliation won't balance | [Reconciliation Problems](#reconciliation-problems) |
| Job costs not showing on reports | [Job Costing Issues](#job-costing-issues) |
| Invoice sent to wrong customer | [Invoice Problems](#invoice-problems) |
| Bill entered twice | [Duplicate Entries](#duplicate-entries) |
| WIP schedule doesn't match QBO | [WIP Discrepancies](#wip-discrepancies) |
| 1099 showing wrong amount | [1099 Issues](#1099-issues) |
| Reports look wrong | [Reporting Issues](#reporting-issues) |
| Can't delete a transaction | [Deletion Problems](#deletion-problems) |

---

## Bank Connection Issues

### Problem: Bank Feed Stopped Downloading

**Symptoms:**
- No new transactions appearing
- "Connection needs attention" message
- Last download date is old

**Solutions:**

1. **Refresh the connection:**
   - Go to **Banking** → Click the account → **Update**
   - Wait 24 hours and try again

2. **Re-authenticate:**
   - Go to **Banking** → Account → **Edit** (pencil icon)
   - **Edit sign-in info** → Re-enter bank credentials

3. **Disconnect and reconnect:**
   - Go to **Banking** → Account → **Edit** → **Disconnect**
   - Wait 1 hour
   - Reconnect using **Link Account**

4. **Check bank's end:**
   - Log directly into bank website
   - Accept any new terms/conditions
   - Update security questions if prompted

**Prevention:** Check bank feeds daily. Connections that sit idle can break.

---

### Problem: Duplicate Transactions from Bank Feed

**Symptoms:**
- Same transaction appearing twice
- Double entries in register
- Account balance is off by exact duplicate amounts

**Solutions:**

1. **Delete the duplicate:**
   - Find the duplicate transaction
   - Click to open → **More** → **Delete**

2. **Exclude instead of adding:**
   - In bank feed, if transaction already exists, choose **Match** not **Add**

3. **Check date ranges:**
   - When reconnecting, don't overlap with manually entered transactions

**Prevention:** Always check "For Review" queue before processing. Match existing transactions instead of creating new ones.

---

### Problem: Bank Feed Transaction Has Wrong Amount

**Symptoms:**
- Downloaded amount doesn't match receipt
- Split transaction downloaded as single amount

**Solutions:**

1. **Edit after adding:**
   - Add the transaction from bank feed
   - Open the transaction → Edit amount and splits

2. **If already matched wrong:**
   - Unmatch: Open transaction → **Undo** match
   - Match to correct transaction or add with correct splits

---

## Transaction Corrections

### Problem: Transaction Assigned to Wrong Job/Class

**Symptoms:**
- Job cost report shows expense on wrong project
- P&L by Class is incorrect

**Solutions:**

1. **Edit the transaction:**
   - Find the transaction (Expenses, Bills, etc.)
   - Open → Change the **Customer/Project** or **Class** field
   - Save

2. **For bank feed transactions:**
   - Go to **Banking** → find transaction in register
   - Click to open → Edit **Class** and **Customer**

**Bulk Fix (many transactions):**

If many transactions have wrong job, consider:
1. Export to Excel
2. Identify all incorrect transactions
3. Correct one by one in QBO (no bulk edit for class)

**Prevention:** Train staff on consistent job coding. Review uncategorized transactions weekly.

---

### Problem: Expense Posted to Wrong Account

**Symptoms:**
- Expense showing in wrong category on P&L
- Materials showing as Subcontractor cost (or similar)

**Solutions:**

1. **Edit the transaction:**
   - Find the expense/bill
   - Open → Change the **Category** (Account) field
   - Save

2. **If from bank feed:**
   - Open from banking register
   - Edit the category before or after adding

**If account was correct but now wrong (chart of accounts issue):**
- Check if account was merged or renamed
- Create new account if needed and reclassify

---

### Problem: Transaction Dated in Wrong Period

**Symptoms:**
- Transaction showing in wrong month's reports
- Reconciliation affected
- Financial statements for month are wrong

**Solutions:**

1. **If period is still open:**
   - Edit the transaction → Change date → Save

2. **If period is closed (closing date set):**
   - Option A: Get closing date password from admin, change date
   - Option B: Create adjusting journal entry in correct period

**For Deposited Payments:**
- Can't easily change date after deposit recorded
- May need to delete deposit, change payment dates, recreate deposit

**Prevention:** Review transaction dates during entry. Verify before reconciling.

---

## Reconciliation Problems

### Problem: Bank Reconciliation Won't Balance

**Symptoms:**
- Difference amount showing during reconciliation
- Can't figure out where difference is

**Diagnostic Steps:**

1. **Check beginning balance:**
   - Does beginning balance match bank statement?
   - If not, prior reconciliation has issue

2. **Check for missing transactions:**
   - Compare statement to QBO list
   - Add any missing deposits or checks

3. **Check for duplicates:**
   - Look for transactions cleared twice
   - Uncheck duplicates

4. **Check for altered transactions:**
   - Post-reconciliation edits can cause differences
   - Run reconciliation discrepancy report

5. **Check deposit totals:**
   - Individual items may match but grouped deposit may not
   - Verify grouped deposit amounts match statement

**Common Culprits:**
- Transposed numbers (e.g., $1,234 entered as $1,243)
- Missing checks/deposits
- Transactions edited after prior reconciliation
- Bank fees not recorded

---

### Problem: Beginning Balance Changed

**Symptoms:**
- Reconciliation shows different beginning balance than last month's ending
- Prior period balance won't match

**Causes:**
- Transaction from prior period was edited (amount or date)
- Transaction from prior period was deleted
- Transaction was incorrectly cleared/uncleared

**Solutions:**

1. **Run Reconciliation Discrepancy Report:**
   - **Reports** → "Reconciliation Discrepancy"
   - Shows changed/deleted transactions

2. **Find and fix the changed transaction:**
   - Restore correct amount
   - Ensure it's still marked cleared

3. **If can't identify:**
   - Make adjusting entry to correct balance
   - Document for audit trail

**Prevention:** Set closing date after reconciliation. Don't edit reconciled transactions.

---

### Problem: Credit Card Won't Reconcile

**Symptoms:**
- Credit card balance doesn't match statement
- Payments not reducing balance correctly

**Common Issues:**

1. **Payment recorded wrong:**
   - Should be recorded as **Transfer** from bank to credit card
   - NOT as an expense

2. **Returns/credits not recorded:**
   - Vendor credits reduce balance
   - Check for missing credits

3. **Finance charges/fees missing:**
   - Record interest, fees as expenses
   - They hit the credit card balance too

**Correct Credit Card Payment Entry:**
- **From Account:** Checking
- **To Account:** Credit Card
- **Amount:** Payment amount
- This reduces credit card liability

---

## Job Costing Issues

### Problem: Job Costs Not Showing on Project Reports

**Symptoms:**
- P&L by Customer shows $0 for a project with known expenses
- Job cost report is incomplete

**Causes & Solutions:**

1. **Customer/Project not assigned:**
   - Edit transactions → Add customer to line items
   - All COGS transactions need customer assigned

2. **Using wrong report:**
   - "P&L by Customer" shows income/expense by customer
   - Make sure you're running correct report

3. **Class vs. Customer confusion:**
   - If using Classes for jobs, run "P&L by Class"
   - If using Customers for jobs, run "P&L by Customer"

4. **Date range wrong:**
   - Verify report dates include transaction dates

5. **Sub-customer issue:**
   - Transactions on parent vs. sub-customer
   - Check both levels

---

### Problem: Revenue Showing But No Costs

**Symptoms:**
- Job looks 100% profitable
- Costs are recorded but not appearing

**Solutions:**

1. **Costs in wrong account type:**
   - Costs should be COGS (Cost of Goods Sold) or Expense
   - If in asset account, won't show on P&L

2. **Customer not on cost transactions:**
   - Edit bills/expenses to add customer

3. **Using Products/Services wrong:**
   - Income items should hit revenue accounts
   - Cost items should hit COGS accounts

---

### Problem: Labor Costs Not Tracking to Jobs

**Symptoms:**
- Payroll expense shows but not by job
- No labor cost on job cost reports

**Solutions:**

1. **Time tracking not job-coded:**
   - Ensure time entries have Customer/Project assigned
   - Enable billable time

2. **Payroll not allocated:**
   - Run labor by job report from payroll
   - Create journal entry to allocate labor to jobs

3. **Using external payroll:**
   - Import or journal entry labor costs with customer assignment

**Manual Labor Allocation Journal Entry:**
```
Debit: Direct Labor - Job A     $5,000  (Customer: Job A)
Debit: Direct Labor - Job B     $3,000  (Customer: Job B)
Credit: Payroll Expense         $8,000
```

---

## Invoice Problems

### Problem: Invoice Sent to Wrong Customer

**Symptoms:**
- Invoice shows on wrong customer's statement
- AR is on wrong customer

**Solutions:**

1. **Edit the invoice:**
   - Open invoice → Change customer at top
   - Update any job-specific details
   - Save

2. **If payment already received:**
   - Unapply payment first (edit payment, uncheck invoice)
   - Edit invoice to correct customer
   - Reapply payment if from same customer
   - Or apply to new customer

---

### Problem: Can't Delete Invoice (Has Payments)

**Symptoms:**
- Error when trying to delete invoice
- "Transaction has payments applied"

**Solutions:**

1. **Unapply payments first:**
   - Go to customer → Open payment
   - Uncheck the invoice from payment
   - Save payment
   - Now delete invoice

2. **If payment was deposited:**
   - May need to delete deposit
   - Then unapply payment
   - Then delete invoice
   - Recreate correctly

---

### Problem: Retention Not Calculating Correctly

**Symptoms:**
- Retention amount is wrong on invoice
- 10% retention showing different amount

**Solutions:**

1. **Manual retention calculation:**
   - QBO doesn't auto-calculate retention
   - Add negative line item: "Less 10% Retention"
   - Amount: (Gross billing × 10%) as negative

2. **Retention on wrong items:**
   - Retention typically on labor and materials
   - Not always on stored materials
   - Calculate per contract terms

**Example Retention Invoice:**
```
Rough Framing - Labor             $25,000
Rough Framing - Materials         $15,000
                          Subtotal $40,000
Less: 10% Retention              ($4,000)
                     Total Due    $36,000
```

---

## Duplicate Entries

### Problem: Bill Entered Twice

**Symptoms:**
- AP balance is doubled
- Vendor shows duplicate bills

**Solutions:**

1. **Delete the duplicate:**
   - Find duplicate bill
   - Open → **More** → **Delete**

2. **If already paid:**
   - This is more complex
   - One payment will be orphaned
   - Delete duplicate bill, then address payment

3. **If both paid:**
   - You may have overpaid vendor
   - Contact vendor for refund or credit

**Prevention:**
- Use vendor invoice numbers consistently
- QBO warns of duplicate invoice numbers
- Review AP aging for duplicates before paying

---

### Problem: Payment Recorded Twice

**Symptoms:**
- Bank account shows double payment
- Vendor balance is negative (credit)

**Solutions:**

1. **Delete duplicate payment:**
   - Find duplicate in banking register
   - Delete the incorrect one

2. **If reconciled:**
   - May need to adjust reconciliation
   - Or post correcting entry

---

## WIP Discrepancies

### Problem: WIP Schedule Doesn't Match QBO Costs

**Symptoms:**
- WIP shows different costs than P&L by Customer
- Can't reconcile WIP to books

**Diagnostic Steps:**

1. **Verify date ranges match:**
   - WIP should be "inception to date"
   - QBO report should match period

2. **Check for missing transactions:**
   - Are all bills entered?
   - Any costs in wrong accounts?

3. **Check for wrong customer assignments:**
   - Costs may be on parent vs. sub-customer
   - Or on wrong project entirely

4. **Compare categories:**
   - WIP categories may differ from QBO accounts
   - Reconcile each category

**Common Causes:**
- Accrued costs not in QBO yet
- Committed costs (POs) in WIP but not QBO
- Different cost categorization

---

### Problem: Over/Under Billing Calculation Wrong

**Symptoms:**
- Over/under billing doesn't match WIP
- Balance sheet CIE/BIE accounts wrong

**Solutions:**

1. **Verify formula:**
   ```
   Billings to Date - Earned Revenue = Over/(Under) Billing
   Positive = Over-billed (liability)
   Negative = Under-billed (asset)
   ```

2. **Verify earned revenue calculation:**
   ```
   Earned Revenue = Contract Price × % Complete
   % Complete = Costs to Date ÷ Total Estimated Cost
   ```

3. **Check billings to date:**
   - Should include all invoices issued
   - Including retention billed

---

## 1099 Issues

### Problem: 1099 Showing Wrong Amount

**Symptoms:**
- 1099 total doesn't match what you paid vendor
- Missing payments or extra payments

**Diagnostic Steps:**

1. **Run 1099 Detail Report:**
   - **Reports** → "1099 Transaction Detail"
   - Compare to AP payments by vendor

2. **Check account mapping:**
   - Go to **Expenses** → **1099 Contractor Settings**
   - Verify which accounts are mapped to 1099 boxes

3. **Common causes:**
   - Payments from unmapped accounts
   - Reimbursements included (may not be reportable)
   - Credit card payments (reported by card company)

---

### Problem: Vendor Should Get 1099 But Doesn't

**Symptoms:**
- Vendor paid over $600 but not appearing on 1099 list

**Solutions:**

1. **Check vendor setup:**
   - Open vendor → Edit
   - Verify **Track payments for 1099** is checked
   - Enter TIN

2. **Check account mapping:**
   - Payments may be in unmapped accounts
   - Add accounts to 1099 mapping

3. **Check payment method:**
   - Credit card payments: Card company reports, not you
   - PayPal Business: PayPal may report

---

### Problem: Corporation Incorrectly Getting 1099

**Symptoms:**
- C-Corp or S-Corp showing on 1099 list
- Should be exempt

**Solutions:**

1. **Update vendor entity type:**
   - Open vendor → Edit
   - Change to Corporation (if applicable)
   - QBO should exclude

2. **Manual exclusion:**
   - In 1099 wizard, uncheck vendor
   - Document why (Corporation exempt)

**Note:** Attorneys get 1099s regardless of corporate status.

---

## Reporting Issues

### Problem: Report Shows Wrong Numbers

**Symptoms:**
- P&L doesn't match expectations
- Balance Sheet is off

**Diagnostic Steps:**

1. **Check date range:**
   - Verify "From" and "To" dates
   - "This Year" may not be what you think

2. **Check accounting method:**
   - Report may show Cash vs. Accrual
   - Change in report settings

3. **Check filters:**
   - Report may be filtered by class, customer, etc.
   - Clear filters to see all data

4. **Verify account types:**
   - Wrong account type = wrong report section
   - E.g., expense vs. COGS

---

### Problem: Cash Flow Statement Doesn't Balance

**Symptoms:**
- Cash change doesn't match actual cash change
- Statement doesn't reconcile

**Solutions:**

1. **Verify balance sheet balances:**
   - Opening and closing balance sheets must be correct
   - Cash flow is derived from balance sheet changes

2. **Check for reclassifications:**
   - Accounts that changed type mid-year
   - Manual adjustments needed

3. **QBO limitations:**
   - QBO cash flow isn't always perfect
   - May need manual preparation for audited statements

---

### Problem: P&L by Class Doesn't Match Total P&L

**Symptoms:**
- Sum of all classes ≠ company total
- "Unclassified" amount exists

**Solutions:**

1. **Find unclassified transactions:**
   - Run P&L by Class
   - Click on "Unclassified" column
   - These need class assignment

2. **Assign classes:**
   - Edit each transaction to add class

3. **Prevention:**
   - Make class required for income/expense
   - **Settings** → **Company** → **Categories** → Require class

---

## Deletion Problems

### Problem: Can't Delete Transaction

**Symptoms:**
- Error message when trying to delete
- "Cannot delete" or similar

**Common Causes & Solutions:**

1. **Transaction is reconciled:**
   - Undo reconciliation first, OR
   - Make correcting entry instead of deleting

2. **Transaction has linked items:**
   - Payments linked to invoices
   - Bills linked to purchase orders
   - Delete links first, then parent

3. **Closing date is set:**
   - Transaction before closing date
   - Need closing date password to edit/delete

4. **Permissions issue:**
   - User doesn't have delete rights
   - Admin needs to delete or grant permission

---

### Problem: Deleted Transaction Still Appears

**Symptoms:**
- Deleted item still shows on reports
- Audit log shows delete but data remains

**Solutions:**

1. **Refresh the page:**
   - QBO cache may be stale
   - Hard refresh: Ctrl+Shift+R (or Cmd+Shift+R on Mac)

2. **Check audit log:**
   - **Settings** → **Audit Log**
   - Verify deletion completed

3. **Clear browser cache:**
   - Sometimes QBO displays old data

4. **Check date range:**
   - Transaction might be in different period now

---

## Payroll Issues

### Problem: Payroll Expense Not Splitting to Jobs

**Symptoms:**
- All labor in one account
- No job breakdown of labor costs

**Solutions:**

1. **Use time tracking with payroll:**
   - Enter time by job
   - Payroll uses time entries
   - Labor costs follow time assignments

2. **Manual allocation:**
   - Run payroll by job report
   - Journal entry to reallocate

3. **Check payroll settings:**
   - Ensure job costing is enabled
   - Workers should be entering time by job

---

### Problem: Payroll Taxes Not Matching 941

**Symptoms:**
- QBO payroll reports don't match filed 941
- Withholding amounts differ

**Diagnostic Steps:**

1. **Check for mid-quarter changes:**
   - Rate changes
   - Employee changes

2. **Run payroll tax summary:**
   - Compare to 941 line by line
   - Identify discrepancy

3. **Check for adjustments:**
   - Manual adjustments may not flow to reports
   - Prior quarter corrections

---

## Performance Issues

### Problem: QBO Running Slow

**Symptoms:**
- Pages load slowly
- Reports take forever
- Timeout errors

**Solutions:**

1. **Clear browser cache:**
   - Often fixes performance issues

2. **Use supported browser:**
   - Chrome recommended
   - Keep browser updated

3. **Check internet connection:**
   - QBO needs good connectivity

4. **Reduce list sizes:**
   - Too many customers/vendors/accounts
   - Archive inactive items

5. **Run reports for shorter periods:**
   - Full-year reports take longer
   - Run quarterly if needed

---

## Frequently Asked Questions

### QBO Setup Questions

**Q: Should I use Projects or Classes for jobs?**

**A:** Use **Projects** if:
- You want QBO's built-in project dashboard
- You have QBO Plus or Advanced
- You want to see project profitability easily

Use **Classes** if:
- You have many jobs (Classes scale better)
- You need hierarchical tracking (regions, divisions)
- You're on QBO Simple Start (no Projects)

Many contractors use **both**: Classes for job types/divisions, Projects for individual jobs.

---

**Q: What QBO subscription do I need for construction?**

**A:**
- **QBO Plus** (minimum recommended): Classes, Projects, time tracking, purchase orders
- **QBO Advanced** (best): Everything in Plus + Custom reports, workflows, enhanced support

Avoid QBO Simple Start and Essentials for construction—missing critical features.

---

**Q: Should I use Cash or Accrual basis?**

**A:**
- **Accrual** recommended for construction (GAAP)
- WIP schedules require accrual basis
- Bonding companies expect accrual
- Can run cash basis reports for tax purposes

**Note:** You can maintain books on accrual and provide cash basis to CPA for taxes.

---

### Day-to-Day Questions

**Q: How do I handle retainage?**

**A:**
1. Invoice for full amount earned
2. Add negative line: "Less: Retention"
3. Customer pays net amount
4. At completion, invoice retention release

**Accounts needed:**
- Retention Receivable (Asset) - for billed, not collected retention
- Or track via AR aging

---

**Q: How do I record equipment I own charged to jobs?**

**A:**
1. Calculate internal equipment rate
2. Create "Equipment Charge" service item
3. Bill job for equipment use (internal charge)
4. Credit goes to equipment cost recovery account

Or use journal entry to allocate equipment costs to jobs.

---

**Q: How do I track stored materials?**

**A:**
1. Bill owner for stored materials (with documentation)
2. Track in inventory or note in project
3. When installed, transfer from stored to installed
4. Ensure not billed twice

---

**Q: How do I handle a job that went over budget?**

**A:**
1. Update WIP with actual costs
2. Recognize loss immediately (GAAP requirement)
3. Document what went wrong
4. Communicate with management

For WIP: Estimated gross profit becomes negative. Entire loss should be recognized.

---

### Billing Questions

**Q: How do I bill for a T&M change order on a lump-sum job?**

**A:**
1. Track T&M portion separately
2. Bill T&M with supporting documentation
3. Or add approved CO amount to contract price
4. Bill per revised schedule of values

---

**Q: How do I bill retention release?**

**A:**
1. Create invoice at project completion
2. Reference original retention amounts
3. Billing for "Retention Previously Withheld"
4. Ensure retention account zeroes out

---

**Q: What if customer disputes part of invoice?**

**A:**
1. Document the dispute
2. If agreeing to reduce: Credit memo
3. If fighting: Keep invoice, note dispute
4. Don't write off without resolution
5. Adjust WIP for disputed amounts if significant

---

### Year-End Questions

**Q: How do I handle a job that spans year-end?**

**A:**
1. Update WIP schedule at year-end
2. Recognize earned revenue based on % complete
3. Over/under billing adjustment on balance sheet
4. Continue tracking in new year
5. Reverse WIP entry in January (if using reversal method)

---

**Q: What if I find errors after year-end close?**

**A:**
1. If material: Discuss with CPA, may need to reopen
2. If immaterial: Correct in current year
3. Document the error and correction
4. Consider restating if financials were distributed

---

**Q: How do I correct prior year depreciation?**

**A:**
1. Calculate correct depreciation
2. Make catch-up entry in current year
3. Or restate prior year (if material)
4. Update depreciation schedule going forward

---

### Technical Questions

**Q: How do I merge duplicate customers?**

**A:**
1. **Customers** → Find duplicate
2. Open → **Edit**
3. Change name to exactly match customer you want to keep
4. QBO will prompt to merge
5. **Warning:** Cannot be undone

---

**Q: How do I inactive old jobs?**

**A:**
1. Ensure job is complete (no open AR/AP)
2. Open customer/project
3. Check **Make inactive**
4. Job won't appear in dropdowns
5. History is preserved

---

**Q: Can I undo a bank reconciliation?**

**A:**
1. Go to **Settings** → **Reconcile**
2. **History by account**
3. Select reconciliation → **Undo**
4. Transactions will be uncleared
5. Re-reconcile correctly

---

## Emergency Situations

### "Help! My data looks completely wrong!"

**Immediate Steps:**

1. **Don't panic** - Changes are usually fixable
2. **Stop making changes** - Don't make it worse
3. **Check audit log** - What changed recently?
   - **Settings** → **Audit Log**
4. **Check for common causes:**
   - Closing date removed?
   - Large transaction edited?
   - Data import went wrong?
5. **Consider restoring backup** - QBO has auto-backups
   - Contact QBO support for restore

---

### "Bank account balance is way off!"

**Immediate Steps:**

1. **Compare to bank statement** - What's the actual balance?
2. **Run reconciliation** - See the difference
3. **Check for:**
   - Missing large deposits
   - Duplicate large payments
   - Wrong transaction amounts
4. **Don't force a reconciliation adjustment** - Find the actual issue

---

### "I deleted something important!"

**Options:**

1. **Check audit log** - Get details of what was deleted
2. **Recreate the transaction** - Using audit log info
3. **Contact QBO support** - They may be able to help
4. **Restore from backup** - Last resort, loses recent work

---

## Getting More Help

### QBO Support Resources

1. **QBO Help Center:** Help button in QBO
2. **QBO Community:** community.intuit.com
3. **QBO Support:** Chat or phone through QBO
4. **ProAdvisor:** Hire a certified QBO expert

### When to Call Your CPA

- Year-end adjustments
- Complex revenue recognition
- Tax questions
- Audit preparation
- Major errors affecting financials

### When to Call QBO Support

- Technical issues (won't load, errors)
- Bank connection problems
- Subscription/billing issues
- Data recovery needs

---

## Key Takeaways

1. **Most problems are fixable** - Don't panic
2. **Document your fix** - For future reference
3. **Prevention beats cure** - Good processes avoid issues
4. **Audit log is your friend** - Shows what changed
5. **Don't force reconciliations** - Find actual issues
6. **Back up decision**: Know when to call for help

---

## Related Resources

- [Common Mistakes](./10-common-mistakes.md) - Prevention is best
- [Month-End Close](../checklists/11-month-end-close.md) - Catch issues early
- [Getting Started](../02-getting-started.md) - Setup best practices
- [Job Costing Setup](../tutorials/03-job-costing-setup.md) - Proper job tracking

---

*[← Previous: GAAP Principles](./12-gaap-principles.md) | [Back to Guide Index →](../../README.md)*
