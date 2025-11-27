# Industry-Specific Construction Accounting Guides

## Overview

While the core principles of construction accounting apply across all trades, each segment of the construction industry has unique requirements, common practices, and specific challenges in QuickBooks Online.

This guide covers accounting considerations for:
- **Residential Contractors** (Custom homes, remodelers, production builders)
- **Commercial Contractors** (General contractors, tenant improvement)
- **Specialty Trade Contractors** (Electrical, plumbing, HVAC, concrete, etc.)
- **Design-Build Firms** (Combined design and construction)

---

## Residential Contractors

### Segment Overview

```
RESIDENTIAL CONTRACTOR TYPES

┌─────────────────────────────────────────────────────────────────────────────────┐
│                                                                                  │
│  CUSTOM HOME BUILDERS                                                            │
│  • One-off projects                                                              │
│  • High-touch client relationship                                                │
│  • Unique designs each time                                                      │
│  • Contract value: $300K - $5M+                                                  │
│  • Project duration: 6-18 months                                                 │
│                                                                                  │
│  PRODUCTION BUILDERS                                                             │
│  • Multiple similar homes                                                        │
│  • Tract/subdivision development                                                 │
│  • Standardized plans and specs                                                  │
│  • Contract value: $200K - $800K per unit                                        │
│  • Volume: 10-500+ homes/year                                                    │
│                                                                                  │
│  REMODELERS                                                                      │
│  • Existing structures                                                           │
│  • Additions, renovations, repairs                                               │
│  • Occupied homes during work                                                    │
│  • Contract value: $10K - $500K                                                  │
│  • Project duration: 2 weeks - 6 months                                          │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### QBO Setup for Residential

#### Chart of Accounts Customization

**Income Accounts:**
```
40000 Contract Revenue
├── 40100 Contract Revenue - Custom Homes
├── 40200 Contract Revenue - Spec Homes
├── 40300 Contract Revenue - Remodeling
├── 40400 Contract Revenue - Additions
├── 40500 Contract Revenue - Repairs/Service
└── 40600 Change Order Revenue
```

**COGS Accounts (Residential Focus):**
```
50000 Cost of Revenue
├── 51000 Labor
│   ├── 51100 Framing Labor
│   ├── 51200 Finish Carpentry
│   ├── 51300 General Labor
│   └── 51400 Supervision
│
├── 52000 Materials
│   ├── 52100 Lumber & Framing
│   ├── 52200 Roofing Materials
│   ├── 52300 Windows & Doors
│   ├── 52400 Cabinets & Countertops
│   ├── 52500 Flooring
│   ├── 52600 Paint & Finishes
│   ├── 52700 Fixtures & Hardware
│   └── 52800 Other Materials
│
├── 53000 Subcontractors
│   ├── 53100 Excavation/Site Work
│   ├── 53200 Foundation/Concrete
│   ├── 53300 Plumbing
│   ├── 53400 Electrical
│   ├── 53500 HVAC
│   ├── 53600 Insulation
│   ├── 53700 Drywall
│   ├── 53800 Tile/Stone
│   └── 53900 Landscaping
```

#### Residential-Specific Classes

```
Class Structure Option 1: By Project Type
├── Custom Homes
├── Spec Homes
├── Remodels
├── Additions
└── Service/Repairs

Class Structure Option 2: By Subdivision (Production)
├── Oakwood Phase 1
├── Oakwood Phase 2
├── Riverside Estates
└── Downtown Condos
```

### Residential Billing Practices

#### Draw Schedules (Custom Homes)

Most residential contracts use a **draw schedule** rather than progress billing:

**Typical 5-Draw Schedule:**
| Draw # | Milestone | Percentage |
|--------|-----------|------------|
| 1 | Contract signed / permits | 10% |
| 2 | Foundation complete | 15% |
| 3 | Framing & rough-in complete | 25% |
| 4 | Drywall & trim complete | 25% |
| 5 | Final completion | 25% |

**In QBO:**
1. Create the full contract as an Estimate
2. Invoice each draw by converting portion of Estimate
3. Track % complete against draw schedule

#### Spec Home Accounting

**Key Difference:** You own the inventory until sale.

**QBO Treatment:**
1. Track costs as "Construction in Progress" (Asset account)
2. When sold, transfer to Cost of Goods Sold
3. Revenue recognized at closing

```
SPEC HOME JOURNAL ENTRY - During Construction

Debit: Construction in Progress - 123 Oak St    $150,000
Credit: Accounts Payable (or Cash)                        $150,000

SPEC HOME JOURNAL ENTRY - At Sale

Debit: Cost of Goods Sold - Spec Homes          $150,000
Credit: Construction in Progress - 123 Oak St             $150,000

Debit: Cash (or Accounts Receivable)            $225,000
Credit: Sales Revenue - Spec Homes                        $225,000
```

### Residential-Specific Considerations

| Issue | Residential Approach |
|-------|---------------------|
| **Allowances** | Track allowance vs. actual for flooring, fixtures, etc. |
| **Upgrades** | Bill as change orders with customer sign-off |
| **Warranty work** | Accrue estimated warranty costs |
| **Model homes** | Capitalize costs, amortize over sales period |
| **Lot purchases** | Track land inventory separately |
| **HOA fees** | May be builder's responsibility until sale |

---

## Commercial General Contractors

### Segment Overview

```
COMMERCIAL GC TYPES

┌─────────────────────────────────────────────────────────────────────────────────┐
│                                                                                  │
│  TRADITIONAL GC (Hard Bid)                                                       │
│  • Competitive bidding                                                           │
│  • Fixed-price contracts                                                         │
│  • Design complete before bid                                                    │
│  • Lower fees, higher risk                                                       │
│                                                                                  │
│  CONSTRUCTION MANAGER (CM)                                                       │
│  • Fee-based engagement                                                          │
│  • GMP or Cost-Plus common                                                       │
│  • Involved during design                                                        │
│  • Less risk, advisory role                                                      │
│                                                                                  │
│  DESIGN-BUILD                                                                    │
│  • Single contract for design + build                                            │
│  • See separate section below                                                    │
│                                                                                  │
│  TENANT IMPROVEMENT (TI)                                                         │
│  • Interior build-outs                                                           │
│  • Fast-track schedules                                                          │
│  • Working in occupied buildings                                                 │
│  • Multiple small projects                                                       │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### QBO Setup for Commercial GCs

#### Chart of Accounts Customization

**Income Accounts:**
```
40000 Contract Revenue
├── 40100 Contract Revenue - Base Contract
├── 40200 Contract Revenue - Change Orders
├── 40300 Fee Income - CM Services
├── 40400 General Conditions Revenue
└── 40500 Other Billable Income
```

**COGS Structure (Commercial):**
```
50000 Cost of Revenue
├── 51000 Self-Performed Labor
│   ├── 51100 Supervision
│   ├── 51200 Carpentry
│   └── 51300 General Labor
│
├── 52000 General Conditions
│   ├── 52100 Project Management Salaries
│   ├── 52200 Field Office Expense
│   ├── 52300 Temporary Facilities
│   ├── 52400 Equipment & Tools
│   ├── 52500 Safety & Security
│   └── 52600 Clean-up
│
├── 53000 Subcontractors (by CSI Division)
│   ├── 53100 Div 03 - Concrete
│   ├── 53200 Div 04 - Masonry
│   ├── 53300 Div 05 - Metals
│   ├── 53400 Div 06 - Wood/Plastics
│   ├── 53500 Div 07 - Thermal/Moisture
│   ├── 53600 Div 08 - Doors/Windows
│   ├── 53700 Div 09 - Finishes
│   ├── 53800 Div 10-14 - Specialties/Conveying
│   ├── 53900 Div 15 - Mechanical
│   └── 54000 Div 16 - Electrical
│
└── 55000 Other Direct Costs
    ├── 55100 Permits & Fees
    ├── 55200 Testing & Inspections
    └── 55300 Insurance (Project-specific)
```

### Commercial-Specific Features

#### General Conditions Tracking

**What Are General Conditions?**
Project overhead that doesn't go into the building:
- Project manager/superintendent salaries
- Job site trailer, utilities
- Temporary facilities (fencing, power, water)
- Safety equipment and programs
- Cleanup and debris removal

**QBO Tracking:**
1. Create "General Conditions" class or use Products/Services
2. Track budget vs. actual separately
3. Bill as line item or include in contract

#### Subcontractor-Heavy Operations

Commercial GCs often subcontract 80-95% of work.

**QBO Subcontractor Management:**
```
For each major subcontract:
□ Original subcontract value
□ Approved sub change orders
□ Revised subcontract value
□ Billed to date (their pay apps)
□ Retention held
□ Remaining to bill
□ Insurance certificate current
□ Lien waivers on file
```

#### AIA Billing Requirements

Commercial projects typically require AIA forms:
- **G702** - Application and Certificate for Payment
- **G703** - Continuation Sheet (Schedule of Values)

See [AIA Forms Companion Guide](./03-aia-forms-companion.md) for detailed instructions.

### Commercial-Specific Considerations

| Issue | Commercial Approach |
|-------|---------------------|
| **Retainage** | Typically 10% until 50%, then 5% |
| **Liquidated damages** | Track schedule; may be liability |
| **Payment bond claims** | Respond to sub/supplier claims |
| **Certified payroll** | Government/public work requirements |
| **OCIP/CCIP** | Owner/Contractor-controlled insurance |
| **Schedule of Values** | Detailed SOV for billing |
| **Substantial completion** | Triggers warranty, retention release |

---

## Specialty Trade Contractors

### Segment Overview

```
SPECIALTY TRADE CATEGORIES

┌─────────────────────────────────────────────────────────────────────────────────┐
│                                                                                  │
│  MEP TRADES (Mechanical, Electrical, Plumbing)                                   │
│  • High material cost (30-50%)                                                   │
│  • Licensed/regulated work                                                       │
│  • Often union labor                                                             │
│  • Fabrication/prefab opportunity                                                │
│                                                                                  │
│  STRUCTURAL TRADES (Concrete, Steel, Masonry)                                    │
│  • Equipment-intensive                                                           │
│  • Material-heavy (concrete, rebar, block)                                       │
│  • Weather-dependent                                                             │
│  • Early in project sequence                                                     │
│                                                                                  │
│  FINISHING TRADES (Drywall, Paint, Flooring, Tile)                               │
│  • Labor-intensive                                                               │
│  • Late in project sequence                                                      │
│  • Punch list exposure                                                           │
│  • Multiple small areas                                                          │
│                                                                                  │
│  SITE TRADES (Excavation, Utilities, Paving, Landscape)                          │
│  • Equipment-intensive                                                           │
│  • Weather-dependent                                                             │
│  • Often unit-price contracts                                                    │
│  • Early in project sequence                                                     │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### QBO Setup for Specialty Trades

#### Electrical Contractor Example

**Income Accounts:**
```
40000 Contract Revenue
├── 40100 Commercial Electrical
├── 40200 Residential Electrical
├── 40300 Service & Repair
├── 40400 Fire Alarm/Low Voltage
└── 40500 Change Orders
```

**COGS Accounts:**
```
50000 Cost of Revenue
├── 51000 Labor
│   ├── 51100 Electrician - Journeyman
│   ├── 51200 Electrician - Apprentice
│   ├── 51300 Foreman
│   └── 51400 Estimator/PM (if direct)
│
├── 52000 Materials
│   ├── 52100 Wire & Cable
│   ├── 52200 Conduit & Fittings
│   ├── 52300 Boxes & Covers
│   ├── 52400 Switchgear
│   ├── 52500 Panels & Breakers
│   ├── 52600 Fixtures & Devices
│   ├── 52700 Fire Alarm Equipment
│   └── 52800 Other Electrical Materials
│
├── 53000 Subcontractors
│   ├── 53100 Fire Alarm Sub
│   ├── 53200 Low Voltage Sub
│   └── 53300 Other Electrical Subs
│
└── 54000 Equipment & Tools
    ├── 54100 Lift Rental
    ├── 54200 Tool Expense
    └── 54300 Equipment Charges
```

#### Plumbing Contractor Example

**COGS Accounts:**
```
50000 Cost of Revenue
├── 51000 Labor
│   ├── 51100 Plumber - Journeyman
│   ├── 51200 Plumber - Apprentice
│   ├── 51300 Pipefitter
│   └── 51400 Foreman
│
├── 52000 Materials
│   ├── 52100 Pipe - Copper
│   ├── 52200 Pipe - PVC/ABS
│   ├── 52300 Pipe - Cast Iron
│   ├── 52400 Fittings
│   ├── 52500 Valves
│   ├── 52600 Fixtures
│   ├── 52700 Water Heaters
│   └── 52800 Other Plumbing Materials
│
└── 53000 Equipment
    ├── 53100 Trencher Rental
    ├── 53200 Threading Equipment
    └── 53300 Testing Equipment
```

### Specialty Trade Considerations

#### Prefabrication Accounting

Many trades prefabricate in-shop:

**QBO Treatment:**
1. Track shop labor separately from field labor
2. Material issued to job when fabricated (not when installed)
3. Consider WIP for large fabrication backlogs

```
PREFAB FLOW

Shop Labor (51500)  ──┐
                      ├──► Fabricated Assembly ──► Job Cost
Shop Materials (52900)──┘
```

#### Tool & Equipment Intensive Trades

Trades like concrete, excavation, steel erection have significant equipment:

**Tracking Options:**
1. **Owned equipment charges** - Allocate to jobs at internal rate
2. **Rental equipment** - Track by job directly
3. **Small tools** - Expense or allocate pool

#### Union Labor Considerations

Many specialty trades are union:

**QBO Setup:**
- Track union dues/assessments
- Separate fringe benefit rates
- Multiple pay classifications
- Certified payroll requirements
- Training fund contributions

### Trade-Specific Metrics

| Trade | Key Metrics |
|-------|-------------|
| **Electrical** | $ per device, labor hours per outlet |
| **Plumbing** | $ per fixture, labor hours per rough-in |
| **HVAC** | $ per ton, labor hours per system |
| **Concrete** | $ per CY, CY per man-day |
| **Drywall** | $ per SF, SF per man-day |
| **Painting** | $ per SF, SF per gallon |
| **Roofing** | $ per square (100 SF) |
| **Flooring** | $ per SF/SY by material type |

---

## Design-Build Firms

### Segment Overview

```
DESIGN-BUILD STRUCTURE

┌─────────────────────────────────────────────────────────────────────────────────┐
│                                                                                  │
│                          SINGLE CONTRACT                                         │
│                              │                                                   │
│              ┌───────────────┴───────────────┐                                   │
│              │                               │                                   │
│         DESIGN PHASE                   BUILD PHASE                               │
│     ┌───────────────┐              ┌───────────────┐                             │
│     │ Architecture  │              │ Construction  │                             │
│     │ Engineering   │              │ Management    │                             │
│     │ Permitting    │              │ Subcontractors│                             │
│     └───────────────┘              │ Materials     │                             │
│                                    └───────────────┘                             │
│                                                                                  │
│  Revenue Recognition Challenge:                                                  │
│  • Design fees earned differently than construction                              │
│  • May have percentage fee on construction                                       │
│  • Need to track both components                                                 │
│                                                                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

### QBO Setup for Design-Build

#### Separate Income Streams

```
40000 Revenue
├── 41000 Design Services
│   ├── 41100 Architectural Design
│   ├── 41200 Engineering Design
│   ├── 41300 Permitting Services
│   └── 41400 Owner's Rep Services
│
├── 42000 Construction Revenue
│   ├── 42100 Base Contract - Construction
│   ├── 42200 Change Order Revenue
│   └── 42300 General Conditions Revenue
│
└── 43000 Design-Build Fee
    └── 43100 Management Fee
```

#### Cost Structure

```
50000 Cost of Revenue
├── 51000 Design Costs
│   ├── 51100 In-House Architects
│   ├── 51200 In-House Engineers
│   ├── 51300 Consultant - Structural
│   ├── 51400 Consultant - MEP
│   ├── 51500 Consultant - Civil
│   └── 51600 Other Design Consultants
│
├── 52000 Construction Costs
│   ├── [Standard construction COGS]
│
└── 53000 Reimbursable Expenses
    ├── 53100 Printing/Plotting
    ├── 53200 Travel
    └── 53300 Permits/Fees
```

### Design-Build Revenue Recognition

**Challenge:** Two types of revenue in one contract

**Approach 1: Separate Performance Obligations**
- Recognize design fees as design work completes
- Recognize construction revenue using POC
- May require separate WIP tracking

**Approach 2: Combined POC**
- Treat entire project as single performance obligation
- Use total contract cost for % complete
- Include design costs in estimate

### Design-Build Specific Issues

| Issue | Design-Build Approach |
|-------|----------------------|
| **Design liability** | Professional liability insurance needed |
| **GMP with design** | Must manage design to hit GMP |
| **Design contingency** | Budget for design unknowns |
| **Owner changes** | Who absorbs re-design cost? |
| **Consultant management** | Track sub-consultant costs |
| **Phase overlap** | Design continues during construction |

---

## Multi-Segment Contractors

### When You Do Multiple Types

Many contractors work across segments:

**Example: Full-Service Contractor**
- Residential custom homes
- Residential remodeling
- Light commercial
- Property management/maintenance

### QBO Structure for Multi-Segment

**Use Classes for Segments:**
```
Classes:
├── Residential - Custom
├── Residential - Remodel
├── Commercial - New
├── Commercial - TI
└── Service/Maintenance
```

**Use Customers/Projects for Jobs:**
```
Each job is a Customer or Project, classified into the appropriate segment.
```

### Multi-Segment Reporting

**Key Reports:**
1. **P&L by Class** - Profitability by segment
2. **P&L by Customer** - Profitability by job
3. **Revenue by Class** - Segment mix
4. **Overhead Allocation** - Fair share to each segment

---

## Industry-Specific Compliance

### Licensing Requirements by Trade

| Trade/Type | Typical License Requirements |
|------------|------------------------------|
| **General Contractor** | State contractor license, liability insurance |
| **Electrical** | State/local electrical license, master electrician |
| **Plumbing** | State/local plumbing license, master plumber |
| **HVAC** | HVAC license, EPA refrigerant certification |
| **Roofing** | Roofing contractor license in many states |
| **Residential** | Home builder license, warranty programs |
| **Fire Protection** | Fire suppression contractor license |

### Insurance Variations by Segment

| Segment | Special Insurance Needs |
|---------|------------------------|
| **Residential** | Completed operations, builder's risk |
| **Commercial** | Higher GL limits, professional liability (D-B) |
| **MEP Trades** | Professional liability for design |
| **Excavation** | Pollution liability |
| **Roofing** | Higher WC rates, completed operations |
| **Design-Build** | Professional liability (E&O) |

---

## Key Takeaways by Segment

### Residential
- Draw schedules, not AIA billing
- Track allowances and upgrades
- Spec home = inventory accounting
- Warranty accrual important

### Commercial
- AIA billing required
- Subcontractor-heavy (manage compliance)
- General conditions tracking
- Schedule of Values critical

### Specialty Trades
- Detailed material tracking
- Labor productivity metrics
- Equipment/tool intensity varies
- Union considerations

### Design-Build
- Dual revenue streams
- Professional liability exposure
- Design contingency management
- Consultant cost tracking

---

## Next Steps

- For AIA billing → [AIA Forms Companion](./03-aia-forms-companion.md)
- For subcontractor management → [Subcontractor Management](../workflows/02-subcontractor-1099-lien-waivers.md)
- For job costing setup → [Job Costing Setup](../tutorials/03-job-costing-setup.md)
- For contract types → [Contract Types Deep Dive](../tutorials/09-contract-types.md)

---

*[← Previous: Multi-Entity Structures](./01-multi-entity-structures.md) | [Next: AIA Forms Companion →](./03-aia-forms-companion.md)*
