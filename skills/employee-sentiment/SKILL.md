---
name: employee-sentiment
description: Tracks employee satisfaction through pulse surveys, 1:1 notes, and engagement signals
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: hr-operations
---

# Employee Sentiment Tracking

## Instructions

Monitor and analyze employee satisfaction across the organization.

### Data Sources
1. **Pulse Surveys** — Bi-weekly 3-question surveys (anonymous)
2. **1:1 Meeting Notes** — Manager-submitted themes (no names)
3. **Engagement Signals** — Participation rates, voluntary feedback
4. **Exit Interview Data** — Themes from departing employees

### Pulse Survey Questions (Rotating)
Core (every survey):
- "How satisfied are you at work this week?" (1-10)

Rotating (pick 2):
- "Do you feel recognized for your contributions?"
- "Is your workload manageable?"
- "Do you have the tools you need?"
- "Do you see a growth path here?"
- "How well does your team collaborate?"
- "How supported do you feel by your manager?"

### Sentiment Scoring
- **9-10**: Highly engaged — acknowledge and maintain
- **7-8**: Engaged — monitor for trends
- **5-6**: Neutral — investigate with follow-up questions
- **3-4**: Disengaged — flag to manager for 1:1 conversation
- **1-2**: At risk — immediate escalation to HR leadership

### Reporting
Monthly sentiment report:
```
Overall Score: X.X / 10 (trend: ↑↓→)
Response Rate: X%
Department Breakdown:
  Engineering: X.X
  Sales: X.X
  Operations: X.X
Top Concern: [Theme]
Bright Spot: [Theme]
Action Items: [1-2 specific recommendations]
```

### Privacy
- Individual responses are NEVER attributed to specific employees
- Minimum team size for department breakdown: 5 people
- Raw data accessible only to HR leadership
- Managers receive aggregate team scores only
