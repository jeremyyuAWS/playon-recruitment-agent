# Workflow: Annual Compensation Review Cycle

## Overview
Annual merit increase, equity refresh, and promotion compensation cycle. Runs January-March each year.

## Steps

```
┌─────────────────────────────────────────────────────────┐
│ 1. DATA GATHERING (January, Weeks 1-2)                  │
│                                                         │
│ Actions:                                                │
│ ├── Pull market compensation data (Radford, Levels.fyi) │
│ ├── Update internal compensation bands                   │
│ ├── Pull performance review ratings (from Q4 cycle)      │
│ ├── Calculate current pay vs. band position per employee │
│ ├── Identify below-market employees (below 25th pctl)    │
│ ├── Calculate total merit budget per department           │
│ └── Identify promotion candidates (from Q4 reviews)      │
│                                                         │
│ Skills: compensation-benchmarking, workforce-planning    │
│ Tools: hris-integration, analytics-dashboard             │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 2. MANAGER RECOMMENDATIONS (January, Weeks 3-4)         │
│                                                         │
│ Actions:                                                │
│ ├── Distribute merit budget to managers with guidelines   │
│ ├── Managers submit recommended increases per employee    │
│ ├── Managers submit promotion nominations with justification│
│ ├── System validates: within budget, within band, equity  │
│ ├── Flag outliers: >15% increase, below minimum, compression│
│ └── Deadline: end of January                             │
│                                                         │
│ Guidelines for managers:                                │
│ ├── Exceeds expectations: 5-8% merit                     │
│ ├── Meets expectations: 3-5% merit                       │
│ ├── Below expectations: 0% (address via PIP instead)     │
│ ├── Market adjustment: additional 0-5% if below band     │
│ └── Promotion: move to 50th percentile of new band       │
│                                                         │
│ Tools: hris-integration, slack-notifier                  │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 3. CALIBRATION (February, Weeks 1-2)                    │
│                                                         │
│ Actions:                                                │
│ ├── HR reviews all recommendations for consistency       │
│ ├── Cross-department calibration sessions                │
│ ├── Pay equity analysis (gender, ethnicity, tenure)      │
│ ├── Compression check (new hires vs. tenured employees)  │
│ ├── Total budget reconciliation with finance              │
│ └── Final recommendations to leadership for approval     │
│                                                         │
│ Skills: compliance-reporting (pay equity)                │
│ Tools: analytics-dashboard, slack-notifier               │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 4. EXECUTIVE APPROVAL (February, Weeks 3-4)             │
│                                                         │
│ Actions:                                                │
│ ├── Present total comp plan to CEO/CFO                   │
│ ├── Highlight: total cost, avg increase %, promotions    │
│ ├── Address any budget exceptions or equity issues        │
│ ├── Get final sign-off                                   │
│ └── If rejected: return to calibration with constraints   │
│                                                         │
│ Agent: csuite-reporting                                 │
│ Tools: analytics-dashboard                              │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 5. COMMUNICATION (March, Weeks 1-2)                     │
│                                                         │
│ Actions:                                                │
│ ├── Manager talking points generated per employee        │
│ ├── Managers communicate changes in 1:1s                 │
│ ├── Updated offer letters / comp confirmations via DocuSign│
│ ├── HRIS and payroll updated with effective date          │
│ ├── Promotion announcements (if employee consents)       │
│ └── Employees who received 0% increase: ensure PIP exists │
│                                                         │
│ Tools: docusign-integration, payroll-connector,          │
│        hris-integration, slack-notifier                  │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 6. EFFECTIVE DATE & TRACKING (April 1)                  │
│                                                         │
│ Actions:                                                │
│ ├── New compensation reflected in April payroll           │
│ ├── Updated compensation bands published internally      │
│ ├── Retro pay processed if delayed                       │
│ ├── Track attrition in 60 days post-cycle                │
│ ├── Flag employees who leave within 90 days (comp-related?)│
│ └── Update cost-per-employee metrics                     │
│                                                         │
│ Tools: payroll-connector, analytics-dashboard            │
│ Hooks: on-sentiment-drop (watch post-cycle sentiment)    │
└─────────────────────────────────────────────────────────┘
```

## Key Metrics
| Metric | Target |
|--------|--------|
| Average merit increase | 4-5% |
| Promotion rate | 10-15% of eligible employees |
| Pay equity gap (gender) | <2% |
| Budget utilization | 95-100% |
| Post-cycle voluntary attrition (90 days) | <3% |
| Manager communication completion | 100% by March 15 |
