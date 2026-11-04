# Module 4 · Launch Strategy · Ascend IQ Copilot

## 4.0 Release Criteria

| Gate | Failure | Metric | Threshold | Dataset | Method | Runs at |
|---|---|---|---|---|---|---|
| Hard | Old Pricing (#HALLUCINATION) | % of answers with correct price | Correct amount of $59/month | Ascend IQ golden set | Code-based check | Pull Request |
| Soft | Row 5 · Hallucination: lists an unconfirmed speaker as confirmed | Name and number of confirmed speakers | 100% | Ascend IQ golden set | Human review | Pull Request |
| Advisory | Row 17 · Tone: slang detected | % of responses with slang language | 90% | Ascend IQ golden set | LLM judge | Staging |

## CI Gate Request for Engineering

- **Hard gate · Old Pricing (#HALLUCINATION).** Check: the code-based check, run on the Ascend IQ golden set at Pull Request. Measures: % of answers with correct price. Passes when: Correct amount of $59/month. On a fail: block the merge.
- **Soft gate · Row 5 · Hallucination: lists an unconfirmed speaker as confirmed.** Check: the human review, run on the Ascend IQ golden set at Pull Request. Measures: Name and number of confirmed speakers. Passes when: 100%. On a fail: pause the release until the PM signs off on an override.
- **Advisory gate · Row 17 · Tone: slang detected.** Check: the LLM judge, run on the Ascend IQ golden set at Staging. Measures: % of responses with slang language. Passes when: 90%. On a fail: post a warning, and don't block.

## Mitigation Plan · Soft Gate

If our Soft gate fails I would recommend a soft launch with link to the event website
