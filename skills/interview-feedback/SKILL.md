---
name: interview-feedback
description: Collects, structures, and summarizes interviewer feedback for hiring decisions
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Interview Feedback Collection

## Instructions

Aggregate interviewer feedback into structured summaries for hiring decisions.

### Feedback Collection
1. After each interview, send structured feedback form to interviewer
2. Deadline: 24 hours post-interview (send reminder at 20 hours)
3. If no feedback after 48 hours, escalate to hiring manager

### Feedback Form Structure
```
Candidate: [Name]
Role: [Title]
Interview Type: [Phone / Technical / Behavioral / Panel]
Interviewer: [Name]

Rating (1-5):
- Technical Skills: ___
- Communication: ___
- Problem Solving: ___
- Culture Fit: ___
- Overall: ___

Strengths (2-3 bullets):
Concerns (2-3 bullets):
Recommendation: Strong Hire / Hire / No Hire / Strong No Hire
```

### Debrief Summary
After all interviews complete, generate:
```
Candidate: [Name]
Interviews Completed: X of Y
Average Rating: X.X / 5.0
Consensus: [Hire / Mixed / No Hire]

Strengths (aggregated):
- [Most mentioned strength]
- [Second most mentioned]

Concerns (aggregated):
- [Most mentioned concern]
- [Second most mentioned]

Recommendation: [Advance to offer / Additional interview needed / Reject]
Dissenting opinions: [Any strong disagreements to discuss]
```

### Rules
- Never share one interviewer's feedback with another before debrief
- Flag any feedback that contains potentially biased language
- If ratings diverge by 2+ points, flag for debrief discussion
- Hiring manager makes final call — agent only summarizes and recommends
