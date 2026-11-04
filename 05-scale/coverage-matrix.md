# Module 5 · Coverage Matrix · Competitor Signal Tracker

## Coverage Row

| Product | Hallucination Rate | Fairness | Latency | UX Trust | Robustness |
|---|---|---|---|---|---|
| Competitor Signal Tracker | ❌ Gap | ❌ Gap | ✅ Covered | ✅ Covered | ⚠️ Partial |

## What Runs Today

- A timer alerts if the nightly scoring run takes more than 2 hours.
- A style check flags summaries written in a casual or alarmist tone before they reach the sales team.

## Accepted Gap

**Fairness.** We accept this gap as news and social posts can be skewed towards a customer in certain geo or customer group so there is a high chance that it could be part of normal product behavior. 

We’ll look again: If I have repeated and high error rate in future I would like to revisit. In the meantime, I will keep doing spot checks with 20 items a month, sampled by region and language, with a set of 5% error threshold.

## Critical Gap

We’ve flagged Hallucination Rate as the most critical gap for Competitor Signal Tracker because Hallucination Rate is our most critical gap, because a wrong claim about a competitor can mislead sales and skew product strategy. To close it, an LLM judge or entailment model will trace every claim in each summary back to its source article. We’ll calibrate the judge on a golden set of 200 labeled articles, then run it automatically on 10% of each night’s output, with a weekly human review. An alert fires if more than 2% of claims are unsupported. PM owns this, with a target date of  12/05. Once we have 30 days of nightly runs and 90%+ agreement between the judge and human labels, we’ll mark it Covered.

## After the Pressure Test

Asked for measurable data for error rate and make it a plan with owner and dates

