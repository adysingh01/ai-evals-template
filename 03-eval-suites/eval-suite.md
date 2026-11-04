# Eval Suite · Old Pricing

## P0 failure (carried from Module 2)

**Failure:** Old Pricing (#HALLUCINATION). Reports outdated pricing despite the reference stating"New Price (update yesterday): $59.mo"

- **Row:** 1
- **Query:** What is InsightFlow's pricing for Enterprise?
- **Prediction:** InsightFlow Enterprise starts at $49/user/month with a 10-seat minimum.
- **Reference:** Source: Pricing Page (Cached). Old Price: $49/mo. New Price (Updated yesterday): $59/mo.

## The three checks

**Rule check.** Looks at: question, answer, reference. Passes when: New price $59/month Fails when: any other price would 

**Safety rule.** Looks at: question, answer, reference. Passes when: No discount or escalation Fails when: Any discount offers

**Judge.** Looks at: question, answer, reference. Passes when: Correct price which is $59/month in this case Fails when: any other price would 

## Results on the 20 Ascend IQ answers

| Check | Caught | Missed (rows) | False alarms (rows) | My P0 row |
|---|---|---|---|---|
| Rule check | 1 of 1 | None | None | Caught it |
| Safety rule | 0 of 1 | 1 | None | Missed it |
| Judge | 1 of 1 | None | None | Caught it |

**Judge on my P0 row:** Quotes the old $49/user/month price instead of the updated $59/mo.

## Where the failure was caught

The failure was caught during the evals and it tells me my agent was providing old pricing

## What I'd ship next

Would add price check rule as code based eval

## Row by row

| Row | Rule | Safety | Judge | Judge reason |
|---|---|---|---|---|
| 1 | 0 | 1 | 0 | Quotes the old $49/user/month price instead of the updated $59/mo. |
| 2 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 3 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 4 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 5 | 1 | 1 | 1 | Mentions pricing relative to market but quotes no price figure. |
| 6 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 7 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 8 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 9 | 1 | 1 | 1 | $45M is a funding amount, not a product price. |
| 10 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 11 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 12 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 13 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 14 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 15 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 16 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 17 | 1 | 1 | 1 | References the Enterprise tier but quotes no price. |
| 18 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 19 | 1 | 1 | 1 | No price stated, so no incorrect price is given. |
| 20 | 1 | 1 | 1 | ~$1B is a company valuation, not a product price. |
