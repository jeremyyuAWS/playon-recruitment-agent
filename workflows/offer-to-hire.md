# Workflow: Offer to Hire

## Overview
From hiring decision through the candidate's first day. This is where deals close or fall apart — speed and communication are critical.

## Steps

```
┌─────────────────────────────────────────────────────────┐
│ 1. OFFER PREPARATION (1-2 days)                         │
│                                                         │
│    Input: Hiring decision + approved compensation        │
│    Actions:                                             │
│    ├── Generate offer letter (offer-generation skill)    │
│    ├── Run comp benchmark (compensation-benchmarking)    │
│    ├── Route to HR for legal review                      │
│    └── Route to hiring manager for final sign-off        │
│                                                         │
│    Tools: docusign-integration, slack-notifier           │
│    Gate: HR + hiring manager approval required           │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 2. OFFER DELIVERY (same day as approval)                │
│                                                         │
│    Actions:                                             │
│    ├── Send offer via DocuSign                           │
│    ├── Recruiter verbal call to walk through offer       │
│    ├── Set 5-day response deadline                       │
│    └── Update Lever status to "Offer Extended"           │
│                                                         │
│    Tools: docusign-integration, lever-ats, ai-caller     │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 3. OFFER TRACKING (1-5 days)                            │
│                                                         │
│    Monitor:                                             │
│    ├── DocuSign open/view events                         │
│    ├── Candidate questions (route to recruiter)          │
│    └── Day 3: proactive recruiter check-in               │
│                                                         │
│    Branches:                                            │
│    ├── ACCEPTED → Step 4                                 │
│    ├── NEGOTIATING → Comp benchmark + HM decision        │
│    └── DECLINED → Log reason, advance backup candidate   │
│                                                         │
│    Hooks: on-offer-response                             │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 4. POST-ACCEPTANCE (1-2 days)                           │
│                                                         │
│    Parallel actions:                                    │
│    ├── Initiate background check                         │
│    ├── Send reference check requests                     │
│    ├── Check work authorization / visa needs             │
│    ├── Create payroll record (pending background)        │
│    ├── Notify rejected candidates (other finalists)      │
│    └── Post #new-hires Slack announcement                │
│                                                         │
│    Tools: background-check, reference-checker,           │
│           immigration-tracker, payroll-connector,        │
│           slack-notifier                                │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 5. CLEARANCE (5-10 days)                                │
│                                                         │
│    Wait for:                                            │
│    ├── Background check clear                            │
│    ├── Reference check responses (min 2 of 3)            │
│    ├── Immigration clearance (if applicable)             │
│    └── DocuSign: NDA, I-9, benefits enrollment           │
│                                                         │
│    If background check fails:                           │
│    ├── Route to HR for adverse action review              │
│    ├── Follow FCRA requirements (pre-adverse → wait →    │
│    │   adverse action notice)                            │
│    └── DO NOT auto-rescind — human decision required      │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ 6. ONBOARDING LAUNCH (2 weeks before start)             │
│                                                         │
│    Actions:                                             │
│    ├── Create HRIS employee record (active)              │
│    ├── IT ticket: equipment order                        │
│    ├── Access provisioning request                       │
│    ├── Assign onboarding buddy                           │
│    ├── Schedule Day 1 orientation                        │
│    ├── Assign LMS training path                          │
│    └── Send welcome email with first-week schedule       │
│                                                         │
│    Skills: onboarding-workflow                           │
│    Tools: hris-integration, lms-integration,             │
│           slack-notifier                                │
│    Agent: hr-helpdesk                                   │
└─────────────────────────────────────────────────────────┘
```

## SLA Summary
| Step | Target |
|------|--------|
| Offer prep | 2 days from decision |
| Offer delivery | Same day as approval |
| Candidate response | 5 days |
| Background check | 7 days |
| References | 5 days |
| Onboarding prep | 2 weeks before start |
| **Total offer-to-start** | **3-4 weeks** |
