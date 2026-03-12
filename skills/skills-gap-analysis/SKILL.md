---
name: skills-gap-analysis
description: Compares team capabilities vs. needs to inform hiring, training, or restructuring decisions
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: hr-operations
---

# Skills Gap Analysis

## Instructions

Identify gaps between current team capabilities and future needs to inform talent strategy.

### Process

1. **Map current skills** — Pull from HRIS profiles, project history, certifications, self-assessments
2. **Define required skills** — From business strategy, tech roadmap, and department heads
3. **Score proficiency** — Rate each skill per person: None (0), Basic (1), Intermediate (2), Advanced (3), Expert (4)
4. **Identify gaps** — Where required proficiency exceeds current team capability
5. **Recommend action** — Hire, train, restructure, or outsource

### Gap Categories

| Gap Size | Definition | Recommended Action |
|----------|-----------|-------------------|
| Critical (0-1 vs. 3-4 needed) | No one on team can do this | Hire immediately or contract |
| Moderate (1-2 vs. 3-4 needed) | Basic capability, not expert | Train existing + hire 1 specialist |
| Minor (2-3 vs. 3-4 needed) | Competent, need mastery | Professional development plan |
| Surplus (team exceeds need) | Over-staffed in this area | Redeploy or expand scope |

### Output Format

```
## Skills Gap Analysis — [Department/Team]
Date: [Date]
Team Size: [N]

### Critical Gaps (Immediate Action Required)
| Skill | Required Level | Current Best | Gap | Action |
|-------|---------------|-------------|-----|--------|
| [Skill] | Expert (4) | None (0) | -4 | Hire |

### Moderate Gaps (Next Quarter)
...

### Minor Gaps (Development Plan)
...

### Strengths (No Action Needed)
| Skill | Required Level | Current Best | Surplus |
|-------|---------------|-------------|---------|

### Recommendations
1. [Hire X role to close critical gap in Y]
2. [Enroll Z team members in W training]
3. [Restructure A team to leverage B surplus]

### Budget Impact
- Hiring cost: $[X] (critical gaps)
- Training cost: $[Y] (moderate + minor gaps)
- Timeline: [Months to close all gaps]
```

### Rules
- Refresh analysis quarterly or when strategy shifts
- Include both technical and soft skills
- Self-assessments are input, not gospel — validate with manager ratings and project outcomes
- Skills taxonomy must be consistent across departments for comparison
- Never use gap analysis to justify terminations — it's a planning tool, not a PIP tool
