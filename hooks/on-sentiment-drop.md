# Hook: Sentiment Drop Alert

## Trigger
When a department's pulse survey score drops by 1.0+ points in a single period, or when an individual's score drops below 4/10.

## Action

### Department-Level Drop
1. Alert HR Business Partner and department head
2. Generate sentiment trend analysis (last 4 periods)
3. Identify top contributing factors from survey responses
4. Recommend intervention (skip-level 1:1s, team retrospective, manager coaching)

### Individual Risk Signal
1. Flag to HR (aggregate signal only — never name the individual from anonymous survey)
2. Suggest manager check-in for the team broadly
3. If combined with other signals (performance decline, PTO spike), flag retention risk

## Message Template
```
:chart_with_downwards_trend: Sentiment Alert — [Department]

Current Score: [X.X] / 10
Previous Score: [Y.Y] / 10
Change: -[Z.Z]
Top Concern: [Theme from responses]
Recommended Action: [Specific intervention]
```
