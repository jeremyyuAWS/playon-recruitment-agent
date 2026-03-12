---
name: calendar-scheduling
description: Automated interview scheduling with recruiter calendar integration and candidate availability matching
license: MIT
allowed-tools: Read Grep
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Calendar Scheduling

## Instructions

Automatically schedule interviews by matching candidate availability with recruiter calendars.

### Process

1. Receive qualified candidate list from pre-screening
2. Check recruiter calendar availability (30-min and 60-min slots)
3. Send candidate availability request via email
4. Match overlapping windows, preferring:
   - Earlier dates (speed matters at scale)
   - Recruiter's preferred interview blocks
   - Buffer time between interviews (15 min minimum)
5. Book the meeting and send confirmations to both parties

### Scheduling Rules

- **Time zone**: All times displayed in ET (PlayOn Sports HQ)
- **Buffer**: Minimum 15 minutes between interviews
- **Daily cap**: Max 6 interviews per recruiter per day
- **Window**: Schedule within 5 business days of pre-screen completion
- **Reminders**: Send 24-hour and 1-hour reminders to both parties

### Conflict Resolution

- Double-booking detected: Prioritize higher-scored candidate, reschedule lower
- Candidate unresponsive after 48 hours: Send one follow-up, then flag for recruiter
- No overlapping availability: Expand window to 10 business days, then escalate

### Output

For each scheduled interview:
```
Candidate: [Name]
Recruiter: [Name]
Date/Time: [ET]
Duration: [30 or 60 min]
Format: [Zoom/Phone/On-site]
Confirmation: [Sent/Pending]
```
