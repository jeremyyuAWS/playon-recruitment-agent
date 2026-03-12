---
name: counter-offer-strategy
description: Models counter-offer scenarios when candidates receive competing offers — match, beat, or walk away with data-driven rationale
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Counter-Offer Strategy

## Instructions

When a candidate receives a competing offer or counters PlayOn's offer, model scenarios and recommend a strategy.

### Trigger Conditions
- Candidate discloses a competing offer
- Candidate counters PlayOn's offer with specific numbers
- Candidate requests time extension (often signals competing process)
- Recruiter intelligence suggests candidate is in multiple final rounds

### Data Collection
1. **PlayOn's current offer**: base, bonus, equity, benefits, title, growth path
2. **Competing offer** (as disclosed): base, bonus, equity, company, role
3. **Market data**: compensation-benchmarking skill output for this role
4. **Internal equity**: what comparable employees at PlayOn earn
5. **Candidate priority signals**: what matters most to them (comp, title, remote, growth)?
6. **Budget ceiling**: maximum approved compensation for this requisition

### Scenario Modeling

#### Scenario A: Match
```
Action: Match the competing offer on base + bonus
Cost: $[difference from current offer]
Risk: Low — candidate likely accepts
Concern: Internal equity compression if significantly above band
```

#### Scenario B: Beat
```
Action: Exceed competing offer by 5-10%
Cost: $[amount]
Risk: Low acceptance risk, but sets high anchor for future negotiations
Concern: Budget exception required if above approved range
```

#### Scenario C: Repackage
```
Action: Keep base similar, enhance other components
Options:
- Sign-on bonus ($X one-time)
- Accelerated review cycle (6 months vs. 12)
- Additional equity/RSU grant
- Title bump (if justified by scope)
- Remote flexibility
- Professional development budget increase
Cost: $[total incremental cost]
Risk: Medium — depends on candidate's priorities
```

#### Scenario D: Hold Firm
```
Action: Reiterate current offer's total value with detailed comparison
When: Competing offer is from a less stable company, different role scope,
      or candidate has shown strong preference for PlayOn
Risk: Candidate declines — advance backup candidate
Cost: $0 incremental, but potential $[cost-to-refill] if candidate walks
```

#### Scenario E: Walk Away
```
Action: Wish candidate well, add to talent CRM
When: Counter exceeds budget by >20%, internal equity would be severely
      impacted, or there's a strong backup candidate
Next steps: Advance #2 candidate, or restart search
```

### Decision Framework

```
                    ┌─ Within budget + no equity issues → Match or Beat
                    │
Competing offer ────┤─ Within budget + equity concerns → Repackage
received            │
                    ├─ Above budget by <15% → Repackage or seek exception
                    │
                    └─ Above budget by >15% → Hold Firm or Walk Away
```

### Output Format

```
## Counter-Offer Analysis — [Candidate Name]

### Current State
PlayOn Offer: $[base] + $[bonus] + $[equity] = $[total]
Competing Offer: $[base] + $[bonus] + $[equity] = $[total]
Gap: $[amount] ([X]%)

### Market Context
Role market 50th percentile: $[amount]
PlayOn offer percentile: [X]th
Competing offer percentile: [X]th

### Recommended Strategy: [Scenario Letter]
Rationale: [2-3 sentences]
Estimated cost: $[incremental]
Internal equity impact: [None / Minor / Significant]
Requires approval from: [Recruiter / HM / HR / VP]

### Talking Points for Recruiter
1. [Specific point to emphasize]
2. [Specific point to emphasize]
3. [What NOT to say]

### If Candidate Declines
Backup candidate: [Name, score]
Re-source needed: [Yes/No]
Add to CRM: [Yes, with notes]
```

### Rules
- Never pressure candidates or use manipulative tactics
- Never disparage the competing company or offer
- All counter-offers require hiring manager + HR approval before verbal communication
- Document everything — counter-offer conversations have legal implications
- If candidate accepts a counter from their current employer (not a new offer), do NOT counter again — the data shows 80% leave within 18 months anyway
