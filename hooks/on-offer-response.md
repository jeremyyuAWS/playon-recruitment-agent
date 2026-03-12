# Hook: Offer Response Tracking

## Trigger
When a candidate responds to an offer (accept, decline, negotiate).

## Actions

### Accepted
1. Notify hiring manager and recruiter via Slack
2. Initiate background check via background-check tool
3. Create onboarding checklist (trigger onboarding-workflow skill)
4. Create employee record in HRIS (pending background check)
5. Send to #new-hires Slack channel

### Declined
1. Notify hiring manager and recruiter
2. Log decline reason in Lever
3. Add candidate to talent CRM for future re-engagement
4. If top candidate, auto-advance next-ranked candidate
5. If pipeline empty, trigger candidate-sourcing skill

### Negotiating
1. Notify recruiter with candidate's counter-offer details
2. Run compensation-benchmarking skill against counter
3. Route recommendation to hiring manager for decision
4. Set 48-hour response SLA
