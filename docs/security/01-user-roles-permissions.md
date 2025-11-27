# User Roles and Permissions for Construction Companies

## Overview

Proper user access controls are essential for protecting your financial data, maintaining internal controls, and satisfying auditor and bonding company requirements. This guide covers user roles, permission settings, and best practices for construction company QBO setups.

> ⚠️ **Disclaimer**: This guide is for informational purposes only. Consult with your CPA and IT security professional. See full [disclaimer](../../README.md#%EF%B8%8F-important-disclaimer).

---

## Table of Contents

1. [Why User Roles Matter](#why-user-roles-matter)
2. [QBO User Types](#qbo-user-types)
3. [Recommended Role Structure](#recommended-role-structure)
4. [Setting Up Users](#setting-up-users)
5. [Custom User Roles (QBO Advanced)](#custom-user-roles-qbo-advanced)
6. [Audit Trail and Activity Log](#audit-trail-and-activity-log)
7. [Security Best Practices](#security-best-practices)
8. [Separation of Duties](#separation-of-duties)

---

## Why User Roles Matter

### Internal Controls

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    WHY RESTRICT ACCESS?                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  FRAUD PREVENTION:                                                           │
│  ─────────────────                                                           │
│  • Limit who can write checks                                               │
│  • Control who can create vendors (ghost employee schemes)                  │
│  • Restrict who can modify transactions                                     │
│  • Prevent unauthorized disbursements                                       │
│                                                                              │
│  ERROR REDUCTION:                                                            │
│  ────────────────                                                            │
│  • Untrained users can't accidentally delete data                           │
│  • Reduces incorrect postings                                               │
│  • Limits access to what user needs                                         │
│                                                                              │
│  BONDING REQUIREMENTS:                                                       │
│  ─────────────────────                                                       │
│  Bonding companies evaluate internal controls:                              │
│  • Who has access to financial data?                                        │
│  • Is there separation of duties?                                           │
│  • Are access logs maintained?                                              │
│                                                                              │
│  AUDIT REQUIREMENTS:                                                         │
│  ───────────────────                                                         │
│  Auditors ask:                                                               │
│  • Who can modify the books?                                                │
│  • Is there an audit trail?                                                 │
│  • Are closed periods protected?                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Common Fraud Scenarios

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FRAUD SCENARIOS PREVENTED BY CONTROLS                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  SCENARIO 1: Ghost Vendor                                                    │
│  ────────────────────────                                                    │
│  Employee creates fake vendor (their own LLC)                               │
│  Submits fake invoices and gets paid                                        │
│                                                                              │
│  Prevention: Separate vendor creation from bill payment                     │
│             Owner/manager approves new vendors                              │
│                                                                              │
│  SCENARIO 2: Check Diversion                                                 │
│  ──────────────────────────                                                  │
│  Bookkeeper writes check to self                                            │
│  Records as payment to legitimate vendor                                    │
│                                                                              │
│  Prevention: Require dual signatures                                        │
│             Segregate check writing from bank reconciliation               │
│                                                                              │
│  SCENARIO 3: Expense Account Padding                                         │
│  ───────────────────────────────────                                         │
│  Employee submits personal expenses as business                             │
│  Codes to vague accounts                                                    │
│                                                                              │
│  Prevention: Require receipts                                               │
│             Expense approval workflow                                       │
│             Regular expense review                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## QBO User Types

### Standard User Categories

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QBO USER TYPES                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. MASTER ADMIN (Primary Admin)                                             │
│     ────────────────────────────                                             │
│     • Full access to everything                                              │
│     • Can manage all users                                                   │
│     • Can manage subscription/billing                                       │
│     • Only ONE per company                                                   │
│     • Usually: Owner or Controller                                          │
│                                                                              │
│  2. COMPANY ADMIN                                                            │
│     ─────────────                                                            │
│     • Full access to QBO features                                           │
│     • Can add/remove standard users                                         │
│     • Cannot manage billing                                                  │
│     • Cannot remove Master Admin                                            │
│     • Usually: CFO, Controller, Office Manager                              │
│                                                                              │
│  3. STANDARD USER                                                            │
│     ─────────────                                                            │
│     • Access controlled by admin                                            │
│     • Multiple access levels available:                                     │
│       - All access                                                          │
│       - Limited access (customizable)                                       │
│       - Custom access (QBO Advanced)                                        │
│     • Most employees                                                         │
│                                                                              │
│  4. REPORTS ONLY                                                             │
│     ────────────                                                             │
│     • Can only view reports                                                  │
│     • Cannot enter/modify transactions                                      │
│     • Usually: Project Managers, Estimators                                 │
│                                                                              │
│  5. TIME TRACKING ONLY                                                       │
│     ──────────────────                                                       │
│     • Can only enter time                                                    │
│     • Cannot see financial data                                             │
│     • Usually: Field workers                                                │
│                                                                              │
│  6. ACCOUNTANT USER (Special)                                                │
│     ─────────────────────────                                                │
│     • Free user slot for accountant                                          │
│     • Full access                                                            │
│     • Can invite other accountants                                          │
│     • Your CPA firm                                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### User Limits by Plan

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    QBO PLAN USER LIMITS                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Plan              │ Users Included │ Accountant Users │ Time-Only Users   │
│  ──────────────────┼────────────────┼──────────────────┼──────────────────│
│  Simple Start      │ 1              │ 2                │ N/A               │
│  Essentials        │ 3              │ 2                │ N/A               │
│  Plus              │ 5              │ 2                │ Unlimited (free)  │
│  Advanced          │ 25             │ 3                │ Unlimited (free)  │
│                                                                              │
│  Additional users can be purchased for most plans                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Recommended Role Structure

### Typical Construction Company Roles

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CONSTRUCTION COMPANY ROLE STRUCTURE                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  OWNER/PRINCIPAL                                                             │
│  ───────────────                                                             │
│  User Type: Master Admin                                                     │
│  Access: Full                                                                │
│  Responsibilities:                                                           │
│  • Ultimate oversight                                                        │
│  • Approve large transactions                                               │
│  • Review financials                                                         │
│  • Manage user access                                                        │
│                                                                              │
│  CONTROLLER/CFO                                                              │
│  ─────────────                                                               │
│  User Type: Company Admin                                                    │
│  Access: Full                                                                │
│  Responsibilities:                                                           │
│  • Day-to-day financial oversight                                           │
│  • Month-end close                                                           │
│  • Bank reconciliations                                                      │
│  • Financial reporting                                                       │
│  • User management                                                           │
│                                                                              │
│  BOOKKEEPER/AP CLERK                                                         │
│  ──────────────────                                                          │
│  User Type: Standard User (Limited)                                          │
│  Access: Bills, Expenses, Vendor management                                 │
│  Restrictions: No check writing, no vendor creation                         │
│  Responsibilities:                                                           │
│  • Enter vendor bills                                                        │
│  • Process pay applications                                                 │
│  • Track AP aging                                                            │
│  • Prepare payments for approval                                            │
│                                                                              │
│  AR CLERK/BILLING SPECIALIST                                                 │
│  ─────────────────────────────                                               │
│  User Type: Standard User (Limited)                                          │
│  Access: Invoicing, Customer management, AR                                 │
│  Restrictions: No AP access, no bank access                                 │
│  Responsibilities:                                                           │
│  • Create and send invoices                                                 │
│  • Record customer payments                                                 │
│  • Track AR aging                                                            │
│  • Customer collections                                                      │
│                                                                              │
│  PROJECT MANAGER                                                             │
│  ───────────────                                                             │
│  User Type: Standard User (Reports Only or Custom)                          │
│  Access: Reports, Time entry, maybe Job costs                               │
│  Restrictions: No transaction entry, no modifications                       │
│  Responsibilities:                                                           │
│  • View job profitability                                                   │
│  • Approve time entries                                                      │
│  • Review budgets                                                            │
│  • Cost monitoring                                                           │
│                                                                              │
│  ESTIMATOR                                                                   │
│  ─────────                                                                   │
│  User Type: Standard User (Reports Only)                                    │
│  Access: Reports only                                                        │
│  Responsibilities:                                                           │
│  • View historical job costs                                                │
│  • Research vendor pricing                                                  │
│  • Analyze margins                                                           │
│                                                                              │
│  FIELD SUPERVISOR                                                            │
│  ────────────────                                                            │
│  User Type: Time Tracking Only                                               │
│  Access: Time entry only                                                     │
│  Responsibilities:                                                           │
│  • Enter crew time                                                           │
│  • Assign time to jobs                                                       │
│                                                                              │
│  EXTERNAL ACCOUNTANT/CPA                                                     │
│  ───────────────────────                                                     │
│  User Type: Accountant User                                                  │
│  Access: Full                                                                │
│  Responsibilities:                                                           │
│  • Month-end review                                                          │
│  • Tax preparation                                                           │
│  • Year-end close                                                            │
│  • Adjusting entries                                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Role Matrix

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PERMISSION MATRIX                                         │
├───────────────────┬───────┬────────┬────────┬────────┬───────┬─────────────┤
│ Function          │ Owner │Contrlr │AP Clerk│AR Clerk│  PM   │ Field Supv  │
├───────────────────┼───────┼────────┼────────┼────────┼───────┼─────────────┤
│ View Reports      │  ✅   │   ✅   │   ⚠️   │   ⚠️   │  ✅   │     ❌      │
│ Enter Invoices    │  ✅   │   ✅   │   ❌   │   ✅   │  ❌   │     ❌      │
│ Enter Bills       │  ✅   │   ✅   │   ✅   │   ❌   │  ❌   │     ❌      │
│ Pay Bills/Checks  │  ✅   │   ✅   │   ❌   │   ❌   │  ❌   │     ❌      │
│ Bank Reconcile    │  ✅   │   ✅   │   ❌   │   ❌   │  ❌   │     ❌      │
│ Create Vendors    │  ✅   │   ✅   │   ❌   │   ❌   │  ❌   │     ❌      │
│ Create Customers  │  ✅   │   ✅   │   ❌   │   ✅   │  ❌   │     ❌      │
│ Enter Time        │  ✅   │   ✅   │   ✅   │   ✅   │  ✅   │     ✅      │
│ Manage Users      │  ✅   │   ✅   │   ❌   │   ❌   │  ❌   │     ❌      │
│ Change Settings   │  ✅   │   ✅   │   ❌   │   ❌   │  ❌   │     ❌      │
│ Close Books       │  ✅   │   ✅   │   ❌   │   ❌   │  ❌   │     ❌      │
├───────────────────┴───────┴────────┴────────┴────────┴───────┴─────────────┤
│ Legend: ✅ Full  ⚠️ Limited  ❌ No Access                                   │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Setting Up Users

### Step-by-Step: Add a New User

**Navigation: ⚙️ Gear → Manage Users → Add User**

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ADDING A NEW USER                                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  STEP 1: SELECT USER TYPE                                                    │
│  ─────────────────────────                                                   │
│  Options:                                                                    │
│  ○ Standard user (most employees)                                           │
│  ○ Company admin                                                             │
│  ○ Reports only                                                              │
│  ○ Time tracking only                                                        │
│                                                                              │
│  STEP 2: SET ACCESS RIGHTS (for Standard User)                              │
│  ─────────────────────────────────────────────                               │
│                                                                              │
│  OPTION A: All Access                                                        │
│  └── Full access to all features                                            │
│                                                                              │
│  OPTION B: Limited Access (configure below)                                  │
│                                                                              │
│  [Customers and Sales]                                                       │
│  ○ None  ○ View only  ○ Full access                                        │
│                                                                              │
│  [Vendors and Purchases]                                                     │
│  ○ None  ○ View only  ○ Full access                                        │
│                                                                              │
│  [Payroll]                                                                   │
│  ○ None  ○ View only  ○ Full access                                        │
│                                                                              │
│  [Time Tracking]                                                             │
│  ○ None  ○ View only  ○ Full access                                        │
│                                                                              │
│  [Reports]                                                                   │
│  ○ None  ○ Full access                                                      │
│                                                                              │
│  STEP 3: ENTER USER DETAILS                                                  │
│  ──────────────────────────                                                  │
│  Email: [user@company.com]                                                   │
│  └── Invitation sent to this email                                          │
│                                                                              │
│  STEP 4: SEND INVITATION                                                     │
│  ───────────────────────                                                     │
│  Click: Send                                                                 │
│  User receives email with setup link                                        │
│  User creates their own password                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Configuring Limited Access

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LIMITED ACCESS OPTIONS                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  AP CLERK CONFIGURATION:                                                     │
│  ───────────────────────                                                     │
│  Customers and Sales:      None                                              │
│  Vendors and Purchases:    Full access                                       │
│  Payroll:                  None                                              │
│  Time Tracking:            Full access                                       │
│  Reports:                  Full access                                       │
│                                                                              │
│  Additional restrictions (if using QBO Advanced):                            │
│  • Cannot write checks (prepare only)                                       │
│  • Cannot create new vendors                                                │
│  • Cannot void/delete transactions                                          │
│                                                                              │
│  AR CLERK CONFIGURATION:                                                     │
│  ───────────────────────                                                     │
│  Customers and Sales:      Full access                                       │
│  Vendors and Purchases:    None                                              │
│  Payroll:                  None                                              │
│  Time Tracking:            View only                                         │
│  Reports:                  Full access                                       │
│                                                                              │
│  PROJECT MANAGER CONFIGURATION:                                              │
│  ──────────────────────────────                                              │
│  Customers and Sales:      View only                                        │
│  Vendors and Purchases:    View only                                        │
│  Payroll:                  None                                              │
│  Time Tracking:            Full access                                       │
│  Reports:                  Full access                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Inviting Your Accountant

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ACCOUNTANT USER SETUP                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Navigation: ⚙️ → Manage Users → Accounting Firms                          │
│                                                                              │
│  STEP 1: Click "Invite Accountant"                                          │
│                                                                              │
│  STEP 2: Enter accountant's email                                           │
│  └── Use their business email (not personal)                                │
│                                                                              │
│  STEP 3: Send invitation                                                    │
│                                                                              │
│  BENEFITS:                                                                   │
│  ─────────                                                                   │
│  • Doesn't count against your user limit                                    │
│  • Accountant gets special tools                                            │
│  • Can close books with password                                            │
│  • Access to accountant toolbox                                             │
│                                                                              │
│  NOTE: Your accountant must have QuickBooks Online Accountant               │
│  (a free platform for accounting professionals)                             │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Custom User Roles (QBO Advanced)

### Custom Role Builder

QBO Advanced allows creating custom roles with granular permissions:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CUSTOM ROLE BUILDER (ADVANCED)                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Navigation: ⚙️ → Manage Users → Roles → Custom Roles                      │
│                                                                              │
│  EXAMPLE: "AP Specialist" Custom Role                                        │
│  ─────────────────────────────────────                                       │
│                                                                              │
│  BILLS & EXPENSES                                                            │
│  ☑️ View bills                                                               │
│  ☑️ Create bills                                                             │
│  ☑️ Edit bills                                                               │
│  ☐ Delete bills                                                              │
│  ☐ Void bills                                                                │
│                                                                              │
│  PAYMENTS                                                                    │
│  ☑️ View payments                                                            │
│  ☑️ Create bill payment (prepare)                                           │
│  ☐ Print checks (requires approval)                                         │
│  ☐ Send ACH payments                                                        │
│                                                                              │
│  VENDORS                                                                     │
│  ☑️ View vendors                                                             │
│  ☐ Create vendors (manager creates)                                         │
│  ☑️ Edit vendor info                                                        │
│  ☐ Delete vendors                                                            │
│                                                                              │
│  BANKING                                                                     │
│  ☑️ View bank feeds                                                          │
│  ☑️ Categorize transactions                                                 │
│  ☐ Reconcile accounts                                                        │
│                                                                              │
│  REPORTS                                                                     │
│  ☑️ AP reports                                                               │
│  ☑️ Vendor reports                                                           │
│  ☐ All company reports                                                       │
│  ☐ Payroll reports                                                           │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Pre-Built Custom Roles for Construction

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CONSTRUCTION CUSTOM ROLES                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ROLE: Job Cost Analyst                                                      │
│  ────────────────────────                                                    │
│  Purpose: Review job costs without modifying                                │
│  Access:                                                                     │
│  ☑️ All reports                                                              │
│  ☑️ View transactions (all)                                                 │
│  ☐ Create/edit transactions                                                 │
│  ☐ Banking                                                                   │
│  ☐ Payroll                                                                   │
│                                                                              │
│  ROLE: Subcontract Administrator                                             │
│  ───────────────────────────────                                             │
│  Purpose: Manage subcontractor bills and payments                           │
│  Access:                                                                     │
│  ☑️ View/create/edit bills                                                  │
│  ☑️ View vendors                                                             │
│  ☑️ Create purchase orders                                                  │
│  ☑️ AP reports                                                               │
│  ☐ Pay bills (prepare only)                                                 │
│  ☐ Banking/reconciliation                                                    │
│                                                                              │
│  ROLE: Billing Coordinator                                                   │
│  ─────────────────────────                                                   │
│  Purpose: Create and manage customer invoices                               │
│  Access:                                                                     │
│  ☑️ View/create/edit invoices                                               │
│  ☑️ View/create/edit estimates                                              │
│  ☑️ View customers                                                           │
│  ☑️ Record payments received                                                │
│  ☑️ AR reports                                                               │
│  ☐ Bank deposits                                                             │
│  ☐ Vendors/AP                                                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Audit Trail and Activity Log

### Viewing the Audit Log

```
Navigation: ⚙️ Gear → Audit Log

┌─────────────────────────────────────────────────────────────────────────────┐
│                    AUDIT LOG                                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  WHAT IT SHOWS:                                                              │
│  ───────────────                                                             │
│  • Date/time of action                                                       │
│  • User who performed action                                                │
│  • Type of event (create, edit, delete)                                     │
│  • Transaction type affected                                                │
│  • History of changes                                                        │
│                                                                              │
│  SAMPLE AUDIT LOG:                                                           │
│  ─────────────────                                                           │
│  Date        │ User       │ Event    │ Name/Detail                          │
│  ────────────┼────────────┼──────────┼─────────────────────────────────────│
│  03/15 2:30p │ J. Smith   │ Created  │ Bill #4521 - ABC Lumber              │
│  03/15 2:45p │ M. Johnson │ Edited   │ Bill #4521 - changed amount          │
│  03/15 3:00p │ J. Smith   │ Created  │ Bill Payment - Check #1542           │
│  03/15 3:15p │ Admin      │ Deleted  │ Expense - Fuel purchase              │
│  03/16 9:00a │ J. Smith   │ Login    │ Sign in from 192.168.1.100           │
│                                                                              │
│  FILTERING:                                                                  │
│  ──────────                                                                  │
│  • By date range                                                             │
│  • By user                                                                   │
│  • By event type                                                             │
│  • By transaction type                                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Using Audit Log for Controls

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    AUDIT LOG BEST PRACTICES                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  MONTHLY REVIEW:                                                             │
│  ───────────────                                                             │
│  1. Review all "Delete" events                                              │
│     • Why was this deleted?                                                  │
│     • Who approved?                                                          │
│                                                                              │
│  2. Review large transactions                                               │
│     • Are they legitimate?                                                   │
│     • Proper approvals?                                                      │
│                                                                              │
│  3. Review vendor changes                                                   │
│     • New vendors added                                                      │
│     • Bank info changes (potential fraud indicator)                         │
│                                                                              │
│  4. Review user activity                                                    │
│     • Unusual hours?                                                         │
│     • Unusual volume?                                                        │
│                                                                              │
│  RED FLAGS:                                                                  │
│  ──────────                                                                  │
│  ⚠️ Deletions without reason                                                │
│  ⚠️ Vendor address/bank changes before payment                              │
│  ⚠️ Large transactions by unauthorized users                                │
│  ⚠️ Activity during unusual hours                                           │
│  ⚠️ Multiple failed login attempts                                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Closing the Books

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CLOSE THE BOOKS                                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  Navigation: ⚙️ → Account and Settings → Advanced → Accounting             │
│                                                                              │
│  Close the books: ON ✅                                                     │
│                                                                              │
│  Closing date: [12/31/2023]                                                 │
│  └── Transactions before this date are protected                            │
│                                                                              │
│  Allow changes after viewing a warning: ○                                   │
│  Allow changes after entering password: ●                                   │
│  └── RECOMMENDED: Require password                                          │
│                                                                              │
│  Password: [Set a strong password]                                          │
│  └── Only share with Controller/CPA                                         │
│                                                                              │
│  WHAT THIS DOES:                                                             │
│  ────────────────                                                            │
│  • Prevents accidental changes to prior periods                             │
│  • Protects filed tax periods                                               │
│  • Creates audit trail for any changes                                      │
│  • Satisfies auditor requirements                                           │
│                                                                              │
│  WHEN TO UPDATE CLOSING DATE:                                                │
│  ─────────────────────────────                                               │
│  • After monthly close (move forward monthly)                               │
│  • After year-end close (protect entire year)                               │
│  • After CPA review/adjustments                                             │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Security Best Practices

### Account Security

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SECURITY BEST PRACTICES                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  1. STRONG PASSWORDS                                                         │
│     ────────────────                                                         │
│     • Minimum 12 characters                                                  │
│     • Mix of upper, lower, numbers, symbols                                 │
│     • Unique (not used elsewhere)                                           │
│     • Changed regularly (quarterly)                                          │
│                                                                              │
│  2. TWO-FACTOR AUTHENTICATION (2FA)                                          │
│     ──────────────────────────────                                           │
│     • Enable for ALL users                                                   │
│     • Required by QBO for admins                                            │
│     • Use authenticator app (not SMS)                                       │
│     • Navigation: ⚙️ → Account and Settings → Security                     │
│                                                                              │
│  3. INDIVIDUAL ACCOUNTS                                                      │
│     ───────────────────                                                      │
│     • NEVER share login credentials                                         │
│     • Each person has own account                                           │
│     • Enables audit trail per user                                          │
│                                                                              │
│  4. IMMEDIATE DEACTIVATION                                                   │
│     ─────────────────────                                                    │
│     • Remove access when employee leaves                                    │
│     • Same day termination = same day removal                               │
│     • Review user list monthly                                              │
│                                                                              │
│  5. REGULAR ACCESS REVIEW                                                    │
│     ─────────────────────                                                    │
│     • Quarterly: Review all user access                                     │
│     • Remove users no longer needed                                         │
│     • Adjust permissions as roles change                                    │
│                                                                              │
│  6. SECURE CONNECTIONS                                                       │
│     ──────────────────                                                       │
│     • Only access from secure networks                                      │
│     • Avoid public WiFi                                                     │
│     • Use VPN if accessing remotely                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Termination Checklist

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    EMPLOYEE TERMINATION CHECKLIST                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  IMMEDIATELY upon termination:                                               │
│                                                                              │
│  □ Remove QBO access                                                         │
│    ⚙️ → Manage Users → [User] → Delete                                     │
│                                                                              │
│  □ Remove access to all integrated apps                                     │
│    (Time tracking, project management, etc.)                                │
│                                                                              │
│  □ Change any shared passwords the user knew                                │
│    (If any were shared despite best practices)                              │
│                                                                              │
│  □ Review audit log for recent activity                                     │
│    Look for unusual transactions before departure                           │
│                                                                              │
│  □ Review vendor records                                                    │
│    Ensure no unauthorized vendors added                                     │
│                                                                              │
│  □ Collect company devices                                                  │
│    That may have saved credentials                                          │
│                                                                              │
│  □ Notify bank                                                               │
│    If user was authorized signer                                            │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Separation of Duties

### Key Control Separations

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SEPARATION OF DUTIES                                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PRINCIPLE:                                                                  │
│  No single person should control all aspects of a financial process.        │
│                                                                              │
│  KEY SEPARATIONS:                                                            │
│                                                                              │
│  1. VENDOR MANAGEMENT vs PAYMENTS                                            │
│     ─────────────────────────────                                            │
│     • Person who creates vendors ≠ Person who pays vendors                  │
│     • Prevents creation of fake vendors for payment                         │
│                                                                              │
│     WHO CREATES VENDORS: Controller or Office Manager                       │
│     WHO ENTERS BILLS: AP Clerk                                              │
│     WHO PAYS BILLS: Controller (with owner approval > threshold)            │
│                                                                              │
│  2. BILLING vs CASH RECEIPTS                                                 │
│     ────────────────────────                                                 │
│     • Person who creates invoices ≠ Person who handles deposits            │
│     • Prevents billing manipulation to cover theft                          │
│                                                                              │
│     WHO CREATES INVOICES: AR Clerk                                          │
│     WHO RECORDS PAYMENTS: Controller                                        │
│     WHO DEPOSITS: Owner or authorized signer                                │
│                                                                              │
│  3. BANK RECONCILIATION vs TRANSACTIONS                                      │
│     ───────────────────────────────────                                      │
│     • Person who reconciles ≠ Person who enters transactions                │
│     • Reconciler can detect unauthorized transactions                       │
│                                                                              │
│     WHO ENTERS TRANSACTIONS: AP/AR Clerks                                   │
│     WHO RECONCILES: Controller (or Owner)                                   │
│                                                                              │
│  4. PAYROLL vs HR                                                            │
│     ─────────────                                                            │
│     • Person who adds employees ≠ Person who processes payroll             │
│     • Prevents ghost employees                                              │
│                                                                              │
│     WHO ADDS EMPLOYEES: HR or Owner                                         │
│     WHO PROCESSES PAYROLL: Controller                                       │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Small Company Workarounds

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    SMALL COMPANY CONTROLS                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PROBLEM: Not enough staff to separate duties                               │
│                                                                              │
│  COMPENSATING CONTROLS:                                                      │
│  ──────────────────────                                                      │
│                                                                              │
│  1. OWNER REVIEW                                                             │
│     • Owner personally reviews all bank statements                          │
│     • Owner signs (or approves) all checks over threshold                   │
│     • Owner reviews vendor list monthly                                     │
│                                                                              │
│  2. EXTERNAL REVIEW                                                          │
│     • CPA performs monthly review                                           │
│     • External bookkeeper handles reconciliation                            │
│     • Periodic surprise audits                                              │
│                                                                              │
│  3. TRANSACTION LIMITS                                                       │
│     • Bank limits on ACH/wire without approval                              │
│     • Credit card limits                                                     │
│     • Check signing limits (dual signature > $X)                            │
│                                                                              │
│  4. TECHNOLOGY CONTROLS                                                      │
│     • Positive Pay with bank                                                │
│     • ACH blocks                                                             │
│     • Bank alerts for large transactions                                    │
│                                                                              │
│  5. REGULAR REVIEWS                                                          │
│     • Weekly: Review all transactions                                       │
│     • Monthly: Review audit log                                             │
│     • Quarterly: Review user access                                         │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    USER ROLES QUICK REFERENCE                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  MANAGE USERS: ⚙️ → Manage Users                                            │
│  AUDIT LOG: ⚙️ → Audit Log                                                  │
│  CLOSE BOOKS: ⚙️ → Account Settings → Advanced → Accounting                │
│                                                                              │
│  RECOMMENDED ROLES:                                                          │
│  • Owner: Master Admin                                                       │
│  • Controller: Company Admin                                                │
│  • AP Clerk: Limited - Vendors only                                         │
│  • AR Clerk: Limited - Customers only                                       │
│  • PM: Reports only or Custom                                               │
│  • Field: Time tracking only                                                │
│  • CPA: Accountant user                                                     │
│                                                                              │
│  SECURITY MUSTS:                                                             │
│  ✅ Enable 2FA for all users                                                │
│  ✅ Individual accounts (no sharing)                                        │
│  ✅ Remove access immediately on termination                                │
│  ✅ Close the books with password                                           │
│  ✅ Review audit log monthly                                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Next Steps

With user roles configured:
- [Month-End Close](../checklists/11-month-end-close.md) - Include access review
- [Common Mistakes](../reference/10-common-mistakes.md) - Security errors to avoid
- [Reporting Guide](../reporting/01-essential-reports.md) - Control reports

---

*[Back to Main Guide](../../README.md)*
