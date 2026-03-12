---
name: stack-ranking
description: High-volume candidate stack-ranking against job descriptions with weighted match scoring
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Stack Ranking

## Instructions

Score and rank candidates against a job description using weighted criteria.

### Scoring Categories (100-point scale)

| Category | Weight | What to Evaluate |
|----------|--------|-----------------|
| Technical Skills | 35% | Required skills match, years of experience with each |
| Experience Level | 25% | Total YOE, relevant industry experience, role seniority match |
| Education | 15% | Degree requirements, relevant certifications |
| Culture Signals | 15% | Company size fit, industry alignment, growth trajectory |
| Bonus Factors | 10% | Location match, immediate availability, referral source |

### Process

1. Parse the job description into required vs. preferred qualifications
2. Extract hiring manager notes for additional weight adjustments
3. For each candidate:
   - Extract skills, experience, education from resume
   - Score each category against job requirements
   - Calculate weighted total
   - Flag any disqualifiers (missing hard requirements)
4. Sort by total score descending
5. Output as ranked table with score breakdowns

### Output Format

```
Rank | Name | Total Score | Skills (35) | Exp (25) | Edu (15) | Culture (15) | Bonus (10) | Flags
1    | Jane | 87          | 32          | 22       | 14       | 12           | 7          | -
2    | John | 74          | 28          | 20       | 10       | 10           | 6          | Missing cert
```

### Escalation Rules
- Score below 40: Auto-archive (log reason)
- Score 40-60: Flag for human review
- Score 60+: Advance to pre-screening
- Any disqualifier flag: Human review regardless of score
