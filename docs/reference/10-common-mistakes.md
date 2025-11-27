# Common Mistakes in Construction Bookkeeping

## Overview

After reviewing thousands of construction company books, certain mistakes appear repeatedly. This chapter catalogs the most common errors, explains why they're problematic, and provides actionable fixes.

---

## Category 1: Setup Mistakes

### Mistake #1: Using QBO Simple Start or Essentials

**The Problem:**
These subscription levels lack essential features:
- No Project tracking
- No Class tracking
- No budgeting
- No inventory

**Why It's Critical:**
Without these features, job costing is impossible. You're flying blind on project profitability.

**The Fix:**
Upgrade to QBO Plus (minimum) or QBO Advanced (recommended for construction).

**Cost-Benefit:**
```
Monthly cost difference: ~$35-80
Cost of not knowing a job is losing money: $10,000+
```

---

### Mistake #2: Using Cash Basis Accounting for Job Costing

**The Problem:**
Cash basis recognizes transactions when cash moves, not when work is performed.

**Why It's Critical:**
```
Cash Basis Reality:
January: Buy $50K materials (cash expense)
February: Do work, no billing yet
March: Bill customer $150K (cash income)

Cash Basis Income Statement:
January: Revenue $0, Expense $50K = Loss ($50K)
February: Revenue $0, Expense $0 = Break even
March: Revenue $150K, Expense $0 = Profit $150K

Actual Job Profitability: $100K (need accrual to see this)
```

**The Fix:**
1. Set QBO to Accrual basis for internal reporting
2. Work with CPA on tax method choice (small contractors may still file cash)
3. Always run job cost reports on accrual basis

---

### Mistake #3: No Naming Convention for Projects/Jobs

**The Problem:**
Jobs named inconsistently:
- "Smith project"
- "123 Main Street"
- "smith"
- "SMITH KITCHEN"

**Why It's Critical:**
- Hard to find jobs in searches
- Sorting doesn't work
- Duplicates get created
- Reports are messy

**The Fix:**
Establish and document a naming convention:
```
Recommended: YYYY-###-ClientName-Description
Example: 2024-015-Johnson-KitchenRemodel
```

Train all users. Update existing jobs if practical.

---

### Mistake #4: Not Using Projects (Relying Only on Customers)

**The Problem:**
Using Customer names as jobs instead of QBO's Project feature.

**Why It's Critical:**
Projects provide:
- Single dashboard for all job activity
- Time tracking association
- Profitability reports
- Milestone tracking

Without Projects, you lose these features.

**The Fix:**
Enable Projects (Settings → Advanced → Projects). Create sub-projects under customers for each job.

---

## Category 2: Transaction Entry Mistakes

### Mistake #5: Not Assigning Transactions to Projects

**The Problem:**
Expenses entered without Customer/Project assignment.

**Why It's Critical:**
```
Bill Entered Without Project Assignment:
Vendor: ABC Lumber
Amount: $5,000
Customer: [blank]

Result:
- $5,000 shows in total COGS
- Job A job cost report: $0 lumber
- Job profitability overstated by $5,000
```

**The Fix:**
1. Make Customer field required (train staff)
2. Run weekly "Transaction List by Customer" filtered for blank customer
3. Correct any unassigned transactions
4. Review before month-end close

---

### Mistake #6: Using Wrong Expense Accounts

**The Problem:**
Transactions coded to incorrect accounts:
- Labor expense coded to Materials
- Subcontractor expense coded to Supplies
- Job costs coded to Overhead

**Why It's Critical:**
- Job cost reports by category are wrong
- Cost analysis is meaningless
- Estimating has bad data

**The Fix:**
1. Review Chart of Accounts with all data entry staff
2. Create clear Products/Services with correct default accounts
3. Monthly review of account balances for anomalies
4. Training for anyone entering transactions

---

### Mistake #7: Not Tracking Retention Separately

**The Problem:**
Retention buried in regular AR/AP or not tracked at all.

**Why It's Critical:**
```
Invoice: $100,000
Retention: $10,000
Customer pays: $90,000

Wrong Way (no retention tracking):
AR shows: $10,000 outstanding (but it's retention, not delinquent!)
AP aging looks bad, collection efforts wasted

Right Way:
Trade AR: $0 (fully collected)
Retention AR: $10,000 (separate account, expected at job completion)
```

**The Fix:**
1. Create separate Retention Receivable and Retention Payable accounts
2. Use negative line item on invoices for retention withheld
3. Track by project for release at completion

---

### Mistake #8: Billing Unapproved Change Orders

**The Problem:**
Including pending change orders on progress billings.

**Why It's Critical:**
- Customer may reject the CO
- You've recorded revenue you may not collect
- Creates disputes
- Overstates AR

**The Fix:**
1. Only bill APPROVED change orders (signed documentation required)
2. Track pending CO costs separately
3. Train PMs on approval-before-work policy

---

### Mistake #9: Ignoring Equipment Costs in Job Costing

**The Problem:**
Not allocating owned equipment costs to jobs.

**Why It's Critical:**
```
Job A uses your excavator for 3 weeks
Job A costs show: $0 equipment

Reality:
Equipment depreciation: $3,000
Insurance: $500
Maintenance: $200
Total real cost: $3,700

Job A is actually $3,700 less profitable than it appears
```

**The Fix:**
1. Calculate internal equipment rates
2. Track equipment usage by job
3. Allocate monthly via journal entry or internal bills
4. Include in estimating for future jobs

---

### Mistake #10: Entering Bills as Expenses

**The Problem:**
Using "Expense" form instead of "Bill" for vendor invoices.

**Why It's Critical:**
- Can't track AP aging
- No due dates for payment management
- Duplicates when bill arrives
- Vendor payment history fragmented

**The Fix:**
Use "Expense" only for immediate payments (debit/credit card, petty cash).
Use "Bill" for anything that will be paid later.

---

## Category 3: Reporting Mistakes

### Mistake #11: Not Running WIP Analysis

**The Problem:**
Never calculating Work in Progress or over/under billing.

**Why It's Critical:**
- Don't know true earned revenue
- Financial statements may be materially wrong
- Bonding company requires WIP
- Can't identify billing problems

**The Fix:**
1. Build WIP schedule (see Chapter 4)
2. Run monthly, minimum quarterly
3. Train PM's on cost-to-complete updates
4. Make adjusting entries for CIE/BIE

---

### Mistake #12: No Job Profitability Review

**The Problem:**
Never running or reviewing job-level profit reports.

**Why It's Critical:**
```
Without Review:
Job A losing $20K? → Don't know
Job B at 5% margin? → Don't know
Job C has scope creep? → Don't know

You find out when:
- Bank account is empty
- Bonding company reviews your financials
- Tax time reveals losses
```

**The Fix:**
1. Run Project Profitability report weekly
2. Review any job below target margin
3. PM's explain variances
4. Action items for troubled jobs

---

### Mistake #13: Using Wrong Report Date Range

**The Problem:**
Running job cost reports for wrong period or all time.

**Why It's Critical:**
```
Report: "All Dates"
Shows: Job A has $500K revenue

Reality: Job A started 3 years ago
This Year: $50K revenue
WIP needs THIS year data, not all time
```

**The Fix:**
1. Match report period to analysis need
2. For active jobs: use project start date to current
3. For monthly analysis: use specific month
4. Document report parameters

---

### Mistake #14: Not Reconciling WIP to GL

**The Problem:**
WIP schedule numbers don't match QBO data.

**Why It's Critical:**
- Two sets of books (which is right?)
- Audit nightmare
- Bank/bonding company questions
- Can't trust either report

**The Fix:**
1. Build WIP from QBO data
2. Reconcile WIP totals to GL balances
3. Document any differences
4. Investigate and fix discrepancies

---

## Category 4: Process Mistakes

### Mistake #15: No Month-End Close Process

**The Problem:**
Month-end happens whenever, if ever.

**Why It's Critical:**
- Data entry catches up weeks later
- Reports are never "final"
- Trends not visible
- Decision-making delayed

**The Fix:**
1. Establish close calendar (e.g., books closed by 10th)
2. Create close checklist (see Chapter 11)
3. Make specific person responsible
4. Review and sign off

---

### Mistake #16: Bookkeeper Has No Construction Experience

**The Problem:**
Generic bookkeeper unfamiliar with construction accounting.

**Why It's Critical:**
- Doesn't understand WIP
- Codes labor to wrong accounts
- Ignores retention
- Misses change orders

**The Fix:**
1. Provide construction-specific training (this guide!)
2. Consider construction accounting specialist
3. CPA oversight from construction-focused firm
4. Regular training updates

---

### Mistake #17: PM's Don't Update Cost Estimates

**The Problem:**
Project managers don't provide updated cost-to-complete estimates.

**Why It's Critical:**
```
Original Budget: $800K cost, $200K profit
PM doesn't update despite scope changes

Reality:
Actual cost to complete: $950K
Actual profit: $50K

WIP still shows $200K profit because estimate wasn't updated
→ Financial statements wrong by $150K
```

**The Fix:**
1. Monthly PM meetings to update estimates
2. Make it mandatory, not optional
3. Track historical estimate accuracy
4. Hold PM's accountable for major variances

---

### Mistake #18: Ignoring Bonding Requirements

**The Problem:**
Not maintaining records bonding company needs.

**Why It's Critical:**
- Delayed bond approvals
- Lower bonding capacity
- Higher premiums
- Lost bid opportunities

**The Fix:**
1. Know what your surety requires
2. Maintain WIP schedule
3. Keep job documentation organized
4. Provide financials timely

---

## Category 5: Cash Management Mistakes

### Mistake #19: Not Billing Promptly

**The Problem:**
Progress billing submitted late or inconsistently.

**Why It's Critical:**
```
Contract allows billing on 25th of month
You bill on 10th of next month = 15 days late
Net 30 payment terms
Total delay: 45 days extra

On $100K billing:
Lost interest @ 5%: $617
Working capital tied up unnecessarily
```

**The Fix:**
1. Calendar all billing dates
2. Prepare billing package in advance
3. Submit on or before deadline
4. Track days from work to billing

---

### Mistake #20: Paying Subs Before Getting Paid

**The Problem:**
Paying subcontractors before receiving corresponding payment from customer.

**Why It's Critical:**
- You're financing the job
- Cash flow stress
- Risk if customer doesn't pay
- No leverage for sub performance

**The Fix:**
1. Align sub payment terms with customer receipt
2. "Pay when paid" or "pay if paid" clauses
3. Don't release retention until you receive yours
4. Monitor cash conversion cycle

---

### Mistake #21: Not Tracking Accounts Receivable Aging

**The Problem:**
No one follows up on unpaid invoices.

**Why It's Critical:**
```
AR Aging Ignored:
Invoice from 90 days ago: $50,000
No one noticed → No follow up → Now 180 days
Collection probability drops 50%+
```

**The Fix:**
1. Run AR aging weekly
2. Assign collection responsibility
3. Call at 30 days overdue
4. Escalate at 60 days
5. Consider collection action at 90 days

---

### Mistake #22: Mixing Owner Personal and Business

**The Problem:**
Owner uses business accounts for personal expenses (or vice versa).

**Why It's Critical:**
- Distorts job costs if charged to jobs
- Tax problems
- Bonding company concerns
- Potential legal issues (piercing corporate veil)

**The Fix:**
1. Strict separation of accounts
2. All personal expenses through Owner Draw
3. Monthly owner draw review
4. Educate owner on risks

---

## Mistake Severity Matrix

| Mistake | Financial Impact | Frequency | Fix Difficulty |
|---------|------------------|-----------|----------------|
| No project tracking | HIGH | Very Common | Medium |
| Cash basis job costing | HIGH | Common | Easy |
| Unassigned expenses | HIGH | Very Common | Easy |
| No WIP analysis | HIGH | Common | Medium |
| No retention tracking | MEDIUM | Common | Medium |
| Equipment not allocated | MEDIUM | Very Common | Medium |
| Billing unapproved COs | HIGH | Common | Easy |
| Late billing | MEDIUM | Very Common | Easy |
| Wrong expense accounts | MEDIUM | Common | Easy |
| No month-end close | MEDIUM | Very Common | Medium |

---

## Self-Assessment Checklist

Rate your company (0-2 points each):

**Setup**
- [ ] Using QBO Plus or Advanced
- [ ] Accrual basis for internal reports
- [ ] Consistent naming convention
- [ ] Projects feature enabled

**Transaction Entry**
- [ ] All expenses assigned to projects
- [ ] Correct accounts used
- [ ] Retention tracked separately
- [ ] Only approved COs billed

**Reporting**
- [ ] WIP analysis performed monthly
- [ ] Job profitability reviewed weekly
- [ ] Reports reconcile to GL

**Process**
- [ ] Month-end close by 10th
- [ ] PM's update estimates monthly
- [ ] Bonding requirements maintained

**Cash Management**
- [ ] Bills on time
- [ ] AR aging monitored weekly
- [ ] Business/personal separate

**Scoring:**
- 20-26 points: Excellent - fine-tuning only
- 14-19 points: Good - address gaps
- 8-13 points: Fair - significant improvement needed
- 0-7 points: Poor - major overhaul required

---

*[← Previous: Chart of Accounts](../templates/09-chart-of-accounts.md) | [Next: Month-End Close Checklist →](../checklists/11-month-end-close.md)*
