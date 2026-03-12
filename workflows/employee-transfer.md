# Workflow: Internal Employee Transfer

## Overview
When an employee moves to a new role via internal mobility — handles current team handoff, new team onboarding, compensation adjustment, and system updates.

## Steps

```
┌─────────────────────────────────────────────────────────┐
│ 1. TRANSFER APPROVAL (3-5 days)                         │
│                                                         │
│ Parties: Current manager, new hiring manager, HR, employee │
│ Actions:                                                │
│ ├── Employee applies to internal posting                 │
│ ├── Internal interview (streamlined, 1 round)            │
│ ├── New hiring manager makes offer                       │
│ ├── Current manager notified and agrees to timeline      │
│ ├── HR reviews comp adjustment (if any)                  │
│ ├── Finance approves budget transfer                     │
│ └── Employee accepts                                     │
│                                                         │
│ Tools: lever-ats, slack-notifier, hris-integration       │
│ Gate: All 3 parties must agree (employee, old mgr, new mgr) │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 2. TRANSITION PLANNING (1 week)                         │
│                                                         │
│ Actions:                                                │
│ ├── Current manager creates knowledge transfer plan      │
│ ├── Identify successor or redistribute responsibilities  │
│ ├── Set transition date (typically 2-4 weeks out)        │
│ ├── Document all ongoing projects, ownership, and context│
│ ├── Introduce replacement or interim coverage            │
│ └── Notify stakeholders of upcoming change               │
│                                                         │
│ Tools: slack-notifier                                   │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 3. KNOWLEDGE TRANSFER (2-3 weeks)                       │
│                                                         │
│ Actions:                                                │
│ ├── Handoff meetings (projects, processes, relationships)│
│ ├── Documentation updates (runbooks, wikis, ownership)   │
│ ├── Shadow sessions for successor                        │
│ ├── Gradual responsibility transfer                      │
│ └── Final handoff sign-off from current manager          │
│                                                         │
│ Checklist:                                              │
│ ├── [ ] All projects reassigned                          │
│ ├── [ ] Documentation updated                            │
│ ├── [ ] Recurring meetings transferred                   │
│ ├── [ ] Key contacts introduced to successor             │
│ └── [ ] Manager sign-off on complete handoff             │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 4. TRANSITION DAY                                       │
│                                                         │
│ Actions:                                                │
│ ├── Update HRIS: new title, department, manager, comp    │
│ ├── Update access: add new team tools, retain shared     │
│ ├── Remove from old team channels, add to new            │
│ ├── Update org chart                                     │
│ ├── Announce in both team channels                       │
│ └── If comp change: update payroll                       │
│                                                         │
│ Tools: hris-integration, sso-provisioner, payroll-connector, │
│        slack-notifier                                   │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 5. NEW ROLE ONBOARDING LITE (30 days)                   │
│                                                         │
│ Different from external onboarding — skip company basics │
│ Actions:                                                │
│ ├── New team welcome (1:1s with direct teammates)        │
│ ├── Role-specific training (LMS courses if applicable)   │
│ ├── Assign new onboarding buddy (from new team)          │
│ ├── 30-day check-in with new manager                     │
│ ├── Pulse survey: "How's the transition going?" (1-10)   │
│ └── Close internal mobility case in Lever                │
│                                                         │
│ Tools: lms-integration, survey-engine, slack-notifier    │
│ Agent: hr-helpdesk                                      │
└─────────────────────────────────────────────────────────┘
```

## Compensation Guidelines for Transfers
- **Lateral move** (same level): No comp change unless below new band minimum
- **Promotion** (higher level): Target 50th percentile of new band, minimum 8% increase
- **Cross-functional** (different job family): Align to new job family bands
- All comp changes require HR + finance approval

## Timeline Summary
| Phase | Duration |
|-------|----------|
| Approval | 3-5 business days |
| Transition planning | 1 week |
| Knowledge transfer | 2-3 weeks |
| Transition day | 1 day |
| New role onboarding | 30 days |
| **Total** | **5-7 weeks** |
