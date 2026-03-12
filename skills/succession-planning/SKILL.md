---
name: succession-planning
description: Identifies flight risks in critical roles, maps internal successors, and triggers proactive sourcing for high-risk positions
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: hr-operations
---

# Succession Planning

## Instructions

Proactively plan for leadership and critical role transitions before they become emergencies.

### Critical Role Identification

A role is "critical" if it meets 2+ of these criteria:
- Specialized knowledge that would take 6+ months to replace
- Direct revenue impact (client-facing, revenue-generating)
- Team/org dependency (10+ people report up through this role)
- Regulatory/compliance requirement (must have a named individual)
- Single point of failure (only person who knows X system/process)

### Flight Risk Assessment

Score each critical role holder on departure likelihood:

| Signal | Weight | Source |
|--------|--------|--------|
| Tenure in role >3 years (no promotion) | High | HRIS |
| Declining sentiment scores | High | Pulse surveys |
| Below-market compensation | Medium | Comp benchmarking |
| Manager relationship issues | Medium | 360 feedback |
| LinkedIn activity spike | Medium | Recruiter intelligence |
| Passed over for promotion | High | Review cycle data |
| Life event signals (relocation, etc.) | Low | Manager 1:1 notes |
| Industry demand for their skills | Medium | Market data |

Risk levels:
- **Critical**: 3+ high signals → immediate action
- **Elevated**: 2 high or 3+ medium → plan within 30 days
- **Watch**: 1 high or 2 medium → quarterly review
- **Low**: No significant signals → annual review

### Successor Mapping

For each critical role, identify:

#### Ready Now (can step in within 2 weeks)
- Internal candidate who has 80%+ of required skills
- Has been cross-trained or acted as backup
- Manager endorsement

#### Ready in 6-12 Months (with development)
- Internal candidate with 60-80% of skills
- Development plan: specific training, stretch assignments, mentoring
- Timeline to readiness

#### External Pipeline (no internal successor)
- Begin passive sourcing via talent CRM
- Build relationship with 2-3 external candidates
- Keep warm through employer branding touchpoints

### Output Format

```
## Succession Plan — [Quarter/Year]

### Critical Roles Summary
Total critical roles: [N]
With ready-now successor: [N] ([X]%)
With development successor: [N] ([X]%)
No successor identified: [N] ([X]%) ← priority action

### Flight Risk Dashboard
| Role | Incumbent | Risk Level | Successor Status | Action |
|------|-----------|-----------|-----------------|--------|
| VP Eng | [Name] | Elevated | Ready in 6mo | Accelerate [Successor] development |
| Sr. Architect | [Name] | Critical | None | Begin external sourcing immediately |

### Immediate Actions Required
1. [Specific action for highest-risk role]
2. [Specific action for gap with no successor]

### Development Plans in Progress
| Successor | Target Role | Gap | Training Plan | ETA |
|-----------|-------------|-----|--------------|-----|
| [Name] | [Role] | [Skill] | [Plan] | [Date] |
```

### Cadence
- **Quarterly**: Review all critical roles and flight risk signals
- **Monthly**: Check-in on active development plans
- **Immediately**: When a critical role holder gives notice, activate succession plan
- **Annually**: Full succession planning review with C-suite

### Rules
- Succession plans are confidential — shared only with HR leadership and C-suite
- Never tell an employee they are "on the succession plan" without explicit approval
- Flight risk data is directional, not deterministic — never confront an employee based solely on signals
- Development plans must have the successor's buy-in (they need to want the path)
- External pipeline building is ongoing, not reactive — start before you need it
