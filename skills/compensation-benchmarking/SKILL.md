---
name: compensation-benchmarking
description: Validates candidate compensation expectations against market data and internal pay bands
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Compensation Benchmarking

## Instructions

Compare candidate compensation expectations against role budgets and market rates.

### Data Sources
- Internal pay bands from HR (by role level and location)
- Market data from compensation surveys (Radford, Levels.fyi, Glassdoor)
- Historical offer data from Lever (accepted vs. declined offers)

### Process

1. Extract candidate's stated compensation expectation from pre-screening
2. Look up role's approved compensation range (base, bonus, equity)
3. Compare against market data for role + location + experience level
4. Calculate:
   - **Budget fit**: % within approved range
   - **Market alignment**: percentile vs. market (25th, 50th, 75th)
   - **Offer competitiveness score**: likelihood of acceptance based on historical data

### Output

```
Candidate: [Name]
Expectation: $X base + $Y bonus
Role Range: $A - $B base
Market 50th: $M
Budget Fit: Within range / Over by X% / Under by X%
Market Percentile: Xth
Offer Competitiveness: High / Medium / Low
Recommendation: Proceed / Negotiate / Flag for budget approval
```

### Escalation
- Expectation exceeds range by >15%: Flag for hiring manager + HR approval
- Expectation below 75th percentile of market: Proceed but note potential flight risk
- No compensation data available for role: Request HR to set range before proceeding
