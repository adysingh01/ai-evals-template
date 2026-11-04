# Module 4 · Launch Strategy · Ascend IQ Copilot

## 4.0 Release Criteria

| Severity | Failure | Metric | Threshold | Dataset | Method |
|---|---|---|---|---|---|
| Hard | Old Pricing (#HALLUCINATION) | % of answers with correct price | Correct amount of $59/month | Ascend IQ golden set | Code-based check |
| Soft | Row 5 · Hallucination: lists an unconfirmed speaker as confirmed | Name and number of confirmed speakers | 100% | Ascend IQ golden set | Human review |
| Advisory | Row 17 · Tone: slang detected | % of responses with slang language | 90% | Ascend IQ golden set | LLM judge |

## Mitigation Plan · Soft Gate

If our Soft gate fails I would recommend a soft launch with link to the event website
