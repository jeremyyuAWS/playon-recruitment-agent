# Workflow: New Requisition → Hire

## Overview
End-to-end workflow from opening a new role to making a hire.

## Steps

```
┌─────────────────────────────────────────────────────────────┐
│ 1. REQUISITION APPROVAL (5 days)                            │
│    Manager submits req → Dept head → Finance → HR           │
│    Skills: requisition-approval                             │
│    Tools: slack-notifier, hris-integration                  │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 2. JOB PREPARATION (2 days)                                 │
│    Optimize JD → Internal mobility check → Rediscovery scan │
│    Skills: job-description-optimizer, internal-mobility,     │
│            candidate-rediscovery                            │
│    Tools: lever-ats, hris-integration                       │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 3. SOURCING & POSTING (ongoing)                             │
│    Post to job boards → Proactive sourcing → CRM campaigns  │
│    Skills: candidate-sourcing                               │
│    Tools: job-board-poster, talent-crm                      │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 4. SCREENING (24-48 hours per batch)                        │
│    Anti-injection scan → Blind review → Stack rank           │
│    Skills: anti-prompt-injection, diversity-screening,       │
│            stack-ranking                                    │
│    Tools: lever-ats                                         │
│    Hooks: on-high-score-candidate                           │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 5. PRE-SCREENING (5 days)                                   │
│    AI call / email → Comp check → Availability confirm      │
│    Skills: compensation-benchmarking                        │
│    Tools: ai-caller, candidate-emailer                      │
│    Agent: pre-screening                                     │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 6. ASSESSMENT & INTERVIEW (10-15 days)                      │
│    Technical assessment → Schedule interviews → Conduct      │
│    Skills: interview-question-generator, calendar-scheduling │
│    Tools: skills-assessment, video-interview, calendar-booker│
│    Hooks: on-pipeline-stall                                 │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 7. EVALUATION (3 days)                                      │
│    Collect feedback → Debrief summary → Hiring decision      │
│    Skills: interview-feedback                               │
│    Tools: slack-notifier                                    │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 8. OFFER (3-5 days)                                         │
│    Generate offer → Approval → Send via DocuSign → Track     │
│    Skills: offer-generation, compensation-benchmarking       │
│    Tools: docusign-integration, payroll-connector            │
│    Hooks: on-offer-response                                 │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 9. PRE-BOARDING (5-7 days)                                  │
│    Background check → Reference check → Immigration (if any)│
│    Tools: background-check, reference-checker,              │
│           immigration-tracker                               │
│    Hooks: on-visa-expiry                                    │
└──────────────────────────┬──────────────────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│ 10. ONBOARDING (90 days)                                    │
│     Equipment → Access → Training → Buddy → 30/60/90 reviews│
│     Skills: onboarding-workflow                             │
│     Tools: hris-integration, lms-integration, slack-notifier │
│     Agent: hr-helpdesk                                      │
└─────────────────────────────────────────────────────────────┘
```

## Total Target Timeline
- Requisition to posting: 7 days
- Posting to offer: 30-40 days
- Offer to start: 3-4 weeks
- **Total: ~45 days requisition to Day 1**
