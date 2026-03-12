# Workflow: Quarterly Review Cycle

## Overview
End-to-end quarterly performance and sentiment review cycle.

## Timeline (Runs Q1/Q2/Q3/Q4)

```
┌─────────────────────────────────────────────────────────┐
│ WEEK 1: DATA COLLECTION                                 │
│                                                         │
│ Actions:                                                │
│ ├── Deploy pulse survey to all employees                 │
│ ├── Send self-assessment forms to employees              │
│ ├── Send manager review forms                            │
│ ├── Pull performance data (project completion, metrics)  │
│ └── Pull sentiment trends from prior surveys             │
│                                                         │
│ Tools: survey-engine, hris-integration                  │
│ Agent: performance-tracking                             │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ WEEK 2: ANALYSIS                                        │
│                                                         │
│ Actions:                                                │
│ ├── Aggregate survey responses (anonymous)               │
│ ├── Calculate department sentiment scores                │
│ ├── Identify retention risks (score <5 + performance ok) │
│ ├── Run skills gap analysis per department               │
│ ├── Compare to prior quarter baselines                   │
│ └── Flag any sentiment drops >1.0 point                  │
│                                                         │
│ Skills: employee-sentiment, skills-gap-analysis          │
│ Hooks: on-sentiment-drop                                │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ WEEK 3: REVIEWS                                         │
│                                                         │
│ Actions:                                                │
│ ├── Managers conduct 1:1 review meetings                 │
│ ├── Agent provides talking points per employee           │
│ ├── Document outcomes and development goals              │
│ ├── Identify promotion candidates                        │
│ └── Identify PIP candidates (with HR review)             │
│                                                         │
│ Tools: slack-notifier (reminders), hris-integration      │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ WEEK 4: REPORTING & ACTION                              │
│                                                         │
│ Actions:                                                │
│ ├── Generate department health reports                   │
│ ├── Generate C-suite executive summary                   │
│ ├── Workforce planning update (attrition forecast)       │
│ ├── Training recommendations from skills gaps            │
│ ├── Compensation review triggers (merit cycle prep)      │
│ └── Update hiring plan based on retention risks          │
│                                                         │
│ Skills: workforce-planning, compliance-reporting         │
│ Agent: csuite-reporting                                 │
│ Tools: analytics-dashboard, lms-integration             │
└─────────────────────────────────────────────────────────┘
```

## Key Metrics Tracked
- Employee NPS (eNPS)
- Department sentiment scores (1-10)
- Review completion rate (target: 100%)
- Retention risk count by department
- Promotion rate vs. target
- Skills gap closure rate
