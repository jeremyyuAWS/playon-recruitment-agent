# Hook: Candidate Withdrawal

## Trigger
When a candidate withdraws from the hiring process at any stage.

## Action
1. Log withdrawal reason in Lever (categorized):
   - Accepted another offer
   - Compensation mismatch
   - Role not as described
   - Too slow process
   - Personal reasons
   - Counter-offered by current employer
   - Unresponsive (assumed withdrawal after 2 follow-ups)
2. Notify hiring manager and recruiter via Slack
3. Send brief candidate experience survey (optional, 2 questions max)
4. Add to talent CRM if they were interview-stage or beyond
5. Auto-advance next-ranked candidate in pipeline if applicable
6. If withdrawal reason is "too slow process" — flag the role for SLA review

## Message to Team
```
:runner: Candidate Withdrawal

Candidate: [Name]
Role: [Title]
Stage: [Pipeline stage at withdrawal]
Reason: [Category]
Details: [Any specifics provided]

Next candidate in pipeline: [Name, score] — auto-advanced to [stage]
```

## Analytics
Track withdrawal reasons monthly — if any single reason exceeds 25% of total withdrawals, escalate to Head of Recruiting for process review.
