# Hook: Pipeline Stall Detection

## Trigger
When a candidate has been in the same pipeline stage for longer than the SLA target (see hiring-sla.md).

## Action
1. Check which stage is stalled and who owns it
2. Send reminder to the owner (recruiter, interviewer, or hiring manager)
3. If stalled 2x past SLA, escalate to recruiter manager
4. If stalled 3x past SLA, escalate to Head of Recruiting

## Escalation Chain
```
Day SLA+1: Friendly reminder to owner
Day SLA×2: Escalation to recruiter manager + owner
Day SLA×3: Escalation to Head of Recruiting
```

## Daily Scan
Run daily at 9:00 AM ET — check all active candidates against SLA targets.

## Message Template
```
:warning: Pipeline Stall — [Stage Name]

Candidate: [Name]
Role: [Title]
Days in stage: [X] (SLA: [Y] days)
Owner: @[Owner]
Action needed: [Specific action required]
```
