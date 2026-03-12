---
name: requisition-approval
description: Manages the requisition approval workflow from manager request through finance and HR sign-off to posting
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Requisition Approval Workflow

## Instructions

Gate the opening of new positions through a structured approval process.

### Approval Flow

```
1. Manager submits requisition
   ↓
2. Validate: role title, level, department, budget, justification
   ↓
3. Route to department head for approval
   ↓
4. Route to finance for headcount/budget confirmation
   ↓
5. Route to HR for compensation band and JD review
   ↓
6. Approved → Create posting in Lever + notify recruiter
   OR
   Rejected → Notify manager with reason + next steps
```

### Requisition Form Fields
- **Role title** and level (IC or management, seniority)
- **Department** and team
- **Justification**: New headcount / Backfill / Conversion (contractor→FTE)
- **Business case**: Why now? Revenue impact? Risk if unfilled?
- **Budget**: Approved compensation range (base + bonus + equity)
- **Start date target**
- **Hiring manager**
- **Interview panel** (suggested interviewers)

### SLA Targets
| Step | Target | Escalation |
|------|--------|------------|
| Department head approval | 2 business days | Auto-remind at 24h, escalate at 48h |
| Finance approval | 2 business days | Auto-remind at 24h, escalate at 48h |
| HR review | 1 business day | Auto-remind at 12h, escalate at 24h |
| Total approval cycle | 5 business days | Flag to VP if exceeded |

### Notifications
- Slack DM to each approver when their turn arrives
- Daily digest of pending approvals to department heads
- Manager notified at each approval stage
- Recruiter notified immediately upon final approval

### Rules
- No requisition can be posted without all 3 approvals
- Budget exceptions (>10% above band) require VP sign-off
- Backfill requisitions get expedited (24h per step)
- All requisitions logged with full audit trail
