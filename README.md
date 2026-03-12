# playon-recruitment-manager

Comprehensive multi-agent recruitment and HR management system for PlayOn Sports. A managerial agent orchestrating 7 specialized sub-agents across the full employee lifecycle — from hiring manager intake through onboarding, performance management, succession planning, and offboarding. Handles 2,500+ applications per role with stack-ranking, anti-prompt injection, diversity screening, and human-in-the-loop escalation. All integrated bidirectionally with Lever ATS, with environment configs for production, sandbox (demo), and development.

## Run

```bash
npx @open-gitagent/gitagent run -r https://github.com/jeremyyuAWS/playon-recruitment-agent
```

## What It Can Do

### Talent Acquisition
- **Stack-rank thousands of applications** with weighted match scores (0-100)
- **Detect prompt injection** in resumes (hidden text, instruction overrides, encoding tricks)
- **Blind diversity screening** — redacts identifying info before scoring to reduce bias
- **Hiring manager intake** — structured kickoff to extract must-haves, hidden preferences, team dynamics
- **Job description optimization** — remove bias, improve clarity, ensure compliance
- **Proactive candidate sourcing** — outbound via LinkedIn Recruiter, job boards, talent CRM
- **Candidate rediscovery** — resurface past applicants when matching roles open
- **Employer branding** — role-specific "why PlayOn" messaging for outreach
- **Compensation benchmarking** — validate expectations against market data and internal bands

### Hiring Pipeline
- **Requisition approval workflow** — manager → dept head → finance → HR → posting
- **Internal mobility matching** — check existing employees before external posting
- **AI-powered pre-screening calls** — confirm comp, experience, and availability
- **Technical assessments** — HackerRank/Codility/CodeSignal integration
- **Interview scheduling** — automatic calendar matching with buffer and daily caps
- **Interview question generation** — role-specific behavioral + technical questions by level
- **Video interview management** — Zoom/Teams links, recording, transcripts
- **Structured feedback collection** — forms, aggregated summaries, debrief reports
- **Reference check analysis** — consistency checks, red flag detection, theme extraction
- **Offer generation** — draft offers with comp details, route via DocuSign
- **Counter-offer strategy** — model scenarios (match, beat, repackage, walk away) with data
- **Background checks** — criminal, education, employment, drug screening
- **Job board distribution** — Indeed, LinkedIn, Glassdoor, BuiltIn, Dice, AngelList

### Candidate Experience
- **Stage-appropriate rejections** — personalized by pipeline depth with empathy and feedback
- **Candidate NPS surveys** — measure experience at each stage
- **Application status updates** — proactive communication, never ghost
- **Silver medal program** — finalist re-engagement for future roles via talent CRM
- **Employer brand touchpoints** — consistent messaging across all candidate interactions

### HR & Employee Experience
- **End-to-end onboarding** — equipment, access (SSO provisioning), training, buddy, 30/60/90 check-ins
- **HR helpdesk** — policy queries, benefits, leave, handbook navigation
- **Employee sentiment tracking** — pulse surveys, satisfaction scoring, retention risk
- **Performance management** — quarterly reviews, manager coaching prompts
- **Skills gap analysis** — team capability vs. needs for hiring/training decisions
- **Succession planning** — flight risk identification, internal successor mapping, proactive sourcing
- **Offboarding workflow** — exit interview, access revocation, knowledge transfer, equipment return
- **Immigration tracking** — visa status, H-1B, work authorization expiry alerts
- **Learning management** — assign and track required training completion
- **Internal transfers** — handoff, comp adjustment, new-team onboarding lite

### Reporting & Compliance
- **C-suite dashboard** — conversational hiring metrics, attrition, pipeline health
- **Workforce planning** — headcount forecasting, attrition projections, gap analysis
- **Compliance reporting** — EEO-1, OFCCP, adverse impact, pay transparency
- **Compensation review cycle** — annual merit, equity, promotion calibration
- **Recruiting spend tracking** — cost-per-hire, channel ROI, budget utilization
- **Compliance calendar** — automated filing deadline tracking and alerts
- **Slack notifications** — real-time hiring updates, approval requests, escalations

## Architecture

```
Manager Agent (orchestrator)
├── Talent Acquisition Agent — resume parsing, match scoring, stack ranking
├── Pre-Screening Agent — outreach, compensation validation, AI calling
├── Talent Operations Agent — requisitions, job posting, mobility, offboarding
├── Candidate Experience Agent — rejections, NPS, status updates, employer brand
├── HR Helpdesk Agent — onboarding, policy queries, buddy program
├── Performance Tracking Agent — quarterly reviews, sentiment, retention
└── C-Suite Reporting Agent — executive metrics, analytics, forecasting
```

## Structure

```
playon-recruitment-agent/
├── agent.yaml                              # Manager agent config (25 skills, 22 tools)
├── SOUL.md                                 # Manager identity & orchestration style
├── RULES.md                                # Hard constraints & boundaries
├── README.md
│
├── agents/                                 # 7 specialized sub-agents
│   ├── talent-acquisition/                 # Resume scanning & stack ranking
│   ├── pre-screening/                      # Outreach & scheduling
│   ├── talent-operations/                  # Requisitions, posting, mobility, offboarding
│   ├── candidate-experience/               # Rejections, NPS, employer brand
│   ├── hr-helpdesk/                        # Employee support & onboarding
│   ├── performance-tracking/               # Reviews & sentiment
│   └── csuite-reporting/                   # Executive analytics
│
├── skills/                                 # 25 reusable capabilities
│   ├── stack-ranking/                      # Weighted candidate scoring
│   ├── anti-prompt-injection/              # Resume security scanning
│   ├── calendar-scheduling/                # Interview booking automation
│   ├── diversity-screening/                # Blind resume review
│   ├── compensation-benchmarking/          # Market rate validation
│   ├── offer-generation/                   # Offer letter drafting & routing
│   ├── candidate-sourcing/                 # Proactive outbound sourcing
│   ├── candidate-rediscovery/              # Re-surface past applicants
│   ├── hiring-manager-intake/              # Structured req kickoff
│   ├── job-description-optimizer/          # JD bias removal & optimization
│   ├── interview-question-generator/       # Role-specific question creation
│   ├── interview-feedback/                 # Structured feedback collection
│   ├── reference-debrief/                  # Reference response analysis
│   ├── counter-offer-strategy/             # Competing offer scenario modeling
│   ├── rejection-communication/            # Stage-appropriate rejection messaging
│   ├── employer-branding/                  # "Why PlayOn" messaging
│   ├── requisition-approval/               # Req approval workflow
│   ├── internal-mobility/                  # Internal candidate matching
│   ├── onboarding-workflow/                # 90-day onboarding automation
│   ├── offboarding-workflow/               # Exit process management
│   ├── employee-sentiment/                 # Pulse surveys & satisfaction
│   ├── succession-planning/                # Flight risk & successor mapping
│   ├── workforce-planning/                 # Headcount forecasting
│   ├── skills-gap-analysis/                # Team capability assessment
│   └── compliance-reporting/               # EEO, OFCCP, regulatory reports
│
├── tools/                                  # 22 integrations
│   ├── lever-ats.yaml                      # Lever ATS (bidirectional)
│   ├── ats-abstraction.yaml                # Multi-ATS adapter (Lever/Greenhouse/Workable)
│   ├── candidate-emailer.yaml              # Template-based email outreach
│   ├── calendar-booker.yaml                # Interview scheduling
│   ├── ai-caller.yaml                      # AI voice pre-screening calls
│   ├── video-interview.yaml                # Zoom/Teams management
│   ├── skills-assessment.yaml              # HackerRank/Codility/CodeSignal
│   ├── linkedin-recruiter.yaml             # LinkedIn Recruiter Seat API
│   ├── background-check.yaml               # Criminal, education, employment checks
│   ├── reference-checker.yaml              # Automated reference collection
│   ├── docusign-integration.yaml           # Electronic document signing
│   ├── job-board-poster.yaml               # Multi-board job posting
│   ├── talent-crm.yaml                     # Passive candidate nurturing
│   ├── hris-integration.yaml               # Workday/BambooHR/ADP
│   ├── payroll-connector.yaml              # ADP/Gusto payroll sync
│   ├── lms-integration.yaml                # Learning management
│   ├── immigration-tracker.yaml            # Visa & work authorization
│   ├── sso-provisioner.yaml                # Okta/Azure AD access management
│   ├── expense-tracker.yaml                # Recruiting spend & ROI tracking
│   ├── slack-notifier.yaml                 # Notifications & approvals
│   ├── survey-engine.yaml                  # Employee surveys
│   └── analytics-dashboard.yaml            # Hiring & workforce metrics
│
├── hooks/                                  # 8 lifecycle event triggers
│   ├── on-high-score-candidate.md          # Alert on 90+ match score
│   ├── on-pipeline-stall.md                # Detect SLA breaches
│   ├── on-offer-response.md                # Handle accept/decline/negotiate
│   ├── on-candidate-withdrawal.md          # Log reason, advance backup, CRM add
│   ├── on-visa-expiry.md                   # Immigration deadline alerts
│   ├── on-sentiment-drop.md                # Department mood change alerts
│   ├── on-new-hire-anniversary.md          # 30/60/90/365-day milestone triggers
│   └── on-requisition-aging.md             # 30/45/60-day escalation tiers
│
├── workflows/                              # 6 end-to-end processes
│   ├── new-requisition.md                  # Req → Post → Screen → Interview → Hire → Onboard
│   ├── offer-to-hire.md                    # Offer → Sign → Background → Payroll → Onboard
│   ├── quarterly-review-cycle.md           # Survey → Analysis → Reviews → Reporting
│   ├── employee-transfer.md                # Internal mobility execution
│   ├── compensation-review-cycle.md        # Annual merit/equity/promotion cycle
│   └── emergency-backfill.md               # Fast-track critical role replacement (~15 days)
│
├── knowledge/                              # 11 reference documents
│   ├── index.yaml
│   ├── playon-context.md                   # Company & team context
│   ├── hiring-sla.md                       # Pipeline stage targets
│   ├── scoring-rubric.md                   # Match score criteria
│   ├── interview-question-bank.md          # Structured question library
│   ├── interview-panel-matrix.md           # Who interviews for what
│   ├── benefits-guide.md                   # Full benefits package
│   ├── employee-handbook.md                # HR policies reference
│   ├── compensation-bands.md               # Pay bands by level & location
│   ├── rejection-templates.md              # Pre-approved rejection messages by stage
│   ├── vendor-contacts.md                  # Background check, immigration, agencies
│   └── compliance-calendar.md              # Filing deadlines & state requirements
│
├── config/                                 # Environment configuration
│   └── environments.yaml                   # Production, sandbox (demo), development
│
├── compliance/                             # Compliance artifacts & audit trail
│   └── README.md                           # Structure, retention policy, access control
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
| Hiring Manager Intake | Structured kickoff extracts must-haves, hidden preferences, team dynamics |
| Internal Mobility | Match existing employees to open roles before external posting |
| Candidate Experience | Stage-appropriate rejections, NPS, status updates — nobody gets ghosted |
| Counter-Offer Modeling | Data-driven scenarios when candidates have competing offers |
| Succession Planning | Flight risk identification, internal successor mapping, proactive pipeline |
| Human-in-the-Loop | Escalates uncertain decisions to recruiters instead of auto-deciding |
| ATS-Native | Bidirectional Lever integration with multi-ATS abstraction layer |
| Full Pipeline | Intake → Source → Screen → Assess → Interview → Feedback → Offer → Background → Onboard |
| Lifecycle Hooks | 8 auto-triggers: high scores, stalls, withdrawals, offers, visa, sentiment, aging, anniversaries |
| End-to-End Workflows | 6 process maps from requisition to hire, transfer, comp review, and emergency backfill |
| Environment Configs | Production, sandbox (for March 24 demo), and development modes |
| Compliance | EEO-1, OFCCP, adverse impact, pay equity, FCRA, state-specific requirements |
| Expense Tracking | Cost-per-hire, channel ROI, recruiting budget utilization |
| Workforce Intelligence | Headcount forecasting, skills gap analysis, sentiment, attrition modeling |

## Built with

[gitagent](https://github.com/open-gitagent/gitagent) — a git-native, framework-agnostic open standard for AI agents.
