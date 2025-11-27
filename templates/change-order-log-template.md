# Change Order Log Template

## Instructions

Use this template to track all change orders across your projects. Copy into Excel or Google Sheets for easy filtering, sorting, and reporting.

---

## Change Order Log

### Header Information

```
COMPANY: _________________________________
PREPARED BY: _____________________________
DATE: ____________________________________
```

---

### Change Order Master Log

| CO# | Project | CO Date | Description | Type | Requested By | Status | Original Amount | Approved Amount | Cost Impact | Margin | Days Added | Submit Date | Approval Date | Invoice # | Notes |
|-----|---------|---------|-------------|------|--------------|--------|-----------------|-----------------|-------------|--------|------------|-------------|---------------|-----------|-------|
| 001 | Smith Residence | 11/1/24 | Upgraded kitchen cabinets | Owner Request | Owner | Approved | $12,500 | $12,500 | $9,800 | 21.6% | 0 | 11/1/24 | 11/5/24 | INV-1045 | |
| 002 | Smith Residence | 11/8/24 | Added recessed lighting (6) | Owner Request | Owner | Approved | $2,400 | $2,200 | $1,600 | 27.3% | 0 | 11/8/24 | 11/10/24 | INV-1046 | Negotiated |
| 003 | Smith Residence | 11/15/24 | Unforeseen soil condition | Site Condition | Contractor | Pending | $8,500 | - | $8,500 | 0% | 5 | 11/15/24 | - | - | Awaiting approval |
| 004 | Jones Office | 10/20/24 | Additional electrical outlets | Owner Request | Architect | Approved | $4,200 | $4,200 | $3,100 | 26.2% | 0 | 10/20/24 | 10/28/24 | INV-1038 | |
| 005 | Jones Office | 11/5/24 | HVAC capacity upgrade | Design Change | Engineer | Approved | $18,000 | $18,000 | $15,200 | 15.6% | 3 | 11/5/24 | 11/12/24 | INV-1044 | |
| 006 | Jones Office | 11/18/24 | Delete break room sink | Owner Request | Owner | Approved | ($1,800) | ($1,800) | ($1,400) | 22.2% | 0 | 11/18/24 | 11/19/24 | CR-005 | Credit |
| | | | | | | | | | | | | | | | |

---

### Column Definitions

| Column | Description | Example Values |
|--------|-------------|----------------|
| **CO#** | Sequential change order number | 001, 002, 003 |
| **Project** | Project name or number | Smith Residence |
| **CO Date** | Date change order originated | 11/1/24 |
| **Description** | Brief description of change | Upgraded kitchen cabinets |
| **Type** | Category of change | Owner Request, Site Condition, Design Change, Code Requirement |
| **Requested By** | Who initiated the change | Owner, Architect, Engineer, Contractor |
| **Status** | Current status | Pending, Submitted, Approved, Rejected, Withdrawn |
| **Original Amount** | Amount initially requested | $12,500 |
| **Approved Amount** | Final approved amount | $12,500 (may differ from original) |
| **Cost Impact** | Your cost to perform the change | $9,800 |
| **Margin** | (Approved - Cost) / Approved × 100 | 21.6% |
| **Days Added** | Schedule extension (if any) | 5 days |
| **Submit Date** | Date submitted to owner/GC | 11/1/24 |
| **Approval Date** | Date approved | 11/5/24 |
| **Invoice #** | QBO invoice number when billed | INV-1045 |
| **Notes** | Additional information | Negotiated, Disputed, etc. |

---

### Summary by Project

```
PROJECT CHANGE ORDER SUMMARY

Project: Smith Residence
─────────────────────────────────────────────────────────────────────────────────
                              Count    Amount      Cost        Margin
─────────────────────────────────────────────────────────────────────────────────
Approved Change Orders           2    $14,700    $11,400       22.4%
Pending Change Orders            1     $8,500     $8,500        0.0%
Rejected Change Orders           0         $0         $0         N/A
─────────────────────────────────────────────────────────────────────────────────
TOTAL                            3    $23,200    $19,900       14.2%

Original Contract Value:    $285,000
Approved COs:                $14,700
Current Contract Value:     $299,700 (5.2% increase)

Days Added: 5
─────────────────────────────────────────────────────────────────────────────────

Project: Jones Office
─────────────────────────────────────────────────────────────────────────────────
                              Count    Amount      Cost        Margin
─────────────────────────────────────────────────────────────────────────────────
Approved Change Orders           3    $20,400    $16,900       17.2%
Pending Change Orders            0         $0         $0         N/A
Rejected Change Orders           0         $0         $0         N/A
─────────────────────────────────────────────────────────────────────────────────
TOTAL                            3    $20,400    $16,900       17.2%

Original Contract Value:    $450,000
Approved COs:                $20,400
Current Contract Value:     $470,400 (4.5% increase)

Days Added: 3
─────────────────────────────────────────────────────────────────────────────────
```

---

### Change Order Type Analysis

```
CHANGE ORDER ANALYSIS BY TYPE

Type                    Count    Total Value    % of All COs
─────────────────────────────────────────────────────────────────
Owner Request              4       $29,100          83.7%
Site Condition             1        $8,500          24.4%
Design Change              1       $18,000          51.7%
Code Requirement           0            $0           0.0%
─────────────────────────────────────────────────────────────────
TOTAL                      6       $55,600         100.0%

Note: Percentages may exceed 100% when analyzing specific projects
```

---

### Status Summary

```
CHANGE ORDER STATUS SUMMARY (All Projects)

Status                  Count    Total Value
─────────────────────────────────────────────────────────────
Pending                    1        $8,500
Submitted                  0            $0
Approved                   5       $35,100
Rejected                   0            $0
Withdrawn                  0            $0
─────────────────────────────────────────────────────────────
TOTAL                      6       $43,600
```

---

### Aging Report (Pending COs)

```
PENDING CHANGE ORDER AGING

CO#    Project          Submitted    Days Out    Amount      Status Notes
─────────────────────────────────────────────────────────────────────────────────
003    Smith Residence  11/15/24     12 days     $8,500      Awaiting owner review
─────────────────────────────────────────────────────────────────────────────────
TOTAL PENDING                                    $8,500

ACTION REQUIRED:
□ CO 003 - Follow up with owner by 11/29/24
```

---

## Excel Formula References

### For Calculating Margin
```
= (Approved Amount - Cost Impact) / Approved Amount
```

### For Days Since Submission (Pending COs)
```
= TODAY() - Submit Date
```

### For Conditional Formatting (Pending > 14 days)
```
Apply red highlight where Days Out > 14
```

---

## Tips for Using This Template

1. **Update daily** - Log changes when they occur
2. **Track ALL changes** - Even if you think they won't be approved
3. **Document thoroughly** - Good descriptions prevent disputes
4. **Link to QBO** - Record invoice numbers when billed
5. **Follow up on pending** - Don't let COs age without action
6. **Review margins** - COs should be profitable too
7. **Track time impacts** - Schedule extensions matter

---

*Template designed for use with QBO Construction Accounting Guide*
