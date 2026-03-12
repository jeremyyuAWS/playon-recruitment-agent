# playon-recruitment-manager

Multi-agent recruitment management system for PlayOn Sports. A managerial agent that orchestrates 5 specialized sub-agents to handle high-volume talent acquisition (2,500+ applications per role), automated pre-screening, HR helpdesk, performance tracking, and C-suite reporting — all integrated with Lever ATS.

## Run

```bash
npx @open-gitagent/gitagent run -r https://github.com/jeremyyuAWS/playon-recruitment-agent
```

## What It Can Do

### Talent Acquisition
- **Stack-rank thousands of applications** against job descriptions with weighted match scores (0-100)
- **Detect prompt injection** in resumes (hidden text, instruction overrides, encoding tricks)
- **Blind diversity screening** — redacts identifying info before scoring to reduce bias
- **Proactive candidate sourcing** — outbound search for hard-to-fill roles
- **Compensation benchmarking** — validates expectations against market data and internal bands

### Hiring Pipeline
- **Automate pre-screening** — confirm compensation, experience, and availability via email
- **Schedule interviews** automatically by matching candidate and recruiter calendars
- **Collect interview feedback** — structured forms, aggregated summaries, debrief reports
- **Generate offer letters** — draft offers with comp details, route for approval via DocuSign
- **Background & reference checks** — automated outreach and tracking
- **Post to job boards** — Indeed, LinkedIn, Glassdoor, BuiltIn, Dice, AngelList

### HR & Employee Experience
- **Answer HR questions** — onboarding, policies, buddy assignments, benefits
- **End-to-end onboarding** — equipment, access, training, buddy program, 30/60/90 check-ins
- **Track employee sentiment** — pulse surveys, satisfaction scoring, retention risk flagging
- **Track performance** — quarterly reviews, manager coaching prompts

### Reporting & Compliance
- **Report to leadership** — real-time hiring metrics, attrition, pipeline health via conversation
- **Compliance reporting** — EEO-1, OFCCP, pay transparency, adverse impact analysis
- **Slack notifications** — hiring updates, approval requests, escalations

## Architecture

```
Manager Agent (orchestrator)
├── Talent Acquisition Agent — resume parsing, match scoring, stack ranking
├── Pre-Screening Agent — outreach, compensation validation, scheduling
├── HR Helpdesk Agent — onboarding, policy queries, buddy program
├── Performance Tracking Agent — quarterly reviews, sentiment, retention
└── C-Suite Reporting Agent — executive metrics, analytics, forecasting
```

## Structure

```
playon-recruitment-agent/
├── agent.yaml                          # Manager agent config
├── SOUL.md                             # Manager identity & orchestration style
├── RULES.md                            # Hard constraints & boundaries
├── README.md
├── agents/
│   ├── talent-acquisition/             # Resume scanning & stack ranking
│   ├── pre-screening/                  # Outreach & scheduling
│   ├── hr-helpdesk/                    # Employee support & onboarding
│   ├── performance-tracking/           # Reviews & sentiment
│   └── csuite-reporting/              # Executive analytics
├── skills/
│   ├── stack-ranking/                  # Weighted candidate scoring
│   ├── anti-prompt-injection/          # Resume security scanning
│   ├── calendar-scheduling/            # Interview booking automation
│   ├── diversity-screening/            # Blind resume review for bias reduction
│   ├── compensation-benchmarking/      # Market rate validation
│   ├── offer-generation/              # Offer letter drafting & routing
│   ├── candidate-sourcing/            # Proactive outbound sourcing
│   ├── onboarding-workflow/           # 90-day onboarding automation
│   ├── interview-feedback/            # Structured feedback collection
│   ├── employee-sentiment/            # Pulse surveys & satisfaction tracking
│   └── compliance-reporting/          # EEO, OFCCP, regulatory reports
├── tools/
│   ├── lever-ats.yaml                  # Lever ATS integration (bidirectional)
│   ├── candidate-emailer.yaml          # Template-based email outreach
│   ├── calendar-booker.yaml            # Interview scheduling
│   ├── background-check.yaml           # Criminal, education, employment checks
│   ├── docusign-integration.yaml       # Electronic document signing
│   ├── slack-notifier.yaml             # Hiring updates & approval requests
│   ├── survey-engine.yaml              # Employee surveys (pulse, exit, 360)
│   ├── analytics-dashboard.yaml        # Hiring & workforce metrics
│   ├── reference-checker.yaml          # Automated reference collection
│   └── job-board-poster.yaml           # Multi-board job posting
└── knowledge/
    ├── index.yaml
    ├── playon-context.md               # Company & team context
    └── scoring-rubric.md               # Match score criteria
```

## Key Features

| Feature | Description |
|---------|-------------|
| Stack Ranking | 5-category weighted scoring (Skills 35%, Exp 25%, Edu 15%, Culture 15%, Bonus 10%) |
| Anti-Prompt Injection | Detects hidden text, instruction overrides, encoding tricks in resumes |
| Diversity Screening | Blind resume review — redacts names, schools, age indicators before scoring |
| Human-in-the-Loop | Escalates uncertain decisions to recruiters instead of auto-deciding |
| ATS-Native | Bidirectional Lever integration — recruiters never leave their ATS |
| Full Pipeline | Source → Screen → Interview → Feedback → Offer → Background Check → Onboard |
| Compliance | EEO-1, OFCCP, adverse impact analysis, pay transparency |
| Separation of Concerns | Recruitment data stays separate from performance/HR data |

## Built with

[gitagent](https://github.com/open-gitagent/gitagent) — a git-native, framework-agnostic open standard for AI agents.
