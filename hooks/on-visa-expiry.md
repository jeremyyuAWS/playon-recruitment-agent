# Hook: Visa Expiry Alert

## Trigger
When an employee's work authorization expires within 90 days.

## Action
1. Alert HR and the employee's manager via Slack DM
2. Check if renewal/extension has been initiated in immigration-tracker
3. If no case exists, create one and assign to immigration attorney
4. Send employee a reminder with required documentation list
5. At 60 days: escalate to HR director if no action taken
6. At 30 days: critical alert to VP HR

## Message Template
```
:passport_control: Work Authorization Expiry Alert

Employee: [Name]
Visa Type: [Type]
Expiry Date: [Date]
Days Remaining: [X]
Renewal Status: [Initiated/Not Started/In Progress]
Action Required: [Specific next step]
```
