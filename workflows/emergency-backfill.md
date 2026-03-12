# Workflow: Emergency Backfill

## Overview
Fast-track process for unexpected departures in critical roles. Compressed SLAs, pre-approved sourcing budget, and streamlined gates to get someone in seat ASAP.

## When to Activate
- Critical role holder gives notice (2 weeks or less)
- Unexpected termination of key personnel
- Extended leave with no succession plan in place
- Business-critical project at risk without immediate hire

## Steps

```
┌─────────────────────────────────────────────────────────┐
│ DAY 0: ACTIVATION                                       │
│                                                         │
│ Actions:                                                │
│ ├── Head of Recruiting declares emergency backfill       │
│ ├── Skip standard requisition approval (VP pre-approved) │
│ ├── Pull succession plan for this role (if exists)       │
│ ├── Assign dedicated recruiter (reduce other req load)   │
│ ├── Pre-approve sourcing budget ($[X] agency + job boards)│
│ ├── Activate candidate-rediscovery immediately           │
│ └── Notify finance of unplanned hiring spend             │
│                                                         │
│ Skills: succession-planning, candidate-rediscovery       │
│ Tools: slack-notifier, lever-ats                        │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ DAYS 1-2: PIPELINE BLAST                                │
│                                                         │
│ Parallel actions (all at once, not sequential):          │
│ ├── Internal mobility scan (can anyone transfer?)        │
│ ├── Rediscovery: pull all 60+ scored candidates from ATS │
│ ├── Talent CRM: contact all warm candidates in pool      │
│ ├── Agency: engage retained/contingency firm immediately  │
│ ├── LinkedIn: targeted InMail campaign (50+ profiles)    │
│ ├── Job boards: sponsored postings on all platforms       │
│ ├── Referral blast: team-wide referral ask with bonus     │
│ └── Contractor search: interim coverage while hiring      │
│                                                         │
│ Skills: internal-mobility, candidate-sourcing,           │
│         employer-branding                               │
│ Tools: linkedin-recruiter, job-board-poster, talent-crm, │
│        slack-notifier                                   │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ DAYS 3-7: COMPRESSED SCREENING                          │
│                                                         │
│ Compressed SLAs (standard → emergency):                  │
│ ├── Resume screen: 24h → same day                        │
│ ├── Pre-screen call: 48h → same day                      │
│ ├── Assessment: 72h → 48h (shortened version)            │
│ ├── Interview scheduling: 3 days → 1 day                 │
│ └── Stack-rank top candidates daily (not weekly)         │
│                                                         │
│ Skills: stack-ranking, anti-prompt-injection,            │
│         compensation-benchmarking                       │
│ Tools: ai-caller, skills-assessment                     │
│ Agent: talent-acquisition, pre-screening                │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ DAYS 5-10: INTERVIEW BLITZ                              │
│                                                         │
│ Actions:                                                │
│ ├── Condensed interview loop: 2 interviews (not 4-5)     │
│ │   ├── Technical/skills (60 min)                        │
│ │   └── Hiring manager + behavioral (60 min)             │
│ ├── Same-day debrief (no waiting for all feedback)       │
│ ├── Decision within 24 hours of final interview          │
│ └── Verbal offer same day as decision                    │
│                                                         │
│ Skills: interview-question-generator, interview-feedback │
│ Tools: video-interview, calendar-booker                  │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ DAYS 8-12: RAPID OFFER                                  │
│                                                         │
│ Actions:                                                │
│ ├── Offer generated and approved within 24 hours         │
│ ├── Competitive offer: target 60th+ percentile (not 50th)│
│ ├── Sign-on bonus pre-approved for immediate start       │
│ ├── DocuSign same day as verbal offer                    │
│ ├── Background check: rush processing (3 days)           │
│ ├── Start date: ASAP (2 weeks or less if possible)       │
│ └── Interim coverage: contractor if gap remains          │
│                                                         │
│ Skills: offer-generation, counter-offer-strategy         │
│ Tools: docusign-integration, background-check            │
│ Hooks: on-offer-response                                │
└────────────────────────┬────────────────────────────────┘
                         ▼
┌─────────────────────────────────────────────────────────┐
│ DAYS 10-15: ACCELERATED ONBOARDING                      │
│                                                         │
│ Actions:                                                │
│ ├── Pre-start: equipment + access provisioned before Day 1│
│ ├── Day 1: abbreviated orientation (2 hours, not full day)│
│ ├── Immediate immersion in critical work                 │
│ ├── Dedicated mentor (not just buddy) for first 2 weeks  │
│ ├── Daily check-ins for first week                       │
│ └── 30-day formal check-in (90-day still applies)        │
│                                                         │
│ Skills: onboarding-workflow                              │
│ Tools: sso-provisioner, lms-integration, hris-integration│
│ Agent: hr-helpdesk                                      │
└─────────────────────────────────────────────────────────┘
```

## Emergency vs. Standard SLAs

| Stage | Standard | Emergency |
|-------|----------|-----------|
| Requisition approval | 5 days | 0 (pre-approved) |
| JD + posting | 2 days | 1 day |
| Resume screening | 1 week | Same day |
| Pre-screening | 5 days | 1-2 days |
| Interview loop | 10-15 days | 3-5 days |
| Hiring decision | 3 days | 1 day |
| Offer prep + approval | 3 days | 1 day |
| Background check | 7 days | 3 days (rush) |
| **Total** | **~45 days** | **~15 days** |

## Budget Pre-Approvals
- Agency fee: up to $[X] (typically 20-25% of base)
- Sign-on bonus: up to $[X] (to incentivize fast start)
- Rush background check: +$[X] per candidate
- Sponsored job postings: up to $[X] across platforms
- Contractor coverage: up to $[X]/month while hiring

## Rules
- Emergency backfill does NOT bypass:
  - Background checks (can be rushed, not skipped)
  - At least 2 interviews (condensed, not eliminated)
  - Reference checks (can run in parallel with offer)
  - Compensation band limits (exceptions still need VP approval)
- Maximum 3 active emergency backfills at any time (recruiter capacity)
- Post-mortem after each emergency: why was there no succession plan?
