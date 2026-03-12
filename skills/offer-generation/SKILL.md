---
name: offer-generation
description: Drafts offer letters with compensation details, benefits summary, and start date coordination
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Offer Generation

## Instructions

Generate offer letter drafts for approved candidates with all compensation and benefits details.

### Required Inputs
- Candidate name and role title
- Approved compensation (base, bonus, equity if applicable)
- Start date (proposed)
- Reporting manager
- Work location / remote policy
- Benefits tier

### Offer Letter Sections
1. **Welcome & Role** — Title, department, reporting structure
2. **Compensation** — Base salary, bonus structure, equity (if applicable)
3. **Benefits Summary** — Health, dental, vision, 401k match, PTO policy
4. **Start Date & Onboarding** — Proposed start date, first-week schedule
5. **Contingencies** — Background check, reference check, I-9 verification
6. **Response Deadline** — Standard 5 business days

### Process
1. Pull approved compensation from hiring manager sign-off
2. Populate offer template with candidate and role details
3. Generate benefits summary based on role level
4. Route draft to HR for legal review
5. After HR approval, send via DocuSign integration
6. Track response — accepted, negotiating, declined

### Rules
- Never send an offer without HR legal review
- All compensation must be within approved range (or have exception approval documented)
- Include at-will employment language per state requirements
- Offer letters expire after 5 business days unless extended by HR
