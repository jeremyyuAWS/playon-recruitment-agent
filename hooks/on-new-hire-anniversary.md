# Hook: New Hire Anniversary Milestones

## Trigger
Employee reaches 30, 60, 90, or 365 days since start date.

## Actions

### Day 30
- Send pulse check survey to new hire (3 questions):
  - "How supported do you feel?" (1-10)
  - "Is the role what you expected?" (Yes/Mostly/No)
  - "What's been your biggest challenge so far?" (free text)
- Remind manager to conduct 30-day check-in
- Remind buddy to schedule coffee/check-in
- If survey score <6: flag to HR for follow-up

### Day 60
- Send second pulse check survey:
  - "How confident are you in your role?" (1-10)
  - "Do you have the tools and access you need?" (Yes/No + details)
  - "How would you rate your onboarding experience?" (1-10)
- Remind manager to conduct 60-day check-in
- Check LMS: are all required trainings completed?
- If any training overdue: escalate to manager

### Day 90
- Trigger formal 90-day review (performance-tracking agent)
- Graduate from buddy program
- Send comprehensive onboarding satisfaction survey
- Calculate quality-of-hire score:
  - Manager satisfaction (from review)
  - New hire satisfaction (from survey)
  - Training completion rate
  - Early productivity indicators
- Feed quality-of-hire data back to talent acquisition for sourcing optimization

### Day 365 (1-Year Anniversary)
- Congratulations message via Slack (#celebrations channel)
- Manager reminder for annual review prep
- Retention check: flag if any risk signals in past quarter
- Track 1-year retention rate as a hiring quality KPI
- If employee's referral source is tracked: update source effectiveness data

## Message Templates

### Day 90 Manager Reminder
```
:calendar: 90-Day Review Due

Employee: [Name]
Start Date: [Date]
Manager: @[Manager]

Action needed: Schedule formal 90-day review within the next week.
Talking points and self-assessment have been shared with you.
```

### Day 365 Celebration
```
:tada: Happy 1-Year Anniversary!

[Name] joined the [Department] team one year ago today as [Title].

@[Manager] — consider acknowledging this milestone with the team!
```
