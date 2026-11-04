# Module 5 · Eval Budget · Ascend IQ

**Quarterly budget cap:** $200,000
**Online eval spend:** $150,000 (2 of at most 3 online evals)

## Budget

| Failure | Trust metric | Risk | Level | Cost |
| --- | --- | :---: | :---: | ---: |
| Data Fabrication | Hallucination Rate | P0 | Online eval | $85,000 |
| Context Specificity | Robustness | P1 | Periodic audit | $7,000 |
| Overconfident Tone | UX Trust | P1 | Online eval | $65,000 |
| Data Bias | Fairness | P2 | Periodic audit | $5,500 |
| Slow Answers | Latency | P3 | Code-based check | $1,250 |

## Downgrades

### Periodic audit · Context Specificity (Robustness · P1)
- **Cheaper check:** I will use a weekly check on 100 samples
- **Why it’s enough:** Its easier to catch with periodic audit as we can see if summary is accurate or not based on new reviews and trend of rating 

### Periodic audit · Data Bias (Fairness · P2)
- **Cheaper check:** I will run a weekly check on 100 questions per week
- **Why it’s enough:** It would be easier to check as I can compare if the reviews are skewed by US customers as compared to APAC 

### Code-based check · Slow Answers (Latency · P3)
- **Cheaper check:** Add latency monitoring (APM alerts on p95/p99, my estimate)
- **Why it’s enough:** A trace records the real milliseconds for every request. APM stack already collects this data. A judge’s cost grows with every request it scores. An alert on p95 or p99 fires within minutes. An eval pipeline adds its own delay.

