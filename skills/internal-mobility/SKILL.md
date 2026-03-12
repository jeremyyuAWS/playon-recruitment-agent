---
name: internal-mobility
description: Matches existing employees to open roles before external posting — reduces cost-per-hire and improves retention
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Internal Mobility

## Instructions

Before posting a role externally, search the internal talent pool for qualified employees.

### Process

1. **New requisition approved** → trigger internal mobility check
2. **Scan HRIS** for employees matching:
   - Skills overlap (>60% of required skills)
   - Tenure >12 months in current role
   - Performance rating: meets or exceeds expectations
   - Career interest alignment (from development plans or 1:1 notes)
   - Manager approval for lateral/upward moves
3. **Generate internal candidate shortlist** with match scores
4. **Internal posting window**: 5 business days before external posting
5. **Internal applicants** go through streamlined interview (1 round vs. full loop)

### Match Scoring (Internal)

| Category | Weight | Source |
|----------|--------|--------|
| Skills match | 30% | HRIS skills profile + project history |
| Performance | 25% | Last 2 review cycles |
| Tenure readiness | 20% | Time in current role (>12mo = ready) |
| Career alignment | 15% | Development plan, stated interests |
| Manager endorsement | 10% | Current manager feedback |

### Output

```
Internal Mobility Report — [Role Title]

Internal candidates found: [N]

Rank | Name | Department | Current Role | Score | Key Strength | Gap
1    | [Name] | [Dept] | [Title] | 85 | [Strength] | [Gap if any]
2    | ...

Recommendation:
- [Advance to internal interview / Post externally / Both]
```

### Rules
- Never bypass internal posting window unless role is confidential (executive search)
- Internal candidates must still meet minimum qualifications
- Current manager must be notified if their report applies (no secret applications)
- Track internal fill rate as a KPI (target: >20% of hires)
- If internal candidate is close but has skill gap, recommend training path instead of rejection
