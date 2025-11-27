# Progress Billing & Applications for Payment

## Overview

Progress billing is how construction companies invoice for work performed during a project. Unlike retail businesses that sell products at point-of-sale, contractors bill incrementally based on work completed.

This chapter covers the complete progress billing workflow, from Schedule of Values to AIA forms to QBO implementation.

---

## Why Progress Billing Exists

### The Construction Cash Flow Challenge

```
MANUFACTURING COMPANY:
Day 1: Buy materials    → Day 5: Make product    → Day 6: Sell product    → Day 10: Get paid
       $100                     $150 value              $200 invoice              $200 cash
       
CONSTRUCTION COMPANY:
Month 1-3: Buy materials + Labor + Subs → Month 4-6: More work → Month 6: Bill → Month 8: Get paid
           $500,000 outflow                 $300,000 outflow        $850,000        $765,000
                                                                                    (10% retention)
```

**The Problem**: Contractors spend money for months before receiving payment. Without progress billing, you'd need massive capital reserves.

**The Solution**: Bill customers monthly (or more frequently) based on work completed.

---

## The Schedule of Values (SOV)

### What is a Schedule of Values?

The Schedule of Values is a detailed breakdown of your contract price by line item. It's submitted at project start and becomes the basis for all progress billings.

### WHY the SOV Matters

> **Contract Principle**: The SOV establishes the agreed-upon value of each work component. It prevents disputes by documenting in advance how progress will be measured.

**For the Contractor:**
- Defines billing structure upfront
- Prevents owner from cherry-picking what to pay
- Creates predictable billing schedule

**For the Owner:**
- Ensures payments match actual progress
- Prevents front-loading (billing more early in project)
- Creates payment audit trail

### Creating an Effective SOV

**HOW to Structure Your SOV:**

```
SCHEDULE OF VALUES
Project: ABC Corporate Office Buildout
Contract Amount: $1,500,000
Date: January 15, 2024

┌──────┬────────────────────────────────────────┬──────────────────┐
│ Item │ Description of Work                    │ Scheduled Value  │
├──────┼────────────────────────────────────────┼──────────────────┤
│ 1    │ General Conditions (10%)               │ $150,000         │
│ 2    │ Site Work & Demolition                 │ $75,000          │
│ 3    │ Concrete & Foundation                  │ $120,000         │
│ 4    │ Structural Steel                       │ $180,000         │
│ 5    │ Exterior Framing & Sheathing           │ $145,000         │
│ 6    │ Roofing                                │ $85,000          │
│ 7    │ Doors, Frames, Hardware                │ $65,000          │
│ 8    │ Windows & Glazing                      │ $95,000          │
│ 9    │ Interior Framing & Drywall             │ $125,000         │
│ 10   │ Flooring                               │ $80,000          │
│ 11   │ Painting & Finishes                    │ $55,000          │
│ 12   │ Mechanical (HVAC)                      │ $130,000         │
│ 13   │ Electrical                             │ $115,000         │
│ 14   │ Plumbing                               │ $65,000          │
│ 15   │ Fire Protection                        │ $35,000          │
│ 16   │ Specialties & Accessories              │ $15,000          │
│ 17   │ Final Cleanup & Punch List             │ $15,000          │
├──────┴────────────────────────────────────────┼──────────────────┤
│ CONTRACT TOTAL                                │ $1,500,000       │
└───────────────────────────────────────────────┴──────────────────┘
```

**SOV Best Practices:**

| Do | Don't | WHY |
|-----|-------|-----|
| Match CSI divisions | Use vague categories | Industry standard, easier owner approval |
| Include General Conditions line | Spread GC costs across items | Allows billing before production work starts |
| Balance line item values | Create one giant line item | Even cash flow through project |
| Get owner approval | Start billing without SOV | Avoids payment disputes |
| Include all change orders | Leave COs off SOV | Ensures complete billing |

### The General Conditions Line Item

> **WHY General Conditions is Important**: General Conditions (overhead costs specific to the project—supervision, temporary facilities, insurance, etc.) are typically billed proportionally throughout the project. A 10% GC line item billed monthly smooths cash flow.

---

## Understanding AIA Billing Forms

### The Industry Standard

The American Institute of Architects (AIA) documents are the construction industry standard for progress billing:

- **AIA G702**: Application and Certificate for Payment (summary page)
- **AIA G703**: Continuation Sheet (line item detail, follows SOV)

### AIA G702 - Application and Certificate for Payment

**WHY G702 Exists**: Creates a standardized payment request format that:
- Summarizes all billing information on one page
- Shows work completed this period and total to date
- Accounts for retention
- Requires contractor certification
- Provides space for architect certification

**Key G702 Sections:**

```
┌────────────────────────────────────────────────────────────────────────┐
│              APPLICATION AND CERTIFICATE FOR PAYMENT                    │
│                           AIA DOCUMENT G702                             │
├────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  TO OWNER:        ABC Development LLC                                   │
│  PROJECT:         Corporate Office Buildout                             │
│  APPLICATION NO:  3                                                     │
│  PERIOD TO:       March 31, 2024                                        │
│                                                                         │
│  ─────────────────────────────────────────────────────────────────────  │
│                                                                         │
│  1. ORIGINAL CONTRACT SUM                           $1,500,000.00       │
│  2. Net change by Change Orders                     $    50,000.00      │
│  3. CONTRACT SUM TO DATE (1 + 2)                    $1,550,000.00       │
│  4. TOTAL COMPLETED & STORED TO DATE                $  620,000.00       │
│     (Column G on G703)                                                  │
│  5. RETAINAGE:                                                          │
│     a. 10% of Completed Work    $62,000.00                              │
│     b. 10% of Stored Material   $    0.00                               │
│     Total Retainage             $62,000.00                              │
│  6. TOTAL EARNED LESS RETAINAGE (4-5)               $  558,000.00       │
│  7. LESS PREVIOUS CERTIFICATES FOR PAYMENT          $  378,000.00       │
│  8. CURRENT PAYMENT DUE (6-7)                       $  180,000.00       │
│  9. BALANCE TO FINISH, INCLUDING RETAINAGE          $  992,000.00       │
│                                                                         │
│  ─────────────────────────────────────────────────────────────────────  │
│                                                                         │
│  CONTRACTOR CERTIFICATION:                                              │
│  I hereby certify that the Work covered by this Application             │
│  for Payment has been completed in accordance with the Contract.        │
│                                                                         │
│  Signature: _________________ Date: _____________                       │
│                                                                         │
└────────────────────────────────────────────────────────────────────────┘
```

### AIA G703 - Continuation Sheet

**WHY G703 Exists**: Provides line-item detail to support the G702 summary. Each SOV line item is tracked with:
- Work completed from previous applications
- Work completed this period
- Materials presently stored
- Total completed and stored to date
- Percentage complete
- Balance to finish
- Retainage

**G703 Column Structure:**

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                    CONTINUATION SHEET - AIA G703                                                        │
├──────┬─────────────────────┬───────────┬──────────────────────────────────────────────┬───────┬───────────┬────────────┤
│      │                     │           │         WORK COMPLETED                       │       │           │            │
│ Item │ Description         │ Scheduled │───────────────────────────────────────────────│ TOTAL │ % (G÷C)  │ Balance    │
│      │                     │ Value     │ From Prior │ This Period│ Materials │ TO DATE │       │          │ to Finish  │
│  A   │         B           │    C      │     D      │     E      │    F      │   G     │   H   │          │  (C - G)   │
├──────┼─────────────────────┼───────────┼────────────┼────────────┼───────────┼─────────┼───────┼──────────┼────────────┤
│ 1    │ General Conditions  │ $150,000  │ $45,000    │ $15,000    │ $0        │ $60,000 │ 40%   │          │ $90,000    │
│ 2    │ Site Work & Demo    │ $75,000   │ $75,000    │ $0         │ $0        │ $75,000 │ 100%  │          │ $0         │
│ 3    │ Concrete & Found.   │ $120,000  │ $120,000   │ $0         │ $0        │ $120,000│ 100%  │          │ $0         │
│ 4    │ Structural Steel    │ $180,000  │ $90,000    │ $90,000    │ $0        │ $180,000│ 100%  │          │ $0         │
│ 5    │ Ext. Framing        │ $145,000  │ $72,500    │ $58,000    │ $0        │ $130,500│ 90%   │          │ $14,500    │
│ 6    │ Roofing             │ $85,000   │ $0         │ $0         │ $0        │ $0      │ 0%    │          │ $85,000    │
│ ...  │ ...                 │ ...       │ ...        │ ...        │ ...       │ ...     │ ...   │          │ ...        │
├──────┴─────────────────────┼───────────┼────────────┼────────────┼───────────┼─────────┼───────┼──────────┼────────────┤
│ TOTALS                     │$1,550,000 │ $420,000   │ $200,000   │ $0        │ $620,000│ 40%   │          │ $930,000   │
└────────────────────────────┴───────────┴────────────┴────────────┴───────────┴─────────┴───────┴──────────┴────────────┘
```

---

## Progress Billing in QBO: Step-by-Step

### Option 1: Basic Progress Billing (Simple Invoices)

For smaller projects or when GC doesn't require AIA forms:

**HOW to Create a Progress Bill:**

1. Go to **+ New** → **Invoice**
2. Select **Customer/Project**
3. In the description field, enter billing period: "Progress Billing #3 - Work through March 31, 2024"
4. Add line items matching your SOV:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ INVOICE                                                                      │
│ Customer: ABC Development - Corporate Office Project                        │
│ Invoice Date: April 1, 2024                                                 │
│ Due Date: April 30, 2024                                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│ Progress Billing #3 - Work Completed Through March 31, 2024                 │
│                                                                              │
│ PRODUCT/SERVICE              │ QTY │ RATE        │ AMOUNT                    │
│ ─────────────────────────────┼─────┼─────────────┼──────────────────────────│
│ General Conditions (March)   │ 1   │ $15,000.00  │ $15,000.00               │
│ Structural Steel - Complete  │ 1   │ $90,000.00  │ $90,000.00               │
│ Exterior Framing (90%)       │ 1   │ $58,000.00  │ $58,000.00               │
│ Interior Framing (20%)       │ 1   │ $25,000.00  │ $25,000.00               │
│ Mechanical Rough-In (30%)    │ 1   │ $39,000.00  │ $39,000.00               │
│ ─────────────────────────────┼─────┼─────────────┼──────────────────────────│
│ SUBTOTAL                     │     │             │ $227,000.00              │
│ Less: 10% Retention          │     │             │ ($22,700.00)             │
│ ─────────────────────────────┼─────┼─────────────┼──────────────────────────│
│ AMOUNT DUE                   │     │             │ $204,300.00              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Option 2: Progress Billing with Estimates (Recommended)

Using QBO Estimates creates a trackable relationship between contract value and billings.

**HOW to Set Up Estimate-Based Billing:**

**Step 1: Create the Estimate (Contract)**
1. Go to **+ New** → **Estimate**
2. Select Customer/Project
3. Add all SOV line items with their scheduled values
4. Save as your "Contract Estimate"

**Step 2: Create Progress Invoice from Estimate**
1. Go to **Sales** → **All Sales** → Find your estimate
2. Click **Create invoice**
3. Choose "A percentage of each line"
4. Enter the percentage complete for each line item this period
5. Adjust line items as needed
6. Add retention as negative line item
7. Save

**WHY This Method is Better:**
- QBO tracks % invoiced vs. estimate
- You can see remaining contract value
- Creates audit trail from contract to billing

### Option 3: Using QBO Projects + Milestones

For QBO Advanced users with Projects enabled:

**HOW:**
1. Create Project for the job
2. Add milestones matching SOV items
3. Mark milestones complete as work progresses
4. Generate invoices from milestone completion

### Setting Up Retention as a Line Item

**WHY Retention Needs Special Handling:**
Retention (typically 5-10%) is withheld from each payment until project completion. In QBO, there's no built-in retention tracking, so we use a negative line item.

**HOW to Create Retention Product:**

1. Go to **Settings ⚙️** → **Products and Services**
2. Click **New** → **Service**
3. Fill in:
   - **Name**: Retention Withheld - 10%
   - **Income Account**: Select your Retention Receivable account (or create one)
   - Leave rate blank (will enter per invoice)
4. Save

**When Invoicing:**
Add as final line item with negative amount:
```
Retention Withheld - 10% | -$22,700.00
```

---

## Matching Progress Billing to Earned Revenue

### The Connection to WIP

Your progress billing should ideally match your earned revenue from the WIP schedule. In practice, there are always differences (that's why over/under billing exists).

**The Ideal Scenario:**
```
Earned Revenue (per WIP):     $620,000
Billings to Date:             $620,000
Over/Under Billing:           $0

Reality:
Earned Revenue (per WIP):     $620,000
Billings to Date:             $620,000 (this month's billing)
Over/Under Billing:           Will calculate after billings reconcile
```

**WHY Perfect Matching is Rare:**
- Billing cycles don't match cost timing
- Some work is hard to quantify until complete
- Customer approval delays billing
- Change order billing lags approval

### Using WIP to Guide Billing

**Best Practice**: Run your WIP analysis before preparing progress billing.

```
WIP Shows:
  Job A: 40% complete, Earned Revenue = $400,000
  Billings to Date (prior): $380,000
  Suggested This Period Billing: $20,000 to catch up

Decision:
  - Bill $20,000 minimum to avoid under-billing growth
  - Consider billing more if work supports it
```

---

## Billing Workflow: Complete Process

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                        PROGRESS BILLING WORKFLOW                                     │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  PREPARATION (Days 1-3 of month)                                                     │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ 1. Project Manager prepares % complete for each SOV line item                   ││
│  │ 2. Document any materials stored on site (if billing stored materials)          ││
│  │ 3. Note any change orders to include                                            ││
│  │ 4. Compare to WIP to ensure billing matches earned revenue                       ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                              │                                                       │
│                              ▼                                                       │
│  BILLING CREATION (Days 3-5)                                                         │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ 5. Complete G703 continuation sheet with current period work                    ││
│  │ 6. Complete G702 summary (auto-calculates from G703)                            ││
│  │ 7. Create corresponding invoice in QBO                                          ││
│  │ 8. Attach supporting documentation (daily reports, photos, etc.)                 ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                              │                                                       │
│                              ▼                                                       │
│  SUBMISSION (Day 5)                                                                  │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ 9. Submit to Architect/Owner per contract requirements                          ││
│  │ 10. Include lien waivers (conditional for current, unconditional for prior)     ││
│  │ 11. Track submission date for payment timeline                                   ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                              │                                                       │
│                              ▼                                                       │
│  FOLLOW-UP (Days 10-30)                                                              │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ 12. Confirm architect certification (if required)                               ││
│  │ 13. Track payment per contract terms                                            ││
│  │ 14. Follow up on unpaid invoices                                                ││
│  │ 15. Apply payment when received                                                 ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

---

## Materials Stored On-Site Billing

### WHY Bill for Stored Materials?

Large material purchases (structural steel, major equipment) are often delivered before installation. Billing for stored materials:
- Improves contractor cash flow
- Customer pays for materials they own
- Reduces contractor financing costs

### Requirements for Billing Stored Materials

Most contracts require:
1. **Segregated storage**: Materials clearly separated and identified
2. **Insurance**: Adequate coverage for stored materials
3. **Documentation**: Photos, delivery tickets, invoices
4. **Bill of sale**: Proof of purchase

### HOW to Bill Stored Materials in QBO

1. Create invoice line item: "Stored Materials - [Description]"
2. Amount: Material cost (per contract terms—some allow markup)
3. Note in description: Location, date delivered, protected storage confirmation
4. Attach documentation to invoice

**Example:**
```
Stored Materials - Structural Steel Package A    $45,000.00
(Delivered 3/15/24, stored at site, protected, insured)
```

**In Next Month's Billing:**
When materials are installed, credit stored materials:
```
Structural Steel - Installed              $45,000.00
Less: Previously Billed Stored Materials -$45,000.00
Net This Period                           $0.00
```

---

## Change Order Billing

### WHY Separate Change Order Billing?

> **Contract Principle**: Change orders modify the original contract. Tracking them separately ensures:
> - Original contract profitability is measurable
> - Change order profitability is visible
> - Contract compliance is documented

### HOW to Bill Change Orders

**Method 1: Add to G703 as New Line Item**
```
G703 Addition:
Item 18: CO #1 - Additional Electrical | $25,000 | 100% | $25,000
Item 19: CO #2 - Upgraded Finishes     | $15,000 | 50%  | $7,500
```

**Method 2: Separate Change Order Invoice**
Some contracts require separate invoicing. Create a new invoice:
```
Change Order Invoice #1
Ref: Change Order #1 - Approved 3/10/24
Description: Additional electrical service for server room
Amount: $25,000.00
Less 10% Retention: ($2,500.00)
Due: $22,500.00
```

### Pending vs. Approved Change Orders

**CRITICAL**: Only bill for **approved** change orders.

| Status | Can Bill? | How to Track |
|--------|-----------|--------------|
| Proposed | No | Track costs in job costing, don't bill |
| Pending Owner Approval | No | Document in billing notes |
| Approved | Yes | Add to SOV and bill |
| Disputed | No | Negotiate resolution, don't bill until resolved |

---

## Common Progress Billing Mistakes

### Mistake 1: Front-Loading

**What It Is**: Billing higher percentages early in project
**Why It's a Problem**: 
- Can damage customer relationship
- Creates cash flow problems later
- May violate contract terms
**Solution**: Bill actual % complete per trade

### Mistake 2: Not Billing Retention Correctly

**What It Is**: Forgetting to subtract retention or tracking incorrectly
**Impact**: AR doesn't match actual receivable
**Solution**: Always include retention line item, track in separate account

### Mistake 3: Billing Without Documentation

**What It Is**: Submitting pay apps without supporting docs
**Impact**: Payment delays, disputes
**Solution**: Standardize documentation package with every billing

### Mistake 4: Ignoring Contract Billing Terms

**What It Is**: Billing whenever convenient vs. per contract
**Impact**: Payment delays, contract disputes
**Solution**: Calendar billing dates, submit on time

### Mistake 5: Not Reconciling to WIP

**What It Is**: Billing without checking earned revenue
**Impact**: Significant over/under billing
**Solution**: WIP review before every billing cycle

---

## Lien Waivers: The Payment Protection

### WHY Lien Waivers Matter

Lien waivers protect both parties:
- **Owner**: Confirmation that you've been paid (reduces double payment risk)
- **Contractor**: Formalizes payment receipt, documents payment timeline

### Types of Lien Waivers

| Type | When Used | What It Covers |
|------|-----------|----------------|
| Conditional - Progress | With progress bill | Current payment, IF payment received |
| Unconditional - Progress | After payment received | Confirms prior payment received |
| Conditional - Final | With final bill | All remaining amounts |
| Unconditional - Final | After final payment | Releases all lien rights |

### Lien Waiver Workflow

```
Progress Billing #3 Submitted ──▶ Include: Conditional Waiver for #3
                                          Unconditional Waiver for #2
                                          
Payment #3 Received ──▶ Next billing includes: Unconditional Waiver for #3
```

---

## Progress Billing Checklist

### Before Preparing Billing:
- [ ] Review contract billing terms and dates
- [ ] Get PM sign-off on % complete per line item
- [ ] Identify any stored materials to bill
- [ ] List approved change orders to include
- [ ] Compare to WIP earned revenue

### When Preparing Billing:
- [ ] Update G703 with current period work
- [ ] Calculate G702 summary
- [ ] Calculate retention correctly
- [ ] Verify math (column totals match)
- [ ] Create matching invoice in QBO

### When Submitting:
- [ ] Include all required documentation
- [ ] Include appropriate lien waivers
- [ ] Submit per contract method (mail, email, portal)
- [ ] Document submission date
- [ ] Set follow-up reminder for payment date

---

## Next Steps

With progress billing set up, the next challenge is tracking retention—the money that's withheld until project completion. In [Retention Tracking](./06-retention-tracking.md), you'll learn:
- Setting up retention receivable/payable accounts
- Tracking retention by project
- Billing for retention release
- Retention aging reports

---

*[← Previous: WIP Schedules](./04-wip-schedules.md) | [Next: Retention Tracking →](./06-retention-tracking.md)*
