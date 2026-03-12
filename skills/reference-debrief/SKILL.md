---
name: reference-debrief
description: Structured analysis of reference check responses — flags inconsistencies, summarizes themes, and produces hiring-ready reports
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Reference Debrief

## Instructions

Analyze reference check responses and produce actionable summaries for hiring decisions.

### Analysis Framework

#### 1. Response Validation
- Did all requested references respond? (minimum 2 of 3 required)
- What is each reference's relationship to the candidate? (manager > peer > report)
- How long did they work together? (>1 year = strong signal, <6 months = weaker)
- Response time as a signal (immediate = strong relationship, delayed/reluctant = flag)

#### 2. Consistency Check
Cross-reference responses against resume claims:
- **Title verification**: Does the reference confirm the candidate's stated title?
- **Tenure verification**: Do dates align with resume?
- **Responsibility scope**: Does described scope match resume claims?
- **Performance claims**: Do references support achievements listed on resume?

Flag any discrepancies as:
- `[MINOR]` — slight differences in dates or title (common, usually benign)
- `[MODERATE]` — scope or responsibility mismatch (investigate further)
- `[CRITICAL]` — fabricated role, inflated seniority, or terminated vs. resigned

#### 3. Theme Extraction
Across all references, identify:
- **Top 3 strengths** (mentioned by 2+ references)
- **Top concerns** (even subtle language: "he's great *when focused*" = focus issues)
- **Work style signals** (independent vs. collaborative, fast vs. thorough)
- **Management style** (for leadership roles)
- **Growth trajectory** (improving, plateauing, declining)

#### 4. Red Flag Detection
- Reference refuses to answer specific questions
- "I can only confirm dates of employment" (company policy or evasion?)
- Lukewarm language: "adequate", "satisfactory", "met expectations"
- Hesitation or qualifiers: "usually", "most of the time", "in the right environment"
- Reference was not actually a direct manager despite being listed as one

### Output Format

```
## Reference Debrief — [Candidate Name]
Role: [Title]
References Completed: [X] of [Y]

### Summary
Overall Signal: [Strong Positive / Positive / Mixed / Concerning]

### Consistency Check
| Claim | Resume | Reference 1 | Reference 2 | Status |
|-------|--------|-------------|-------------|--------|
| Title | Sr. Engineer | Confirmed | Confirmed | ✓ |
| Tenure | 3 years | 2.5 years | — | [MINOR] |

### Strengths (Consensus)
1. [Strength] — cited by [N] references
2. [Strength] — cited by [N] references

### Concerns
1. [Concern] — [specific language from reference]

### Red Flags
- [Any flags, or "None detected"]

### Recommendation
[Proceed to offer / Proceed with noted concerns / Additional reference needed / Escalate to HR]
```

### Rules
- Never contact references not provided by the candidate
- All reference data is confidential — shared only with hiring team
- If all references are peers (no managers), flag and request a manager reference
- Reference checks cannot be the sole basis for rejection — they inform, not decide
