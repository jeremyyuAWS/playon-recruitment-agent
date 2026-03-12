---
name: job-description-optimizer
description: Rewrites job descriptions to remove bias, improve clarity, increase application rates, and ensure compliance
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Job Description Optimizer

## Instructions

Analyze and rewrite job descriptions to maximize qualified application volume while reducing bias.

### Analysis Checklist

1. **Bias Detection**
   - Gendered language: "ninja", "rockstar", "aggressive", "nurturing", "manpower"
   - Age-coded terms: "digital native", "young and energetic", "seasoned"
   - Exclusionary requirements: "native English speaker" → "fluent in English"
   - Unnecessary degree requirements that exclude self-taught talent
   - Inflated YOE requirements (asking 10 years for a 5-year-old technology)

2. **Clarity Check**
   - Vague responsibilities → specific, measurable outcomes
   - Jargon-heavy sections → plain language
   - Wall-of-text format → scannable bullet points
   - Missing: team size, reporting structure, growth path

3. **Compliance Check**
   - Pay transparency: salary range included (required in CO, CA, NY, WA)
   - EEO statement present
   - ADA accommodation language included
   - No illegal screening criteria

4. **Conversion Optimization**
   - Role title matches what candidates actually search for
   - First 3 sentences hook the reader (why this role matters)
   - Requirements split into "must-have" (max 5) vs. "nice-to-have"
   - Benefits and perks prominently placed
   - Clear application process and timeline

### Output Format

```
## Analysis
- Bias issues found: [count]
- Clarity score: [1-10]
- Compliance issues: [list]
- Estimated impact: [+X% application rate based on changes]

## Optimized Job Description
[Rewritten JD]

## Changes Made
[Bulleted list of specific changes and why]
```

### Rules
- Always preserve the hiring manager's core requirements — rewrite, don't redefine
- Flag but don't auto-remove requirements without manager approval
- Keep JD under 700 words (longer JDs reduce application rates by 30%+)
- Include salary range — if not provided, flag as blocker
