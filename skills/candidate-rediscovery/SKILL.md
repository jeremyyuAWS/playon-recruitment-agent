---
name: candidate-rediscovery
description: Re-surfaces past applicants who scored well but weren't hired when matching new roles open
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Candidate Rediscovery

## Instructions

Mine the existing ATS database for past candidates who match newly opened roles.

### Why This Matters
- PlayOn receives 2,500+ applications per role — many strong candidates aren't selected
- Re-engaging past applicants is 3-5x cheaper than sourcing new ones
- Candidates who previously applied already know and are interested in PlayOn

### Trigger
- New requisition approved → auto-run rediscovery before external posting
- Run after internal mobility check, before external sourcing

### Matching Criteria

1. **Previous match score**: Originally scored 60+ on a similar role
2. **Recency**: Applied within last 18 months (beyond that, skills may be stale)
3. **Disposition reason**: Not hired due to timing/headcount/close competition — NOT performance concerns
4. **Role similarity**: >70% overlap in required skills between old and new role
5. **Availability signal**: Not currently employed at PlayOn (check HRIS)

### Process

1. Pull all candidates from Lever who:
   - Applied in last 18 months
   - Scored 60+ on any role
   - Were not hired
   - Disposition ≠ "poor performance" or "culture concern"
2. Re-score against the new job description
3. Rank and present top 20
4. For top candidates, check:
   - Are they still in the talent CRM? Last engagement?
   - LinkedIn: have they changed roles since? (don't poach from current employer publicly)
5. Generate personalized re-engagement message referencing their previous application

### Output

```
## Rediscovery Report — [New Role Title]

Candidates found in ATS: [N]
Qualified matches: [N]

Rank | Name | Previous Role Applied | Previous Score | New Score | Last Contact | Status
1    | [Name] | [Role] | 78 | 82 | [Date] | [Available/Employed/Unknown]

## Recommended Outreach
[Candidate 1]: [Personalized message draft]
[Candidate 2]: [Personalized message draft]
```

### Re-engagement Message Template
```
Subject: A new opportunity at PlayOn Sports

Hi [Name],

You applied for our [Previous Role] position [X months ago], and we were
impressed by your [specific strength from previous evaluation].

We've just opened a [New Role] that aligns well with your background in
[relevant skill]. I'd love to reconnect — would you be open to a quick chat?

[Recruiter Name]
```

### Rules
- Respect candidate opt-outs — check do-not-contact list before outreach
- Don't re-engage candidates who explicitly declined offers (different from not selected)
- Maximum 2 re-engagement attempts per candidate per year
- Always reference their previous application — shows you valued their time
- Track rediscovery-to-hire conversion rate as a sourcing KPI
