# Retention Tracker Template

## Instructions

Use this template to track retention held and released across all projects. Copy into Excel or Google Sheets for automatic calculations and alerts.

---

## Company Information

```
COMPANY: _________________________________
PREPARED BY: _____________________________
AS OF DATE: ______________________________
```

---

## Retention Summary Dashboard

```
RETENTION SUMMARY
═══════════════════════════════════════════════════════════════════════════════

RECEIVABLES (Retention We Are Owed):
────────────────────────────────────────────────────────────────────────────────
  Active Projects                         $______________
  Substantially Complete Projects         $______________
  Awaiting Final Payment                  $______________
                                         ─────────────────
  TOTAL RETENTION RECEIVABLE              $______________

PAYABLES (Retention We Owe):
────────────────────────────────────────────────────────────────────────────────
  Active Projects                         $______________
  Substantially Complete Projects         $______________
  Ready to Release                        $______________
                                         ─────────────────
  TOTAL RETENTION PAYABLE                 $______________

NET RETENTION POSITION                    $______________

═══════════════════════════════════════════════════════════════════════════════
```

---

## Retention Receivable Detail (What We Are Owed)

### By Project

| Project | Owner/GC | Contract Value | Retention % | Total Billed | Retention Held | Released | Balance Due | Status | Expected Date |
|---------|----------|----------------|-------------|--------------|----------------|----------|-------------|--------|---------------|
| Smith Residence | J. Smith | $285,000 | 10% | $265,000 | $26,500 | $0 | $26,500 | Active | 03/15/25 |
| Jones Office | ABC Corp | $450,000 | 5% | $450,000 | $22,500 | $11,250 | $11,250 | Punchlist | 02/01/25 |
| Main St Retail | XYZ Dev | $875,000 | 10% | $780,000 | $78,000 | $0 | $78,000 | Active | 06/30/25 |
| City Hall Reno | City Gov | $1,200,000 | 5% | $1,200,000 | $60,000 | $60,000 | $0 | Complete | PAID |
| | | | | | | | | | |
| | | | | | | | | | |
| **TOTALS** | | | | | **$187,000** | **$71,250** | **$115,750** | | |

### Status Definitions

| Status | Description | Action Required |
|--------|-------------|-----------------|
| **Active** | Project in progress | Continue billing retention |
| **Substantial** | Substantially complete | Submit retention invoice |
| **Punchlist** | Completing punchlist | Finish items, submit final |
| **Final Pending** | Final invoice submitted | Follow up on payment |
| **Complete** | Retention collected | Archive |

---

## Retention Receivable Aging

```
RETENTION RECEIVABLE AGING REPORT

Days Since Substantial Completion:

0-30 Days:
────────────────────────────────────────────────────────────────────────────────
  Project               Amount Due      Substantial Date    Days    Status
  ────────────────────────────────────────────────────────────────────────────
  Jones Office          $11,250         11/15/24            12      Punchlist
                                       ──────────────
  Subtotal 0-30 Days                   $11,250

31-60 Days:
────────────────────────────────────────────────────────────────────────────────
  [None]                                $0
                                       ──────────────
  Subtotal 31-60 Days                  $0

61-90 Days:
────────────────────────────────────────────────────────────────────────────────
  [None]                                $0
                                       ──────────────
  Subtotal 61-90 Days                  $0

Over 90 Days:
────────────────────────────────────────────────────────────────────────────────
  [None]                                $0
                                       ──────────────
  Subtotal Over 90 Days                $0

Still Active (Not Yet Due):
────────────────────────────────────────────────────────────────────────────────
  Smith Residence       $26,500         In Progress
  Main St Retail        $78,000         In Progress
                                       ──────────────
  Subtotal Active                      $104,500

═══════════════════════════════════════════════════════════════════════════════
TOTAL RETENTION RECEIVABLE             $115,750
```

---

## Retention Payable Detail (What We Owe Subcontractors)

### By Subcontractor

| Subcontractor | Project | Subcontract | Retention % | Total Paid | Retention Held | Released | Balance Owed | Lien Waiver | Status |
|---------------|---------|-------------|-------------|------------|----------------|----------|--------------|-------------|--------|
| ABC Electric | Smith Res | $45,000 | 10% | $38,000 | $4,500 | $0 | $4,500 | Pending | Active |
| ABC Electric | Jones Off | $62,000 | 5% | $62,000 | $3,100 | $1,550 | $1,550 | Partial | Punchlist |
| DEF Plumbing | Smith Res | $38,000 | 10% | $32,000 | $3,800 | $0 | $3,800 | Pending | Active |
| DEF Plumbing | Main St | $95,000 | 10% | $85,000 | $9,500 | $0 | $9,500 | Pending | Active |
| GHI HVAC | Jones Off | $78,000 | 5% | $78,000 | $3,900 | $3,900 | $0 | Final | PAID |
| JKL Roofing | Main St | $125,000 | 10% | $110,000 | $12,500 | $0 | $12,500 | Pending | Active |
| | | | | | | | | | |
| **TOTALS** | | | | | **$37,300** | **$5,450** | **$31,850** | | |

### By Project Summary

| Project | Total Sub Contracts | Total Retention Held | Released | Balance to Release |
|---------|---------------------|----------------------|----------|---------------------|
| Smith Residence | $83,000 | $8,300 | $0 | $8,300 |
| Jones Office | $140,000 | $7,000 | $5,450 | $1,550 |
| Main St Retail | $220,000 | $22,000 | $0 | $22,000 |
| | | | | |
| **TOTALS** | **$443,000** | **$37,300** | **$5,450** | **$31,850** |

---

## Retention Release Checklist

### Before Releasing Subcontractor Retention

```
PROJECT: ______________________  SUBCONTRACTOR: ______________________

PRE-RELEASE VERIFICATION:
□ Work is 100% complete
□ All punchlist items resolved
□ Final inspection passed
□ As-built drawings received (if applicable)
□ O&M manuals received (if applicable)
□ Warranty documentation received
□ All permits closed
□ Final lien waiver received
□ All invoices reconciled
□ No back charges pending
□ We have received corresponding retention from owner/GC

APPROVAL:
□ PM Approval: _________________ Date: _______
□ Accounting Verification: _________________ Date: _______

PAYMENT DETAILS:
Check #: _________ Date: _________ Amount: $_________
```

---

## Retention Release Schedule

### Upcoming Releases (Owner → Us)

| Project | Expected Date | Amount | Requirements to Release | Notes |
|---------|---------------|--------|-------------------------|-------|
| Jones Office | 02/01/25 | $11,250 | Complete punchlist, final invoice | 3 items remaining |
| Smith Residence | 03/15/25 | $26,500 | Project completion | Est. complete Feb 25 |
| Main St Retail | 06/30/25 | $78,000 | Project completion | On schedule |
| | | | | |

### Upcoming Releases (Us → Subs)

| Subcontractor | Project | Expected Date | Amount | Requirements | Notes |
|---------------|---------|---------------|--------|--------------|-------|
| ABC Electric | Jones Off | 02/01/25 | $1,550 | Final waiver | Tied to our retention |
| ABC Electric | Smith Res | 03/15/25 | $4,500 | Complete & waiver | |
| DEF Plumbing | Smith Res | 03/15/25 | $3,800 | Complete & waiver | |
| | | | | | |

---

## Monthly Retention Tracking

### Month: _______________

```
MONTHLY RETENTION ACTIVITY

BEGINNING BALANCES (1st of Month):
  Retention Receivable                    $______________
  Retention Payable                       $______________
  Net Position                            $______________

RETENTION HELD THIS MONTH:
  From Owners (new billings)              $______________
  From Subcontractors (new payments)      $______________

RETENTION RELEASED THIS MONTH:
  From Owners (received)                  $______________
  To Subcontractors (paid)                $______________

ENDING BALANCES (End of Month):
  Retention Receivable                    $______________
  Retention Payable                       $______________
  Net Position                            $______________

CHANGE IN NET POSITION                    $______________
```

---

## QBO Integration

### Setting Up Retention Accounts

```
RECOMMENDED QBO CHART OF ACCOUNTS

Assets:
  12100 - Retention Receivable (Current Asset)

Liabilities:
  22100 - Retention Payable (Current Liability)

Sub-Accounts by Project (Optional):
  12100 - Retention Receivable
    12101 - Smith Residence Retention
    12102 - Jones Office Retention
    12103 - Main St Retail Retention

  22100 - Retention Payable
    22101 - Smith Residence - Sub Retention
    22102 - Jones Office - Sub Retention
    22103 - Main St Retail - Sub Retention
```

### Recording Retention in QBO

**When Billing with Retention:**
1. Create invoice for full work completed
2. Create credit memo for retention amount
3. Apply credit memo to invoice
4. Journal entry: DR Retention Receivable, CR A/R

**When Paying Sub with Retention:**
1. Record bill for full amount
2. Apply partial payment (less retention)
3. Journal entry: DR A/P, CR Retention Payable

**When Releasing Retention:**
1. Invoice owner for retention
2. When collected: DR Cash, CR Retention Receivable
3. Pay sub retention: DR Retention Payable, CR Cash

---

## Retention Tracking Reports

### QBO Reports to Run

| Report | Purpose | Frequency |
|--------|---------|-----------|
| Balance Sheet | Verify retention balances | Monthly |
| A/R Aging by Customer | Identify outstanding retention invoices | Weekly |
| A/P Aging by Vendor | Track retention owed to subs | Weekly |
| Transaction List by Account | Detail for 12100/22100 | Monthly |

### Custom Report: Retention Reconciliation

```
RETENTION BALANCE RECONCILIATION

As of: ____________

RETENTION RECEIVABLE (12100):
  QBO Balance:                            $______________

  Per Tracker:
    Project 1                             $______________
    Project 2                             $______________
    Project 3                             $______________
    Total per Tracker                     $______________

  Difference                              $______________

  Explanation: _________________________________________

RETENTION PAYABLE (22100):
  QBO Balance:                            $______________

  Per Tracker:
    Sub 1                                 $______________
    Sub 2                                 $______________
    Sub 3                                 $______________
    Total per Tracker                     $______________

  Difference                              $______________

  Explanation: _________________________________________

Reconciled by: _________________ Date: _____________
```

---

## Best Practices

### For Retention Receivables

1. **Invoice promptly** - Submit retention invoice as soon as eligible
2. **Track expiration** - Some contracts have retention release deadlines
3. **Follow up regularly** - Don't let retention age without action
4. **Document completion** - Maintain closeout documentation
5. **Know your rights** - Understand state prompt pay laws

### For Retention Payables

1. **Release promptly** - Pay subs when you receive your retention
2. **Get final waivers** - Always collect before releasing
3. **Verify completion** - Ensure all work is truly complete
4. **Back charge first** - Deduct any back charges before release
5. **Maintain documentation** - Keep records of release conditions

### General

1. **Reconcile monthly** - Match tracker to QBO balances
2. **Update regularly** - Keep tracker current with every payment
3. **Track by project** - Know retention position per job
4. **Watch cash flow** - Retention release = positive cash event
5. **Review contracts** - Know retention terms before starting

---

## Formulas for Excel/Sheets

### Calculate Retention Held
```
= Total Billed × Retention %
```

### Calculate Balance Due
```
= Retention Held - Released
```

### Days Since Substantial Completion
```
= TODAY() - Substantial Completion Date
```

### Aging Category
```
= IF(Status="Active", "Active",
    IF(Days<=30, "0-30",
    IF(Days<=60, "31-60",
    IF(Days<=90, "61-90", "Over 90"))))
```

---

## Alerts and Reminders

```
SET UP ALERTS FOR:

□ Retention over 30 days past substantial completion - FOLLOW UP
□ Retention release conditions met - SUBMIT INVOICE
□ Subcontractor retention ready for release - VERIFY & PAY
□ Monthly retention reconciliation due
□ Contract retention terms about to expire

REVIEW SCHEDULE:
□ Weekly: Check for completed projects ready for retention release
□ Monthly: Reconcile tracker to QBO
□ Quarterly: Review all aging retention receivables
```

---

*Template designed for use with QBO Construction Accounting Guide*
