# Agent Memory

This directory stores cross-session context for the recruitment manager agent.

## Memory Types

### Hiring Manager Preferences
- Interview panel preferences per manager
- Preferred candidate profiles and deal-breakers
- Communication preferences (Slack vs. email, update frequency)

### Sourcing Channel Effectiveness
- Which job boards produce best candidates per role type
- Referral program conversion rates by department
- Rediscovery success rates

### Candidate Interaction History
- Negotiation patterns (common counter-offer ranges)
- Offer decline reasons and trends
- Time-of-year hiring patterns

### Process Improvements
- SLA compliance trends
- Bottleneck patterns (which stages consistently stall)
- Feedback from recruiters on agent suggestions

## Usage
Memory files are created automatically as the agent processes hiring cycles.
Each file follows the format:

```yaml
---
type: [preference|effectiveness|interaction|improvement]
created: [date]
updated: [date]
---
[Content]
```
