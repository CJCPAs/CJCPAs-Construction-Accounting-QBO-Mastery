# Connecting Bank Accounts in QuickBooks Online

## Overview

Connecting your bank accounts is one of the first and most critical setup steps in QBO. This chapter provides step-by-step instructions for linking your business bank accounts, understanding bank feeds, and properly categorizing transactions for construction accounting.

---

## Why Connect Your Bank Accounts?

### The Manual Entry Problem

```
WITHOUT BANK CONNECTION:
1. Write a check
2. Log into bank website
3. Wait for check to clear
4. Manually enter into QBO
5. Hope you didn't make typos
6. Reconcile at month end... discover errors

RESULT: Hours wasted, errors everywhere
```

### The Bank Feed Solution

```
WITH BANK CONNECTION:
1. Write a check (or use debit card)
2. Transaction appears in QBO automatically
3. Categorize with one click
4. Already matched for reconciliation

RESULT: Minutes instead of hours, fewer errors
```

---

## Step-by-Step: Connecting Your Bank Account

### Step 1: Gather Your Information

Before you start, have ready:
- [ ] Online banking username and password
- [ ] Security question answers (some banks require them)
- [ ] Phone for two-factor authentication codes
- [ ] Account numbers (for verification)

### Step 2: Navigate to Bank Connections

**HOW:**
1. Log into QuickBooks Online
2. Click **Banking** in the left navigation menu
3. Click **Connect account** (or **Add account** if you have existing connections)

```
┌─────────────────────────────────────────────────────────────────┐
│  QuickBooks Online                                              │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ☰ Dashboard                                                     │
│                                                                  │
│  💰 Banking  ◄─── Click here                                    │
│                                                                  │
│  📊 Sales                                                        │
│                                                                  │
│  📋 Expenses                                                     │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Step 3: Search for Your Bank

**HOW:**
1. In the search box, type your bank's name
2. Select your bank from the list
3. If your bank isn't listed, try alternate names (e.g., "Bank of America" vs "BofA")

**Common Banks:**
- Chase
- Bank of America
- Wells Fargo
- US Bank
- PNC
- TD Bank
- Capital One
- Regional/local banks

**If Your Bank Isn't Listed:**
1. Check if your bank has a different official name
2. Try searching by city/state + "bank"
3. Contact your bank to ask if they support Intuit/QuickBooks connections
4. As last resort, use manual import (CSV files)

### Step 4: Enter Your Bank Credentials

**HOW:**
1. Enter your online banking username
2. Enter your online banking password
3. Click **Continue** or **Sign in**

```
┌─────────────────────────────────────────────────────────────────┐
│                    CONNECT TO [BANK NAME]                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Username: [_______________________]                             │
│                                                                  │
│  Password: [_______________________]                             │
│                                                                  │
│  🔒 Your credentials are encrypted and secure                   │
│                                                                  │
│                              [Continue]                          │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**SECURITY NOTE:**
- QBO uses bank-grade encryption
- Your credentials are not stored by Intuit
- Connection goes through secure third-party aggregators (Plaid, Yodlee)

### Step 5: Complete Security Verification

Most banks require additional verification:

**Common Verification Methods:**
1. **Security Questions**: Answer the questions you set up with your bank
2. **SMS Code**: Enter code texted to your phone
3. **Email Code**: Enter code sent to your email
4. **Authenticator App**: Enter code from Google Authenticator, etc.

**HOW:**
1. Select your preferred verification method
2. Enter the code or answer questions
3. Click **Verify** or **Continue**

### Step 6: Select Accounts to Connect

After verification, QBO shows all available accounts:

```
┌─────────────────────────────────────────────────────────────────┐
│           SELECT ACCOUNTS TO CONNECT                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ☑ Business Checking ****1234              $45,678.90           │
│                                                                  │
│  ☑ Payroll Checking ****5678               $12,345.67           │
│                                                                  │
│  ☐ Personal Savings ****9012               $5,000.00            │
│     (Don't connect personal accounts!)                          │
│                                                                  │
│  ☑ Business Savings ****3456               $25,000.00           │
│                                                                  │
│                              [Connect]                           │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**CRITICAL - Select Only Business Accounts:**
- ✅ Operating/Checking account
- ✅ Payroll account (if separate)
- ✅ Business savings
- ✅ Business money market
- ❌ Personal accounts (keep these OUT of business books!)

### Step 7: Map Accounts to QBO

For each connected account, QBO asks you to map it to a Chart of Accounts entry:

**HOW:**
1. For each bank account, select the matching QBO account
2. If no matching account exists, create one

**Mapping Examples:**

| Bank Account | Map To QBO Account | Account Type |
|--------------|-------------------|--------------|
| Business Checking ****1234 | 10000 Checking - Operating | Bank |
| Payroll Checking ****5678 | 10100 Checking - Payroll | Bank |
| Business Savings ****3456 | 10200 Savings | Bank |

**HOW to Create New Account During Setup:**
1. In the dropdown, select **+ Add new**
2. Fill in:
   - **Account Type**: Bank
   - **Detail Type**: Checking (or Savings)
   - **Name**: Descriptive name (e.g., "Operating Account - Chase")
   - **Number**: Your account numbering (e.g., 10000)
3. Click **Save and Close**

### Step 8: Select Date Range for Import

QBO will ask how much transaction history to import:

**Options:**
- Last 90 days (recommended for new setup)
- Last 6 months
- Last 12 months
- Custom date range

**RECOMMENDATION:**
```
For new QBO setup: Start with 90 days or your "go-live" date
For migration: Import from your conversion date forward

WHY: Importing too much history creates a massive backlog
     to categorize and may duplicate data you've already entered
```

### Step 9: Confirm and Connect

1. Review your selections
2. Click **Connect** or **Finish**
3. Wait for initial sync (may take several minutes)

---

## Understanding the Bank Feed

### What You'll See After Connection

Once connected, go to **Banking** to see your bank feed:

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  BANKING                                                                             │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Checking - Operating         Last updated: Today 8:15 AM        Balance: $45,678.90│
│  ├─ For Review (23)                                                                  │
│  ├─ Categorized (0)                                                                  │
│  └─ Excluded (2)                                                                     │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  FOR REVIEW                                              [Add]  [Match]  [Transfer] │
│  ┌────────────────────────────────────────────────────────────────────────────────┐ │
│  │ ☐  03/15  CHECK 1234           Home Depot              -$1,234.56   [Categorize]│ │
│  │ ☐  03/14  ACH PAYMENT          ABC Subcontractor       -$5,000.00   [Categorize]│ │
│  │ ☐  03/14  DEPOSIT              Smith Residence         +$10,000.00  [Match]     │ │
│  │ ☐  03/13  CARD PURCHASE        Lowe's                   -$456.78   [Categorize]│ │
│  └────────────────────────────────────────────────────────────────────────────────┘ │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Bank Feed Status Tabs

| Tab | Meaning | Action Needed |
|-----|---------|---------------|
| **For Review** | New transactions awaiting categorization | Categorize each one |
| **Categorized** | Transactions you've accepted but not yet added | Click to add to books |
| **Excluded** | Transactions you've marked to ignore | None (review periodically) |
| **Recognized** | QBO auto-matched based on rules | Review and accept |

---

## Categorizing Bank Transactions

### The Three Options

For each bank transaction, you have three choices:

```
┌─────────────────────────────────────────────────────────────────┐
│     CATEGORIZE THIS TRANSACTION                                  │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌─────────┐   ┌─────────┐   ┌──────────┐                       │
│  │   ADD   │   │  MATCH  │   │ TRANSFER │                       │
│  │         │   │         │   │          │                       │
│  │ Create  │   │ Link to │   │ Move     │                       │
│  │ new     │   │ existing│   │ between  │                       │
│  │ expense │   │ invoice │   │ accounts │                       │
│  │ or      │   │ or bill │   │          │                       │
│  │ deposit │   │         │   │          │                       │
│  └─────────┘   └─────────┘   └──────────┘                       │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Option 1: ADD (Create New Transaction)

**Use When:**
- No existing invoice, bill, or expense for this transaction
- It's a new expense not yet recorded
- It's a new deposit not yet recorded

**HOW to Add an Expense:**
1. Click on the transaction
2. In the expanded panel:
   - **Vendor**: Select or create vendor (e.g., Home Depot)
   - **Category**: Select expense account (e.g., 51100 Lumber & Framing)
   - **Customer**: Assign to project (CRITICAL for job costing!)
   - **Billable**: Check if you'll bill this to customer
   - **Memo**: Add description if needed
3. Click **Add**

**Example - Adding a Material Purchase:**
```
Transaction: CHECK 1234 - Home Depot -$1,234.56

Fill in:
┌─────────────────────────────────────────────────────────────────┐
│  Vendor:    [Home Depot               ▼]                        │
│  Category:  [51100 Lumber & Framing   ▼]                        │
│  Customer:  [2024-015-Johnson-Kitchen ▼]  ◄── ASSIGN TO JOB!    │
│  ☑ Billable                                                     │
│  Memo:      [Framing lumber for kitchen addition]               │
│                                                                  │
│                                    [Add]  [Cancel]              │
└─────────────────────────────────────────────────────────────────┘
```

### Option 2: MATCH (Link to Existing Transaction)

**Use When:**
- You've already entered an invoice (for deposits)
- You've already entered a bill (for payments)
- It's a payment against an existing payable

**HOW to Match a Deposit to Invoice:**
1. Click on the deposit transaction
2. Click **Match** tab (or it may auto-suggest)
3. QBO shows possible matches
4. Select the matching invoice(s)
5. Click **Match**

**Example - Matching Customer Payment:**
```
Bank Transaction: DEPOSIT - Smith Residence +$10,000.00

QBO suggests:
┌─────────────────────────────────────────────────────────────────┐
│  POSSIBLE MATCHES                                                │
├─────────────────────────────────────────────────────────────────┤
│  ☑ Invoice #1045  Smith Residence  03/01/24  $10,000.00  ✓ MATCH│
│  ☐ Invoice #1032  Smith Residence  02/15/24  $8,500.00          │
│                                                                  │
│                                    [Match]  [Cancel]            │
└─────────────────────────────────────────────────────────────────┘
```

**HOW to Match a Bill Payment:**
1. Click on the payment/check transaction
2. Click **Match** tab
3. Select the bill being paid
4. Click **Match**

### Option 3: TRANSFER (Move Between Accounts)

**Use When:**
- Moving money between your bank accounts
- Owner contributions or distributions (to/from equity)
- Loan proceeds or payments (to/from liability)

**HOW to Record a Transfer:**
1. Click on the transaction
2. Click **Transfer** tab
3. Select the account money is moving to/from
4. Click **Transfer**

**Example - Transfer Between Accounts:**
```
Transaction: ACH TRANSFER -$15,000.00 (in Operating account)

Transfer to: [Savings Account ▼]

Result:
Operating Account: -$15,000
Savings Account: +$15,000 (creates matching entry)
```

---

## Setting Up Bank Rules

### Why Bank Rules Save Hours

Bank rules automatically categorize recurring transactions.

**Without Rules:**
Every month you manually categorize:
- Electric bill → Utilities expense
- Phone bill → Telephone expense  
- Same vendors over and over

**With Rules:**
QBO auto-categorizes based on your rules:
- "ELECTRIC COMPANY" → 61300 Utilities
- "AT&T WIRELESS" → 63300 Telephone
- "HOME DEPOT" → Suggest 51000 Materials

### Creating a Bank Rule

**HOW:**
1. Go to **Banking** → **Rules** (or use gear icon)
2. Click **New rule**
3. Set up the rule:

```
┌─────────────────────────────────────────────────────────────────┐
│                    CREATE BANK RULE                              │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Rule name: [Electric Bill Auto-Categorize]                      │
│                                                                  │
│  WHEN                                                            │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Bank text [contains ▼] [POWER COMPANY           ]           ││
│  │ Transaction type [Expense ▼]                                ││
│  │ Amount [Any ▼]                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                  │
│  THEN                                                            │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Assign to category: [61300 Utilities ▼]                     ││
│  │ Assign to vendor: [Local Power Company ▼]                   ││
│  │ Assign to customer: [Leave blank for overhead]              ││
│  │                                                             ││
│  │ ☑ Automatically add to my books (auto-confirm)              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                  │
│                              [Save]  [Cancel]                    │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Recommended Rules for Construction Companies

| Rule Name | Bank Text Contains | Category | Customer |
|-----------|-------------------|----------|----------|
| Electric | ELECTRIC, POWER CO | 61300 Utilities | (blank) |
| Phone | ATT, VERIZON, TMOBILE | 63300 Telephone | (blank) |
| Fuel - Non Job | SHELL, CHEVRON, EXXON | 62200 Fuel - Non-Job | (blank) |
| Office Supplies | STAPLES, OFFICE DEPOT | 63100 Office Supplies | (blank) |
| Insurance | STATE FARM, NATIONWIDE | 64000 Insurance | (blank) |

**For Job-Specific Vendors:**
Be careful with rules for job costs - you may need to assign different customers each time. Consider rules that pre-fill the vendor but let you choose the customer.

---

## Bank Reconciliation Basics

### Why Reconcile?

Reconciliation ensures your QBO balance matches your actual bank balance. It catches:
- Missing transactions
- Duplicate entries
- Errors
- Fraud

### Monthly Reconciliation Process

**HOW:**
1. Go to **Accounting** → **Reconcile** (or Settings → Reconcile)
2. Select the bank account
3. Enter statement information:
   - Statement ending date
   - Ending balance (from bank statement)
4. Check off each transaction that appears on your statement
5. Difference should equal $0
6. Click **Finish now**

```
┌─────────────────────────────────────────────────────────────────┐
│              RECONCILE: OPERATING ACCOUNT                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Statement Ending Date: [03/31/2024]                            │
│  Statement Ending Balance: [$45,678.90]                          │
│                                                                  │
│  ──────────────────────────────────────────────────────────────  │
│                                                                  │
│  Beginning Balance:          $42,000.00                          │
│  ☑ Cleared Deposits:        +$50,000.00                          │
│  ☑ Cleared Payments:        -$46,321.10                          │
│  ──────────────────────────────────────────────────────────────  │
│  Cleared Balance:            $45,678.90                          │
│  Statement Balance:          $45,678.90                          │
│  Difference:                      $0.00  ✓                       │
│                                                                  │
│                        [Finish now]  [Save for later]            │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Troubleshooting Bank Connections

### Common Issues and Fixes

| Issue | Cause | Solution |
|-------|-------|----------|
| **Connection error** | Bank changed security | Disconnect and reconnect |
| **No transactions downloading** | Account not linked properly | Check account mapping |
| **Duplicate transactions** | Manual + bank feed entry | Delete duplicate, set rule to match |
| **"Action Required"** | Bank needs re-authentication | Click to re-enter credentials |
| **Transactions from wrong account** | Mapping error | Update account mapping |

### Refreshing a Stuck Connection

**HOW:**
1. Go to **Banking**
2. Click on the account with issues
3. Click the **Update** button (or pencil icon → **Edit sign-in info**)
4. Re-enter credentials if prompted
5. Complete any security verification

### Disconnecting and Reconnecting

**When to Use:**
- Persistent connection errors
- After changing bank password
- Bank migrated to new system

**HOW:**
1. Go to **Banking**
2. Click pencil icon next to account
3. Click **Disconnect this account on save**
4. Save
5. Add the connection fresh (follow steps above)

---

## Best Practices for Bank Feeds

### Daily/Weekly Habits

- [ ] Review bank feed 2-3 times per week minimum
- [ ] Categorize transactions promptly (don't let backlog build)
- [ ] Always assign Customer for job costs
- [ ] Review auto-categorized transactions (rules can be wrong)

### Monthly Habits

- [ ] Reconcile all accounts by the 10th
- [ ] Review and update bank rules
- [ ] Check for unreconciled items from prior months
- [ ] Verify no personal transactions in business accounts

### Red Flags to Watch For

- [ ] Transactions you don't recognize
- [ ] Duplicate vendor payments
- [ ] Missing expected deposits
- [ ] Checks cleared out of sequence
- [ ] Unusual transfers

---

*[← Previous: Getting Started](../02-getting-started.md) | [Next: Connecting Credit Cards →](./02-connecting-credit-cards.md)*
