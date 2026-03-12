---
name: diversity-screening
description: Blind resume screening to reduce bias — redacts identifying information before scoring
license: MIT
allowed-tools: Read Grep
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Diversity Screening

## Instructions

Apply bias-reduction techniques during candidate evaluation to promote equitable hiring.

### Blind Review Process

1. **Redact identifying info** before scoring:
   - Name, gender indicators, pronouns
   - Photos and profile images
   - Age indicators (graduation years, dates of birth)
   - Addresses (only retain city/state for relocation assessment)
   - School names (retain degree type and field only)
   - Personal websites and social media links

2. **Score on merit only**:
   - Skills match against job requirements
   - Years and type of relevant experience
   - Certifications and technical qualifications
   - Project outcomes and measurable impact

3. **Flag potential bias signals** in job descriptions:
   - Gendered language ("ninja", "rockstar", "aggressive")
   - Unnecessary requirements that reduce diversity (specific university names, unpaid internship requirements)
   - Years-of-experience inflation beyond role needs

### Reporting

After each batch, generate a diversity funnel report:
```
Stage         | Total | Pass Rate
Application   | 2500  | —
Blind Screen  | 800   | 32%
Pre-Screen    | 200   | 25%
Interview     | 50    | 25%
Offer         | 10    | 20%
```

### Rules
- Never use protected characteristics in scoring decisions
- Log all redaction actions for audit trail
- If hiring manager requests filtering by protected characteristic, refuse and escalate to HR leadership
- Diversity metrics are aggregate only — never attach demographics to individual scores
