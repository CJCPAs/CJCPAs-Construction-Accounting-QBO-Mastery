# Connecting Credit Cards in QuickBooks Online

## Overview

Credit cards are commonly used in construction for materials, supplies, fuel, and other job-related purchases. Properly connecting and managing credit cards in QBO ensures:
- Complete job costing (nothing falls through the cracks)
- Easy reconciliation at month-end
- Clear tracking of company vs. employee cards

---

## Business Credit Cards vs. Debit Cards

### Key Differences for QBO

| Feature | Credit Card | Debit Card |
|---------|-------------|------------|
| **Account Type in QBO** | Credit Card | Bank |
| **Liability** | Yes (you owe money) | No (draws from bank) |
| **Statement Cycle** | Monthly billing cycle | Real-time from checking |
| **Reconciliation** | Reconcile to CC statement | Reconciles with bank account |

**IMPORTANT:** Don't accidentally set up a credit card as a bank account or vice versa. This creates balance and reconciliation nightmares.

---

## Step-by-Step: Connecting Your Credit Card

### Step 1: Navigate to Bank Connections

**HOW:**
1. Log into QuickBooks Online
2. Click **Banking** in the left navigation
3. Click **Connect account** or **Add account**

### Step 2: Search for Your Credit Card Issuer

**HOW:**
1. Type your credit card company name (e.g., "Chase", "American Express", "Capital One")
2. Select the correct option from the list

**Common Credit Card Issuers:**
- American Express
- Chase
- Capital One
- Discover
- Citi
- US Bank
- Bank of America
- Wells Fargo

### Step 3: Enter Your Credentials

**HOW:**
1. Enter your credit card online account username
2. Enter your password
3. Complete any security verification (codes, questions, etc.)
4. Click **Continue**

### Step 4: Select the Credit Card(s) to Connect

```
┌─────────────────────────────────────────────────────────────────┐
│           SELECT ACCOUNTS TO CONNECT                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ☑ Business Platinum Card ****4567        Balance: $3,456.78    │
│                                                                  │
│  ☑ Company Purchasing Card ****8901       Balance: $1,234.56    │
│                                                                  │
│  ☐ Personal Rewards Card ****2345         Balance: $567.89      │
│     (Don't connect personal cards!)                             │
│                                                                  │
│                              [Connect]                           │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Select Only Business Cards:**
- ✅ Business credit cards
- ✅ Company purchasing cards
- ✅ Fuel cards (if supported)
- ❌ Personal credit cards

### Step 5: Map to QBO Credit Card Account

**CRITICAL:** Map the card to a **Credit Card** account type, NOT Bank.

**HOW:**
1. For each card, select the matching QBO account
2. If no account exists, create one:

```
┌─────────────────────────────────────────────────────────────────┐
│           CREATE NEW ACCOUNT                                     │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Account Type:   [Credit Card ▼]  ◄── MUST be Credit Card       │
│                                                                  │
│  Detail Type:    [Credit Card ▼]                                │
│                                                                  │
│  Name:           [Chase Business Card ****4567]                  │
│                                                                  │
│  Number:         [21000]                                         │
│                                                                  │
│  Description:    [Company purchasing card]                       │
│                                                                  │
│                              [Save and Close]                    │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Step 6: Select Transaction Import Period

**HOW:**
1. Choose how far back to import transactions
2. Click **Connect**

**RECOMMENDATION:**
- For new setup: 90 days or your go-live date
- For existing QBO: Only import from last reconciled date forward

---

## Understanding Credit Card Feeds

### The Credit Card Feed View

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│  BANKING - Credit Cards                                                              │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  Chase Business Card ****4567     Last updated: Today 9:00 AM   Balance: $3,456.78  │
│  ├─ For Review (15)                                                                  │
│  ├─ Categorized (0)                                                                  │
│  └─ Excluded (0)                                                                     │
│                                                                                      │
│  ──────────────────────────────────────────────────────────────────────────────────  │
│                                                                                      │
│  FOR REVIEW                                                                          │
│  ┌────────────────────────────────────────────────────────────────────────────────┐ │
│  │ ☐  03/15  HOME DEPOT #1234         Purchases            $567.89   [Categorize] │ │
│  │ ☐  03/14  LOWES #5678              Purchases            $234.56   [Categorize] │ │
│  │ ☐  03/13  SHELL OIL                Fuel                  $85.00   [Categorize] │ │
│  │ ☐  03/12  PAYMENT - THANK YOU      Payment             -$2,000.00 [Categorize] │ │
│  └────────────────────────────────────────────────────────────────────────────────┘ │
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### Credit Card Transaction Types

| Transaction | Sign | What It Is | How to Categorize |
|-------------|------|------------|-------------------|
| **Purchase** | + (adds to balance) | Something you bought | Categorize as expense |
| **Payment** | - (reduces balance) | Payment you made | Match to bank payment |
| **Credit/Return** | - (reduces balance) | Refund received | Match to original expense |
| **Interest/Fee** | + (adds to balance) | Card charges | 70500 Interest Expense |

---

## Categorizing Credit Card Transactions

### Step-by-Step: Categorizing a Purchase

**Scenario:** You purchased materials at Home Depot for a job.

**HOW:**
1. Click on the transaction in the feed
2. Fill in the details:

```
┌─────────────────────────────────────────────────────────────────┐
│  CATEGORIZE: HOME DEPOT #1234  $567.89                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Vendor:    [Home Depot               ▼]                        │
│                                                                  │
│  Category:  [51100 Lumber & Framing   ▼]  ◄── Expense Account   │
│                                                                  │
│  Customer:  [2024-015-Johnson-Kitchen ▼]  ◄── CRITICAL: Job!    │
│                                                                  │
│  ☑ Billable                                                     │
│                                                                  │
│  Memo:      [Framing lumber - kitchen remodel]                   │
│                                                                  │
│                                    [Add]  [Cancel]              │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

3. Click **Add**

### Step-by-Step: Recording Credit Card Payments

**When you pay your credit card bill, it reduces your balance (liability).**

**Two Methods:**

#### Method A: Match from Bank Feed

When the payment shows up in both your bank account AND credit card:

1. In **Bank Feed**, find the payment
2. Click **Match**
3. QBO auto-matches to the credit card liability

```
Bank Transaction: ACH PAYMENT - CHASE CARD  -$2,000.00

Match to:
┌─────────────────────────────────────────────────────────────────┐
│  ☑ Credit Card Payment - Chase ****4567  03/12/24  $2,000.00   │
└─────────────────────────────────────────────────────────────────┘
```

#### Method B: Create Transfer Manually

If not auto-matched:

1. Click **Transfer** tab
2. Select the credit card account
3. Click **Transfer**

```
From: Checking Account - $2,000.00
To: Chase Business Card ****4567

Result:
Checking decreases: -$2,000
Credit Card Balance decreases: -$2,000
```

### Step-by-Step: Handling Returns/Credits

**Scenario:** You returned materials and received a credit.

**HOW:**
1. Find the credit in the credit card feed
2. Choose one of these approaches:

**Option A: If you find the original purchase:**
- Match the credit to the original expense
- Or manually reduce the original expense

**Option B: If original was in prior period:**
- Categorize as negative expense to same account
- Assign to same customer/job

```
Transaction: HOME DEPOT RETURN  -$125.00

Vendor:    [Home Depot]
Category:  [51100 Lumber & Framing]  ◄── Same as original
Customer:  [2024-015-Johnson-Kitchen]
Amount:    -$125.00 (negative reduces expense)
```

---

## Managing Multiple Credit Cards

### Scenario: Company Cards vs. Employee Cards

Many construction companies have:
- **Company cards**: For office/purchasing manager
- **Employee cards**: For field supervisors, PMs

### Setting Up Employee Cards

**Option 1: Single Account, Track by Memo**
- All cards feed into one Credit Card account
- Add employee name in memo field
- Simple but less visibility

**Option 2: Sub-Accounts per Employee**
```
21000 Credit Cards
├── 21100 Company Card - Main
├── 21200 Employee Card - John Smith
├── 21300 Employee Card - Mike Johnson
└── 21400 Employee Card - Sarah Williams
```
- More setup, but clearer tracking
- Can see spending by employee

### Card Assignment Best Practices

| Card Type | Assigned To | Typical Use |
|-----------|-------------|-------------|
| Main Company Card | Bookkeeper/Office | Large purchases, recurring expenses |
| Project Manager Card | PM | Job-site purchases, emergency supplies |
| Supervisor Card | Field Supervisor | Materials, fuel, small tools |
| Fuel Card | Fleet | Fuel only (may be separate system) |

---

## Fuel Cards: Special Considerations

### Fleet Fuel Cards (WEX, Fuelman, etc.)

Many construction companies use fleet fuel cards:
- WEX
- Fuelman
- Shell Fleet
- Chevron/Texaco Commercial

**Connection Options:**

1. **Direct Connection**: Some fuel cards connect directly to QBO
2. **Manual Import**: Download CSV from fuel card portal, import to QBO
3. **Third-Party Integration**: Use apps that sync fuel data

### Setting Up Fuel Card in QBO

**HOW:**
1. Try to connect directly first (Banking → Add account → search for card)
2. If not available, create manual Credit Card account:

```
Account Type: Credit Card
Name: WEX Fleet Card
Number: 21500

For each transaction:
- Enter as Credit Card Expense
- OR import from CSV file
```

### Fuel Card Categorization Tips

```
Fuel Card Transaction: SHELL #12345  $125.00  TRUCK 145

Categorize:
┌─────────────────────────────────────────────────────────────────┐
│  Vendor:    [Shell]                                             │
│  Category:  [54300 Equipment - Fuel (Job) ▼]                    │
│  Customer:  [2024-015-Johnson-Kitchen ▼]  ◄── Job assignment    │
│  Memo:      [Truck 145 - delivery to jobsite]                   │
└─────────────────────────────────────────────────────────────────┘

OR for non-job fuel:

┌─────────────────────────────────────────────────────────────────┐
│  Vendor:    [Shell]                                             │
│  Category:  [62200 Fuel - Non-Job ▼]  ◄── Overhead              │
│  Customer:  [(leave blank)]                                      │
│  Memo:      [Truck 145 - shop/office travel]                    │
└─────────────────────────────────────────────────────────────────┘
```

---

## Credit Card Reconciliation

### Monthly Reconciliation Process

**WHY RECONCILE:**
Credit card statements are your source of truth. Reconciliation catches:
- Missing transactions
- Duplicate entries
- Fraudulent charges

**HOW:**
1. Get your credit card statement (paper or PDF)
2. Go to **Accounting** → **Reconcile**
3. Select the credit card account
4. Enter:
   - Statement ending date
   - Statement ending balance (the amount you owe)

```
┌─────────────────────────────────────────────────────────────────┐
│        RECONCILE: CHASE BUSINESS CARD ****4567                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Statement Ending Date: [03/31/2024]                            │
│                                                                  │
│  Statement Ending Balance: [$3,456.78]                          │
│  (Enter the balance you OWE, not available credit)              │
│                                                                  │
│                              [Start reconciling]                 │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

5. Check off each transaction that appears on statement
6. Difference should equal $0
7. Click **Finish now**

### Reconciliation Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| Balance doesn't match | Missing transactions | Check for unrecorded purchases |
| Duplicate transactions | Entered manually AND via feed | Delete the duplicate |
| Payment not showing | Not matched properly | Find and match payment |
| Wrong starting balance | Prior reconciliation error | May need to adjust opening balance |

---

## Credit Card Rules for Construction

### Recommended Auto-Categorization Rules

| Rule Name | Bank Text Contains | Category | Vendor |
|-----------|-------------------|----------|--------|
| Home Depot | HOME DEPOT | 51000 Direct Materials | Home Depot |
| Lowe's | LOWES | 51000 Direct Materials | Lowe's |
| Shell Fuel | SHELL | 54300 Fuel - Job | Shell |
| Office Supplies | STAPLES, OFFICE DEPOT | 63100 Office Supplies | (varies) |
| Amazon | AMAZON, AMZN | 63100 Office Supplies | Amazon |

**CAUTION with Auto-Rules for Job Costs:**
- Rules can pre-fill category/vendor
- But leave Customer BLANK in rules
- You must manually assign to correct job each time

### Creating a Rule from Transaction

**HOW:**
1. When categorizing a transaction, look for **Create a rule**
2. Click to create rule based on this transaction
3. Adjust rule parameters:
   - What text to match
   - Category assignment
   - Vendor assignment
   - Auto-add setting (use cautiously)

---

## Credit Card Best Practices for Construction

### Daily/Weekly Habits

- [ ] Review credit card feed 2-3 times per week
- [ ] Categorize transactions promptly
- [ ] ALWAYS assign job costs to Customer/Project
- [ ] Collect receipts from employees with cards
- [ ] Match receipts to transactions

### Monthly Habits

- [ ] Reconcile all credit cards to statements
- [ ] Review for unusual or fraudulent charges
- [ ] Verify job cost assignments are correct
- [ ] Update rules for new recurring vendors

### Receipt Management

**WHY KEEP RECEIPTS:**
- IRS audit documentation
- Verify job cost assignments
- Catch errors in categorization
- Support billable expense claims

**HOW TO ATTACH RECEIPTS IN QBO:**
1. When categorizing transaction, click **Attachments**
2. Upload photo or PDF of receipt
3. Receipt is now linked to transaction

**Mobile Option:**
Use QBO Mobile app to:
1. Take photo of receipt
2. App matches to transaction
3. Attach automatically

---

## Common Credit Card Mistakes

### Mistake 1: Setting Up as Bank Account

**Problem:** Credit card mapped as Bank type instead of Credit Card
**Symptom:** Balance shows positive when you owe money
**Fix:** Create proper Credit Card account, re-map connection

### Mistake 2: Not Matching Payments

**Problem:** Payment recorded as expense instead of payment on card
**Symptom:** Credit card balance never decreases
**Fix:** Delete incorrect entry, match payment properly

### Mistake 3: Mixing Personal and Business

**Problem:** Personal charges on business card
**Symptom:** Job costs include non-business items
**Fix:** Categorize personal items to Owner Draw, discuss card policy with team

### Mistake 4: Not Assigning to Jobs

**Problem:** Job costs categorized without Customer/Project
**Symptom:** Job profitability reports are inaccurate
**Fix:** Review and update past transactions, train on process

### Mistake 5: Duplicate Entries

**Problem:** Manual entry AND bank feed entry for same transaction
**Symptom:** Expenses overstated, reconciliation fails
**Fix:** Delete duplicate, rely on bank feed going forward

---

## Credit Card Checklist

### Initial Setup:
- [ ] Connect all business credit cards
- [ ] Map to Credit Card account type (NOT Bank)
- [ ] Set up sub-accounts if multiple cards
- [ ] Create rules for common vendors
- [ ] Train cardholders on receipt requirements

### Weekly:
- [ ] Categorize all new transactions
- [ ] Assign job costs to correct projects
- [ ] Attach receipts where available
- [ ] Review auto-categorized for accuracy

### Monthly:
- [ ] Reconcile to statement
- [ ] Match all payments
- [ ] Review for errors or fraud
- [ ] Update rules as needed

---

*[← Previous: Connecting Bank Accounts](./01-connecting-bank-accounts.md) | [Next: Recording Transactions →](./03-recording-transactions.md)*
