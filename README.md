# playon-recruitment-manager

Multi-agent recruitment management system for PlayOn Sports. A managerial agent that orchestrates 5 specialized sub-agents to handle high-volume talent acquisition (2,500+ applications per role), automated pre-screening, HR helpdesk, performance tracking, and C-suite reporting — all integrated with Lever ATS.

## Run

```bash
npx @open-gitagent/gitagent run -r https://github.com/jeremyyuAWS/playon-recruitment-agent
```

## What It Can Do

- **Stack-rank thousands of applications** against job descriptions with weighted match scores (0-100)
- **Detect prompt injection** in resumes (hidden text, instruction overrides, encoding tricks)
- **Automate pre-screening** — confirm compensation, experience, and availability via email
- **Schedule interviews** automatically by matching candidate and recruiter calendars
- **Answer HR questions** — onboarding, policies, buddy assignments, benefits
- **Track performance** — quarterly reviews, sentiment analysis, retention risk flagging
- **Report to leadership** — real-time hiring metrics, attrition, pipeline health via conversation

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
│   │   ├── agent.yaml
│   │   └── SOUL.md
│   ├── pre-screening/                  # Outreach & scheduling
│   │   ├── agent.yaml
│   │   └── SOUL.md
│   ├── hr-helpdesk/                    # Employee support & onboarding
│   │   ├── agent.yaml
│   │   └── SOUL.md
│   ├── performance-tracking/           # Reviews & sentiment
│   │   ├── agent.yaml
│   │   └── SOUL.md
│   └── csuite-reporting/              # Executive analytics
│       ├── agent.yaml
│       └── SOUL.md
├── skills/
│   ├── stack-ranking/                  # Weighted candidate scoring
│   │   └── SKILL.md
│   ├── anti-prompt-injection/          # Resume security scanning
│   │   └── SKILL.md
│   └── calendar-scheduling/            # Interview booking automation
│       └── SKILL.md
├── tools/
│   ├── lever-ats.yaml                  # Lever ATS integration
│   ├── candidate-emailer.yaml          # Email outreach
│   └── calendar-booker.yaml            # Calendar management
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
| Human-in-the-Loop | Escalates uncertain decisions to recruiters instead of auto-deciding |
| ATS-Native | Bidirectional Lever integration — recruiters never leave their ATS |
| Separation of Concerns | Recruitment data stays separate from performance/HR data |

## Built with

[gitagent](https://github.com/open-gitagent/gitagent) — a git-native, framework-agnostic open standard for AI agents.
