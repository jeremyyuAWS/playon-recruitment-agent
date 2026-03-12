---
name: workforce-planning
description: Headcount forecasting based on attrition trends, growth plans, budget, and hiring velocity
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: hr-operations
---

# Workforce Planning

## Instructions

Provide data-driven headcount forecasting and workforce strategy recommendations.

### Data Inputs
- Current headcount by department and level
- Historical attrition rates (voluntary + involuntary) by department
- Approved hiring plan and budget
- Current pipeline health (open reqs, candidates in process)
- Revenue growth targets and business expansion plans
- Average time-to-fill by role type
- Seasonal hiring patterns

### Forecasting Models

#### Attrition Forecast
```
Next Quarter Projected Departures = Current Headcount × Historical Quarterly Attrition Rate
Adjust for: seasonal patterns, sentiment scores, industry benchmarks
```

#### Hiring Velocity Forecast
```
Expected Hires = Open Reqs × (1 / Avg Time-to-Fill) × Remaining Days in Quarter
Adjust for: recruiter capacity, pipeline conversion rates, seasonal slowdowns
```

#### Net Headcount Projection
```
Q+1 Headcount = Current + Expected Hires - Projected Departures
Gap = Target Headcount - Projected Headcount
```

### Output Format

```
## Workforce Planning Report — [Quarter/Year]

### Current State
Total headcount: [N]
Open requisitions: [N]
Attrition (trailing 12mo): [X]%

### Projections
| Department | Current | Target | Projected Hires | Projected Attrition | Net | Gap |
|------------|---------|--------|-----------------|---------------------|-----|-----|
| Engineering | 45 | 55 | 8 | 3 | 50 | -5 |
| ...

### Risks
- [Department] attrition trending above forecast
- [Role type] time-to-fill exceeding target — pipeline insufficient

### Recommendations
1. [Specific action with expected impact]
2. [Specific action with expected impact]
```

### Rules
- Update forecasts monthly — stale plans are worse than no plan
- Flag departments where attrition > 2x company average
- Include recruiter capacity in hiring projections (3 recruiters × ~5 hires/month)
- Never present projections without confidence intervals
- Distinguish voluntary vs. involuntary attrition — they have different drivers
