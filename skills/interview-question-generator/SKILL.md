---
name: interview-question-generator
description: Generates role-specific behavioral and technical interview questions calibrated to seniority level
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: talent-acquisition
---

# Interview Question Generator

## Instructions

Generate structured interview questions tailored to the specific role, level, and competencies being evaluated.

### Input Required
- Job description and title
- Seniority level (junior, mid, senior, staff, manager)
- Interview type (technical, behavioral, system design, hiring manager)
- Key competencies to evaluate (from job requirements)
- Interview duration (30, 45, 60 minutes)

### Question Types

#### Behavioral (STAR Format)
Structure: Situation → Task → Action → Result
- "Tell me about a time you [competency]. What was the situation, what did you do, and what was the outcome?"
- Generate 2-3 follow-up probes per question

#### Technical
- Calibrate to level: Junior = fundamentals, Mid = application, Senior = architecture, Staff = strategy
- Include expected answer benchmarks (what good/great/red-flag answers look like)
- Mix: 40% problem-solving, 30% domain knowledge, 30% system thinking

#### System Design (Senior+ only)
- Real-world scenario relevant to PlayOn's domain (sports tech, streaming, data)
- Expected discussion points at each level
- Time allocation: 5 min clarify → 10 min high-level → 15 min deep dive → 5 min tradeoffs

#### Culture & Values
- Align to PlayOn's values (teamwork, speed, fan experience)
- Avoid questions that test "culture fit" (homogeneity) — test "culture add" (what new perspectives they bring)

### Output Format

```
## Interview Guide: [Role Title] — [Interview Type]
Duration: [X] minutes
Interviewer: [Name/TBD]

### Competency 1: [Name]
**Q1:** [Question]
- Follow-up: [Probe]
- Follow-up: [Probe]
- Green flag: [What a strong answer includes]
- Red flag: [Warning signs]
Time: ~[X] minutes

### Competency 2: [Name]
...
```

### Rules
- Generate 4-6 questions per 60-minute interview (depth > breadth)
- Never include illegal questions (age, family, religion, disability, national origin)
- Include at least 1 "culture add" question per interview
- Provide scoring rubric (1-5) for each competency
- Rotate question bank — don't reuse exact questions across candidates for same role
