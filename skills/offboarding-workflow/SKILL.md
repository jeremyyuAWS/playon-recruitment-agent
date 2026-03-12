---
name: offboarding-workflow
description: End-to-end employee offboarding — exit interview, access revocation, knowledge transfer, equipment return
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: hr-operations
---

# Offboarding Workflow

## Instructions

Manage the complete employee departure process from resignation/termination through final day.

### Trigger Events
- Employee resignation (voluntary)
- Termination (involuntary)
- Contract end
- Retirement

### Offboarding Checklist

#### Immediate (Day of notice)
- [ ] HR confirms last day and transition timeline
- [ ] Notify IT: schedule access revocation for last day
- [ ] Notify finance: final paycheck, PTO payout, benefits termination date
- [ ] Manager assigns knowledge transfer plan
- [ ] Schedule exit interview (HR, not direct manager)

#### Transition Period
- [ ] Knowledge transfer sessions with successor or team
- [ ] Document handoff: projects, passwords (via vault), key contacts
- [ ] Client/stakeholder notification (if external-facing role)
- [ ] Reassign ongoing tasks and meetings
- [ ] Update org chart and team distribution lists

#### Last Day
- [ ] Exit interview completed
- [ ] Equipment return: laptop, badge, keys, monitors
- [ ] Access revocation: email, Slack, GitHub, VPN, all SaaS tools
- [ ] Final paycheck and benefits info packet sent
- [ ] Remove from HRIS active roster
- [ ] Alumni network invitation (voluntary departures only)

#### Post-Departure
- [ ] 30-day check: verify all access revoked (security audit)
- [ ] COBRA/benefits continuation paperwork sent
- [ ] Update internal knowledge base with any gaps identified
- [ ] Backfill requisition created (if approved)

### Exit Interview Questions
1. What prompted your decision to leave?
2. What did you enjoy most about working here?
3. What would you change about the team or company?
4. How would you describe your relationship with your manager?
5. Would you consider returning in the future?
6. Is there anything we could have done to retain you?

### Data Capture
Aggregate exit interview themes quarterly:
```
Top Departure Reasons (Q[X]):
1. [Reason] — [X]% of departures
2. [Reason] — [X]%
3. [Reason] — [X]%

Actionable Insight: [Pattern or recommendation]
```

### Rules
- Involuntary terminations: IT access revoked same day, escorted departure per policy
- Voluntary departures: standard 2-week notice period
- Exit interview data is confidential — aggregate only, never attributed
- Never skip security access audit — even for trusted long-tenure employees
- Final paycheck timing must comply with state law (some states require same-day)
