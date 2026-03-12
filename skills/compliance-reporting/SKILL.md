---
name: compliance-reporting
description: Generates EEO, OFCCP, and hiring compliance reports for regulatory requirements
license: MIT
allowed-tools: Read Grep Glob
metadata:
  author: playon-sports
  version: "1.0.0"
  category: compliance
---

# Compliance Reporting

## Instructions

Generate required compliance reports for hiring and employment regulations.

### Report Types

#### EEO-1 Report (Annual)
- Workforce demographic data by job category
- Required for employers with 100+ employees
- Deadline: Typically March 31
- Data: race/ethnicity, gender by EEO-1 job categories

#### OFCCP Compliance (Federal Contractors)
- Applicant flow logs with disposition reasons
- Adverse impact analysis for each selection stage
- Good faith effort documentation
- Internet applicant tracking

#### State-Specific Requirements
- Pay transparency compliance (CO, CA, NY, WA)
- Ban-the-box compliance (criminal history inquiry timing)
- Salary history ban compliance

### Applicant Flow Log
Track for every requisition:
```
Stage          | Applied | Advanced | Rate  | Adverse Impact?
Application    | 2500    | —        | —     | —
Screen         | 2500    | 800      | 32%   | Check
Pre-Screen     | 800     | 200      | 25%   | Check
Interview      | 200     | 50       | 25%   | Check
Offer          | 50      | 10       | 20%   | Check
Hire           | 10      | 8        | 80%   | Check
```

### Adverse Impact Analysis
- Use 4/5ths (80%) rule as initial screen
- If selection rate for any group < 80% of highest group: flag for review
- Document legitimate business justification for any disparities
- Recommend corrective actions if patterns persist

### Rules
- All compliance data is confidential — restricted to HR leadership and legal
- Reports must be generated from verified ATS data, not estimates
- Retain applicant flow data for minimum 3 years
- Never alter historical data — corrections must be documented
