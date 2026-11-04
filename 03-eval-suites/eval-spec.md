# Eval Spec · Ascend IQ

# Eval Spec · Old Pricing (#HALLUCINATION), an output risk

| Part | Spec |
|---|---|
| Target risk | Old Pricing (#HALLUCINATION), an output risk |
| Evaluator | The rule check from Lab 1 |
| Threshold | Correct amount of $59/month. Supported by: the rule check caught 1 of 1, the safety rule caught 0 of 1, the judge caught 1 of 1 |
| Business stakes | This can lead to financial loss and can also cause trust issues with customers |
| Owner | PM |

## Messages

**Engineering · acceptance criteria:** Using the rule check from Lab 1, an answer passes if every price it states for the plan is exactly $59/month, or if it states no price at all. It fails if it states any other dollar amount or billing period for the plan, and a failing answer is blocked before it reaches the user.

**Design · what the user sees:** When the check blocks an answer, the user never sees the blocked text or an error. They see a short, plain reply that the plan costs $59/month, with a way to ask a follow-up question.

**Leadership · risk and return:** This check stops the assistant from quoting old pricing, which can lead to financial loss and trust issues with customers. It is a simple rule check that caught 1 of 1 in testing, while the safety rule caught 0 of 1, so it is low cost to run and the right tool for this risk.
