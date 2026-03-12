# playon-recruitment-manager

Comprehensive multi-agent recruitment and HR management system for PlayOn Sports. A managerial agent orchestrating 6 specialized sub-agents across the full employee lifecycle — from requisition approval through onboarding and ongoing performance management. Handles 2,500+ applications per role with stack-ranking, anti-prompt injection, diversity screening, and human-in-the-loop escalation. All integrated bidirectionally with Lever ATS.

## Run

```bash
npx @open-gitagent/gitagent run -r https://github.com/jeremyyuAWS/playon-recruitment-agent
```

## What It Can Do

### Talent Acquisition
- **Stack-rank thousands of applications** with weighted match scores (0-100)
- **Detect prompt injection** in resumes (hidden text, instruction overrides, encoding tricks)
- **Blind diversity screening** — redacts identifying info before scoring to reduce bias
- **Proactive candidate sourcing** — outbound search for hard-to-fill roles
- **Candidate rediscovery** — resurface past applicants when matching roles open
- **Compensation benchmarking** — validate expectations against market data and internal bands
- **Job description optimization** — remove bias, improve clarity, ensure compliance

### Hiring Pipeline
- **Requisition approval workflow** — manager → dept head → finance → HR → posting
- **Internal mobility matching** — check existing employees before external posting
- **AI-powered pre-screening calls** — confirm comp, experience, and availability
- **Technical assessments** — HackerRank/Codility integration for coding challenges
- **Interview scheduling** — automatic calendar matching with buffer and daily caps
- **Interview question generation** — role-specific behavioral + technical questions
- **Video interview management** — Zoom/Teams links, recording, transcripts
- **Structured feedback collection** — forms, aggregated summaries, debrief reports
- **Offer generation** — draft offers with comp details, route via DocuSign
- **Background & reference checks** — automated outreach and tracking
- **Job board distribution** — Indeed, LinkedIn, Glassdoor, BuiltIn, Dice, AngelList

### HR & Employee Experience
- **End-to-end onboarding** — equipment, access, training, buddy, 30/60/90 check-ins
- **HR helpdesk** — policy queries, benefits, leave, handbook navigation
- **Employee sentiment tracking** — pulse surveys, satisfaction scoring, retention risk
- **Performance management** — quarterly reviews, manager coaching prompts
- **Skills gap analysis** — team capability vs. needs for hiring/training decisions
- **Offboarding workflow** — exit interview, access revocation, knowledge transfer
- **Immigration tracking** — visa status, H-1B, work authorization expiry alerts
- **Learning management** — assign and track required training completion

### Reporting & Compliance
- **C-suite dashboard** — conversational hiring metrics, attrition, pipeline health
- **Workforce planning** — headcount forecasting, attrition projections, gap analysis
- **Compliance reporting** — EEO-1, OFCCP, adverse impact, pay transparency
- **Slack notifications** — real-time hiring updates, approval requests, escalations

## Architecture

```
Manager Agent (orchestrator)
├── Talent Acquisition Agent — resume parsing, match scoring, stack ranking
├── Pre-Screening Agent — outreach, compensation validation, AI calling
├── Talent Operations Agent — requisitions, job posting, internal mobility, offboarding
├── HR Helpdesk Agent — onboarding, policy queries, buddy program
├── Performance Tracking Agent — quarterly reviews, sentiment, retention
└── C-Suite Reporting Agent — executive metrics, analytics, forecasting
```

## Structure

```
playon-recruitment-agent/
├── agent.yaml                              # Manager agent config (19 skills, 18 tools)
├── SOUL.md                                 # Manager identity & orchestration style
├── RULES.md                                # Hard constraints & boundaries
├── README.md
│
├── agents/                                 # 6 specialized sub-agents
│   ├── talent-acquisition/                 # Resume scanning & stack ranking
│   ├── pre-screening/                      # Outreach & scheduling
│   ├── talent-operations/                  # Requisitions, posting, mobility, offboarding
│   ├── hr-helpdesk/                        # Employee support & onboarding
│   ├── performance-tracking/               # Reviews & sentiment
│   └── csuite-reporting/                   # Executive analytics
│
├── skills/                                 # 19 reusable capabilities
│   ├── stack-ranking/                      # Weighted candidate scoring
│   ├── anti-prompt-injection/              # Resume security scanning
│   ├── calendar-scheduling/                # Interview booking automation
│   ├── diversity-screening/                # Blind resume review
│   ├── compensation-benchmarking/          # Market rate validation
│   ├── offer-generation/                   # Offer letter drafting & routing
│   ├── candidate-sourcing/                 # Proactive outbound sourcing
│   ├── candidate-rediscovery/              # Re-surface past applicants
│   ├── onboarding-workflow/                # 90-day onboarding automation
│   ├── offboarding-workflow/               # Exit process management
│   ├── interview-feedback/                 # Structured feedback collection
│   ├── interview-question-generator/       # Role-specific question creation
│   ├── job-description-optimizer/          # JD bias removal & optimization
│   ├── requisition-approval/               # Req approval workflow
│   ├── internal-mobility/                  # Internal candidate matching
│   ├── employee-sentiment/                 # Pulse surveys & satisfaction
│   ├── workforce-planning/                 # Headcount forecasting
│   ├── skills-gap-analysis/                # Team capability assessment
│   └── compliance-reporting/               # EEO, OFCCP, regulatory reports
│
├── tools/                                  # 18 integrations
│   ├── lever-ats.yaml                      # Lever ATS (bidirectional)
│   ├── candidate-emailer.yaml              # Template-based email outreach
│   ├── calendar-booker.yaml                # Interview scheduling
│   ├── ai-caller.yaml                      # AI voice pre-screening calls
│   ├── video-interview.yaml                # Zoom/Teams management
│   ├── skills-assessment.yaml              # HackerRank/Codility integration
│   ├── background-check.yaml               # Criminal, education, employment checks
│   ├── reference-checker.yaml              # Automated reference collection
│   ├── docusign-integration.yaml           # Electronic document signing
│   ├── job-board-poster.yaml               # Multi-board job posting
│   ├── talent-crm.yaml                     # Passive candidate nurturing
│   ├── hris-integration.yaml               # Workday/BambooHR/ADP
│   ├── payroll-connector.yaml              # ADP/Gusto payroll sync
│   ├── lms-integration.yaml                # Learning management
│   ├── immigration-tracker.yaml            # Visa & work authorization
│   ├── slack-notifier.yaml                 # Notifications & approvals
│   ├── survey-engine.yaml                  # Employee surveys
│   └── analytics-dashboard.yaml            # Hiring & workforce metrics
│
├── hooks/                                  # 5 lifecycle event triggers
│   ├── on-high-score-candidate.md          # Alert on 90+ match score
│   ├── on-pipeline-stall.md                # Detect SLA breaches
│   ├── on-offer-response.md                # Handle accept/decline/negotiate
│   ├── on-visa-expiry.md                   # Immigration deadline alerts
│   └── on-sentiment-drop.md               # Department mood change alerts
│
├── workflows/                              # 3 end-to-end processes
│   ├── new-requisition.md                  # Req → Post → Screen → Interview → Hire → Onboard
│   ├── offer-to-hire.md                    # Offer → Sign → Background → Payroll → Onboard
│   └── quarterly-review-cycle.md           # Survey → Analysis → Reviews → Reporting
│
├── knowledge/                              # 7 reference documents
│   ├── index.yaml
│   ├── playon-context.md                   # Company & team context
│   ├── hiring-sla.md                       # Pipeline stage targets
│   ├── scoring-rubric.md                   # Match score criteria
│   ├── interview-question-bank.md          # Structured question library
│   ├── benefits-guide.md                   # Full benefits package
│   ├── employee-handbook.md                # HR policies reference
│   └── compensation-bands.md              # Pay bands by level & location
│
└── memory/                                 # Cross-session context
    └── README.md                           # Memory structure documentation
```

## Key Features

| Feature | Description |
|---------|-------------|
| Stack Ranking | 5-category weighted scoring (Skills 35%, Exp 25%, Edu 15%, Culture 15%, Bonus 10%) |
| Anti-Prompt Injection | Detects hidden text, instruction overrides, encoding tricks in resumes |
| Diversity Screening | Blind resume review — redacts names, schools, age indicators before scoring |
| AI Pre-Screening | Voice calls and email to confirm comp, experience, and availability |
| Internal Mobility | Match existing employees to open roles before external posting |
| Human-in-the-Loop | Escalates uncertain decisions to recruiters instead of auto-deciding |
| ATS-Native | Bidirectional Lever integration — recruiters never leave their ATS |
| Full Pipeline | Source → Screen → Assess → Interview → Feedback → Offer → Background → Onboard |
| Lifecycle Hooks | Auto-alerts for high scores, stalled pipelines, offer responses, visa expiry |
| End-to-End Workflows | Visual process maps from requisition to hire to quarterly review |
| Compliance | EEO-1, OFCCP, adverse impact analysis, pay transparency, FCRA |
| Workforce Intelligence | Headcount forecasting, skills gap analysis, sentiment tracking, attrition modeling |

## Built with

[gitagent](https://github.com/open-gitagent/gitagent) — a git-native, framework-agnostic open standard for AI agents.
