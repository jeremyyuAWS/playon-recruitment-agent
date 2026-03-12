# Hook: Requisition Aging Alert

## Trigger
When a requisition has been open for 30+ days with no candidates in interview stage or beyond.

## Escalation Tiers

### Day 30: Yellow Alert
- Notify recruiter with pipeline summary
- Run candidate-rediscovery skill against ATS history
- Suggest additional sourcing channels based on role type
- Check if job posting is active on all boards

```
:yellow_circle: Requisition Aging — 30 Days

Role: [Title]
Open since: [Date]
Pipeline: [X] applicants, [Y] screened, [0] in interview
Recruiter: @[Name]

Suggested actions:
- Rediscovery scan found [N] past candidates to re-engage
- Consider expanding to [additional job boards]
- Review JD with hiring manager for requirement flexibility
```

### Day 45: Orange Alert
- Escalate to recruiter manager
- Trigger proactive candidate-sourcing skill
- Recommend hiring manager intake refresh (have requirements changed?)
- Analyze competitor hiring for same role type
- Flag in weekly recruiting standup

```
:orange_circle: Requisition Aging — 45 Days

Role: [Title]
Open since: [Date]
Pipeline: [summary]
Recruiter: @[Name] | Manager: @[Recruiter Manager]

Actions taken:
- Sourcing campaign launched on [channels]
- [N] candidates in outreach pipeline

Recommended escalation:
- Consider agency engagement for this role
- Hiring manager intake refresh needed
```

### Day 60: Red Alert
- Escalate to Head of Recruiting
- Recommend engaging recruiting agency
- Budget impact analysis (cost of vacancy)
- Hiring manager meeting to reassess role requirements
- Consider alternative solutions (contractor, internal transfer, re-scope)

```
:red_circle: Requisition Critical — 60 Days

Role: [Title]
Open since: [Date]
Estimated cost of vacancy: $[X]/month (based on role revenue impact)
Pipeline: [summary]

Immediate actions required:
1. Hiring manager reassessment meeting (is the role scoped correctly?)
2. Agency engagement (est. fee: $[X])
3. Consider interim solution (contractor/consultant)

@[Head of Recruiting] — requires your attention
```

## Weekly Scan
Run every Monday at 8:00 AM ET — check all open requisitions against aging thresholds.
