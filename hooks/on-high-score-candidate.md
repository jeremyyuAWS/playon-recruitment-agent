# Hook: High-Score Candidate Alert

## Trigger
When a candidate scores 90+ on the stack-ranking evaluation.

## Action
1. Send Slack notification to #hiring-alerts with candidate summary
2. DM the hiring manager with the candidate profile
3. Auto-advance candidate to pre-screening with priority flag
4. Tag candidate as "fast-track" in Lever

## Message Template
```
:star: High-Score Candidate Alert

Role: [Title]
Candidate: [Name]
Match Score: [Score]/100
Top Skills: [Skills]
Status: Auto-advanced to pre-screening (fast-track)

@[hiring-manager] — heads up, this one looks strong.
```
