# Change Order Management in QuickBooks Online

## Overview

Change orders are modifications to the original construction contract—changes in scope, design, materials, or conditions that affect the contract price. Proper change order tracking is critical because:

- They directly affect job profitability
- Approved change orders increase (or decrease) contract value
- Unapproved work is a major source of disputes
- Change order margin often differs from original contract margin

This chapter provides a complete system for managing change orders in QBO.

---

## Understanding Change Orders

### What Triggers a Change Order?

| Trigger | Example | Who Initiates |
|---------|---------|---------------|
| Owner request | "Add a bathroom" | Owner |
| Design changes | Architect revises plans | Owner/Architect |
| Field conditions | Rock discovered during excavation | Contractor |
| Code requirements | Inspector requires additional fire stopping | Contractor |
| Errors & omissions | Plans missing structural detail | Varies |
| Substitutions | Material specified unavailable | Either |
| Acceleration | "Finish 2 weeks early" | Owner |

### Change Order Lifecycle

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                           CHANGE ORDER LIFECYCLE                                     │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                      │
│  1. IDENTIFICATION                                                                   │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ Change in scope identified                                                       ││
│  │ Field documentation started                                                      ││
│  │ Initial cost estimate prepared                                                   ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                              │                                                       │
│                              ▼                                                       │
│  2. PROPOSAL                                                                         │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ Formal change order proposal prepared                                            ││
│  │ Pricing detailed: Labor + Materials + Equipment + OH&P                           ││
│  │ Schedule impact documented                                                       ││
│  │ Submitted to owner/architect                                                     ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                              │                                                       │
│                              ▼                                                       │
│  3. NEGOTIATION                                                                      │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ Owner/architect reviews proposal                                                 ││
│  │ May request additional information                                               ││
│  │ Price negotiation (if applicable)                                                ││
│  │ Status: PENDING                                                                  ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                              │                                                       │
│              ┌───────────────┴───────────────┐                                       │
│              ▼                               ▼                                       │
│  4a. APPROVAL                        4b. REJECTION                                   │
│  ┌──────────────────────┐            ┌──────────────────────┐                        │
│  │ Signed change order  │            │ Work does not proceed│                        │
│  │ Contract modified    │            │ No revenue/cost      │                        │
│  │ Status: APPROVED     │            │ Status: REJECTED     │                        │
│  └──────────────────────┘            └──────────────────────┘                        │
│              │                                                                       │
│              ▼                                                                       │
│  5. EXECUTION & BILLING                                                              │
│  ┌─────────────────────────────────────────────────────────────────────────────────┐│
│  │ Work performed                                                                   ││
│  │ Costs tracked against change order                                               ││
│  │ Billing per contract terms                                                       ││
│  │ Status: IN PROGRESS → COMPLETE                                                   ││
│  └─────────────────────────────────────────────────────────────────────────────────┘│
│                                                                                      │
└─────────────────────────────────────────────────────────────────────────────────────┘
```

### WHY Change Order Management Matters

> **Contract Principle**: Work performed outside the original contract scope without written authorization creates significant legal and financial risk.

**Without Proper Change Order Tracking:**
- You may perform work you can't bill for
- Project profitability becomes impossible to measure
- Disputes become he-said/she-said
- Cash flow forecasting fails

---

## Change Order Status Categories

### Critical: Track Status Separately

Not all change orders are equal. Your tracking system must distinguish:

| Status | Can Bill? | Include in Contract Value? | Track Costs? |
|--------|-----------|---------------------------|--------------|
| **Proposed** | No | No | Yes (separate) |
| **Pending** | No | No | Yes (separate) |
| **Approved** | Yes | Yes | Yes |
| **Rejected** | No | No | Stop tracking |
| **Complete** | Yes (if not fully billed) | Yes | Yes |

### The Danger of Pending Change Orders

```
COMMON SCENARIO:

Project Manager: "The owner wants us to add the extra wall, they'll approve it."
Accountant: "Is it signed?"
Project Manager: "No, but they said to start. We need to keep the schedule."

SIX WEEKS LATER:
Owner: "We never approved that change order. We're not paying $25,000."
Contractor: "But we already did the work!"

RESULT: $25,000 unbillable cost
```

**Best Practice**: Never bill for unapproved change orders. Track costs separately until approved.

---

## Setting Up Change Order Tracking in QBO

### Account Structure for Change Orders

**Income Accounts:**

| Account # | Name | Type | Purpose |
|-----------|------|------|---------|
| 40600 | Change Order Revenue | Income | All approved CO revenue |
| 40610 | ↳ CO - Owner Requests | Income | Owner-initiated changes |
| 40620 | ↳ CO - Field Conditions | Income | Changed conditions |
| 40630 | ↳ CO - Design Changes | Income | Architect/design changes |

**Cost Accounts:**

| Account # | Name | Type | Purpose |
|-----------|------|------|---------|
| 51000 | Change Order Costs | COGS | Direct costs on COs |
| 51010 | ↳ CO - Labor | COGS | Labor on COs |
| 51020 | ↳ CO - Materials | COGS | Materials on COs |
| 51030 | ↳ CO - Subcontractors | COGS | Sub costs on COs |

**Asset Account (for Pending COs):**

| Account # | Name | Type | Purpose |
|-----------|------|------|---------|
| 14000 | Pending Change Order Costs | Other Current Assets | Costs incurred on unapproved COs |

### Products/Services for Change Orders

**HOW to Create:**

1. Go to **Settings ⚙️** → **Products and Services**
2. Create:

| Name | Type | Income Account | Use For |
|------|------|----------------|---------|
| Change Order - Approved | Service | 40600 Change Order Revenue | Invoicing approved COs |
| Change Order - Pending | Service | N/A | Tracking only (not invoiced) |

### Change Order Log (External to QBO)

QBO doesn't have native change order tracking. Maintain a log in Excel:

```
CHANGE ORDER LOG
Project: ABC Corporate Office

┌────┬────────────┬─────────────────────────────┬───────────┬─────────────┬──────────┬────────────┬────────────┬──────────┐
│ CO#│ Date       │ Description                 │ Proposed  │ Approved    │ Status   │ Costs      │ Billed     │ % Billed │
│    │ Submitted  │                             │ Amount    │ Amount      │          │ to Date    │ to Date    │          │
├────┼────────────┼─────────────────────────────┼───────────┼─────────────┼──────────┼────────────┼────────────┼──────────┤
│ 1  │ 2/15/2024  │ Additional electrical panel │ $18,500   │ $17,000     │ APPROVED │ $14,200    │ $17,000    │ 100%     │
│ 2  │ 2/28/2024  │ Upgraded flooring - lobby   │ $12,000   │ $12,000     │ APPROVED │ $8,500     │ $6,000     │ 50%      │
│ 3  │ 3/10/2024  │ Rock removal - foundation   │ $25,000   │ --          │ PENDING  │ $18,000    │ $0         │ 0%       │
│ 4  │ 3/15/2024  │ Owner-requested ceiling ht  │ $8,500    │ --          │ PROPOSED │ $0         │ $0         │ 0%       │
│ 5  │ 3/18/2024  │ HVAC duct relocation        │ $6,200    │ REJECTED    │ REJECTED │ $0         │ $0         │ N/A      │
├────┴────────────┴─────────────────────────────┼───────────┼─────────────┼──────────┼────────────┼────────────┼──────────┤
│ TOTALS - APPROVED                             │ $30,500   │ $29,000     │          │ $22,700    │ $23,000    │          │
│ TOTALS - PENDING                              │ $25,000   │ --          │          │ $18,000    │ $0         │          │
│ TOTALS - PROPOSED                             │ $8,500    │ --          │          │ $0         │ $0         │          │
└───────────────────────────────────────────────┴───────────┴─────────────┴──────────┴────────────┴────────────┴──────────┘
```

---

## Recording Change Order Costs

### For Approved Change Orders

Track costs the same as base contract work, using your change order accounts.

**HOW to Enter Labor:**

1. Enter time with:
   - **Customer**: Project name
   - **Service**: Select a CO-specific service or add CO # to memo
   
**HOW to Enter Materials/Subs:**

1. Create Bill
2. Use Product/Service: Materials - Change Order (or standard item)
3. Add description: "CO #2 - Upgraded flooring materials"
4. Assign to Customer (project)

### For Pending Change Orders (Critical!)

**The Accounting Problem:**
You've incurred real costs, but can't recognize revenue until approved.

**Solution**: Track costs in a separate asset account.

**HOW:**

**Method 1: Direct to Asset Account**

When entering costs for pending COs:

1. Create Bill or Expense
2. Use Account (not Product/Service): 14000 Pending Change Order Costs
3. Add memo: "Pending CO #3 - Rock removal labor"
4. Assign to Customer (project)

**When CO is Approved - Reclassify:**

```
Journal Entry:
Date: [Approval date]
Memo: Reclassify Pending CO #3 to approved - Rock removal

Account                            Debit      Credit    Customer
────────────────────────────────────────────────────────────────────────
51000 Change Order Costs          $18,000               ABC Office
  14000 Pending CO Costs                     $18,000    ABC Office
────────────────────────────────────────────────────────────────────────
```

**Method 2: Track in COGS with Sub-Account**

Some prefer keeping all costs in COGS but separating:

| Account | Purpose |
|---------|---------|
| 51000 Change Order Costs - Approved | Costs on approved COs |
| 51900 Change Order Costs - Pending | Costs on unapproved COs |

At month-end, review 51900 and follow up on approval status.

---

## Billing for Change Orders

### When to Bill Change Orders

| Contract Type | When to Bill COs |
|--------------|------------------|
| Progress Billing | Include in monthly progress billing |
| T&M | Bill as work is performed |
| Lump Sum | Upon approval or per CO terms |
| Unit Price | As units are completed |

### Adding Change Orders to Progress Billing

**Option 1: Add to Schedule of Values**

When CO is approved, add a new line to your SOV:

```
G703 (Continuation Sheet) - After CO Approval:

Original SOV Lines 1-17:     $1,500,000
CO #1 - Add'l Electrical:       $17,000
CO #2 - Flooring Upgrade:       $12,000
─────────────────────────────────────────
REVISED CONTRACT:            $1,529,000
```

**Option 2: Separate CO Billing Section**

```
G703 Section 1: Original Contract Work
  Items 1-17: [standard SOV lines]
  
G703 Section 2: Approved Change Orders
  CO #1: Additional Electrical    $17,000  |  100%  |  $17,000
  CO #2: Flooring Upgrade         $12,000  |  50%   |  $6,000
```

### QBO Invoice for Change Orders

**HOW:**

1. Create Invoice or add to existing progress invoice
2. Add line item:
   - **Product/Service**: Change Order - Approved
   - **Description**: "CO #1 - Additional electrical panel per approved CO dated 2/20/24"
   - **Amount**: Approved amount (or % if partial billing)
3. Apply retention if applicable
4. Save

**Example Invoice Section:**
```
CHANGE ORDERS:
CO #1 - Additional Electrical (100%)        $17,000.00
CO #2 - Upgraded Flooring (50%)             $6,000.00
─────────────────────────────────────────────────────────
Subtotal - Change Orders:                   $23,000.00
Less 10% Retention:                         ($2,300.00)
─────────────────────────────────────────────────────────
Net Change Order Billing:                   $20,700.00
```

---

## Change Order Impact on WIP

### Approved COs Affect Contract Value

When a CO is approved, your WIP schedule must reflect:
1. **Increased Contract Price**: Original + Approved COs
2. **Updated Total Estimated Cost**: Include CO costs
3. **Recalculated % Complete**: Using new totals

**Example:**

```
BEFORE CO #1 Approved:
Contract Price:         $1,500,000
Total Est. Cost:        $1,200,000
Est. Gross Profit:        $300,000 (20%)
Costs to Date:            $400,000
% Complete:               33.3%
Earned Revenue:           $500,000

AFTER CO #1 ($17,000 @ 15% margin) Approved:
Contract Price:         $1,517,000  (+$17,000)
Total Est. Cost:        $1,214,450  (+$14,450)
Est. Gross Profit:        $302,550  (+$2,550)
Costs to Date:            $414,200  (+$14,200 from CO work)
% Complete:               34.1%     (recalculated)
Earned Revenue:           $517,300  (recalculated)
```

### Pending COs and WIP

**WHY Pending COs Are Excluded from WIP:**

> **GAAP Principle**: Revenue recognition requires a valid contract. Pending change orders are not contractually enforceable, therefore no revenue can be recognized.

**Proper Treatment:**
- Contract Price: Original contract only
- Costs: Exclude pending CO costs from % complete calculation
- Disclosure: Note pending COs in WIP schedule footer

```
WIP SCHEDULE FOOTER:

Note: The following change orders are pending approval and 
excluded from contract values and earned revenue calculations:

  CO #3 - Rock Removal: Proposed $25,000, Costs incurred $18,000
  CO #4 - Ceiling Height: Proposed $8,500, Costs incurred $0
  
  Total Pending CO Value:    $33,500
  Total Pending CO Costs:    $18,000
```

---

## Change Order Profitability Analysis

### WHY Analyze CO Profitability Separately

Change orders often have different economics than the base contract:
- May include fewer competitive bids (no rebid requirement)
- May have higher markup allowed (disruption premium)
- May have worse margins (rush pricing, inefficiency)

### Tracking CO Profitability

**Report Structure:**

```
CHANGE ORDER PROFITABILITY REPORT
Project: ABC Corporate Office
As of: March 31, 2024

┌────┬─────────────────────────────┬────────────┬────────────┬────────────┬──────────┐
│ CO#│ Description                 │ Revenue    │ Cost       │ Gross      │ Margin   │
│    │                             │            │            │ Profit     │          │
├────┼─────────────────────────────┼────────────┼────────────┼────────────┼──────────┤
│ 1  │ Additional electrical panel │ $17,000    │ $14,200    │ $2,800     │ 16.5%    │
│ 2  │ Upgraded flooring - lobby   │ $12,000    │ $8,500     │ $3,500     │ 29.2%    │
├────┴─────────────────────────────┼────────────┼────────────┼────────────┼──────────┤
│ TOTAL APPROVED COs              │ $29,000    │ $22,700    │ $6,300     │ 21.7%    │
└─────────────────────────────────┴────────────┴────────────┴────────────┴──────────┘

COMPARISON:
Base Contract Margin:     20.0%
Change Order Margin:      21.7%
Variance:                 +1.7%  (COs are more profitable)
```

### Red Flags in CO Profitability

| Indicator | Problem | Action |
|-----------|---------|--------|
| CO margin < Base margin | Underpricing COs | Review estimating process |
| CO margin negative | Losing money on COs | Stop work, renegotiate |
| High CO volume, low margin | Scope creep issues | Review change control process |
| No COs on complex project | Likely untracked changes | Audit for missing COs |

---

## Change Order Best Practices

### The Golden Rule

> **Never perform change order work without written authorization.**

If verbal authorization is given:
1. Document the conversation in writing
2. Send email confirming: "Per our conversation, we will proceed with [work] while the formal CO is processed."
3. Get written acknowledgment before significant spending

### Pricing Change Orders

**Standard Markup Structure:**

```
CHANGE ORDER PRICING TEMPLATE

Direct Costs:
  Labor (including burden):     $XX,XXX
  Materials:                    $XX,XXX
  Equipment:                    $XX,XXX
  Subcontractors:              $XX,XXX
─────────────────────────────────────────
Subtotal Direct Costs:          $XX,XXX

Markup:
  Overhead (10-15%):            $X,XXX
  Profit (10-15%):              $X,XXX
─────────────────────────────────────────
TOTAL CHANGE ORDER:             $XX,XXX
```

**WHY Standard Markup:**
- Consistent pricing builds trust
- Contractually defensible
- Simplifies estimating

### Change Order Documentation Checklist

For every change order, maintain:

- [ ] Written request or identification of change
- [ ] Detailed cost estimate with backup
- [ ] Impact statement (schedule, other trades)
- [ ] Formal change order proposal
- [ ] Owner/architect correspondence
- [ ] Signed approval (or rejection)
- [ ] Updated SOV/G703 reflecting CO
- [ ] Cost tracking records
- [ ] Final close-out documentation

---

## Disputed Change Orders

### Types of Disputes

| Dispute Type | Example | Resolution Path |
|--------------|---------|-----------------|
| Price disagreement | Owner says $25K, you say $40K | Negotiation, detailed backup |
| Scope disagreement | Owner says base contract, you say extra | Contract interpretation |
| Authorization | You claim verbal approval | Documentation review |
| Backcharges | Owner deducting for claimed defects | Quality documentation |

### Accounting for Disputed COs

**Conservative Approach (Recommended):**
- Do NOT include in contract value
- Do NOT recognize revenue
- Track costs separately
- Disclose in financial statement notes

**When to Recognize:**
Only when:
1. Dispute is resolved in your favor, OR
2. Resolution is probable and amount is estimable (requires strong documentation)

---

## Common Change Order Mistakes

### Mistake 1: Working Without Approval

**Problem**: Starting change order work without written approval
**Impact**: Unbillable costs, disputes
**Solution**: Strict approval-before-work policy

### Mistake 2: Not Tracking CO Costs Separately

**Problem**: CO costs mixed with base contract costs
**Impact**: Can't measure CO profitability, contract analysis impossible
**Solution**: Separate cost accounts or memo tracking

### Mistake 3: Billing Unapproved COs

**Problem**: Including pending COs in progress billing
**Impact**: Overstates receivables, creates disputes
**Solution**: Only bill approved COs

### Mistake 4: Underpricing Change Orders

**Problem**: Not including full costs and markup
**Impact**: COs dilute overall project margin
**Solution**: Standardized pricing template with full costs

### Mistake 5: Poor Documentation

**Problem**: No written records of change requests and approvals
**Impact**: Disputes become unprovable
**Solution**: Document everything, get signatures

### Mistake 6: Forgetting to Update WIP

**Problem**: WIP shows original contract value after COs approved
**Impact**: Incorrect % complete, wrong earned revenue
**Solution**: Update WIP immediately upon CO approval

---

## Change Order Tracking Checklist

### When Change is Identified:
- [ ] Document the change in writing
- [ ] Assign CO number
- [ ] Begin cost estimate
- [ ] Log in change order register

### When Proposal is Submitted:
- [ ] Formal CO proposal sent to owner
- [ ] Save copy with date sent
- [ ] Set follow-up reminder
- [ ] Status: PROPOSED in log

### During Negotiation:
- [ ] Track all correspondence
- [ ] Document any verbal agreements in writing
- [ ] Update cost estimate if scope changes
- [ ] Status: PENDING in log

### Upon Approval:
- [ ] Get signed change order document
- [ ] Update change order log: Status = APPROVED
- [ ] Update contract value in WIP
- [ ] Add to Schedule of Values
- [ ] Begin billing
- [ ] Reclassify any pending costs to approved

### Upon Rejection:
- [ ] Document rejection in writing
- [ ] Status: REJECTED in log
- [ ] Stop any work in progress
- [ ] Evaluate dispute options if applicable

---

## Next Steps

You've now completed the core tutorials on construction accounting in QBO. The following reference sections will provide:
- [Chart of Accounts Templates](../templates/09-chart-of-accounts.md) - Ready-to-use account structures
- [Common Mistakes to Avoid](../reference/10-common-mistakes.md) - Lessons learned
- [Month-End Close Checklist](../checklists/11-month-end-close.md) - Step-by-step closing process
- [GAAP Principles Reference](../reference/12-gaap-principles.md) - Accounting standards explained

---

*[← Previous: Equipment Allocation](./07-equipment-allocation.md) | [Next: Chart of Accounts Templates →](../templates/09-chart-of-accounts.md)*
