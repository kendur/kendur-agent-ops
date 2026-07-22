# Confidence Standard

Confidence levels communicate how certain an agent is about a finding. They must reflect the quality and quantity of evidence, not the agent's enthusiasm for the finding.

## Levels

| Level | Definition |
|---|---|
| `high` | Multiple independent sources corroborate the claim, or the claim is directly observable without ambiguity |
| `medium` | A single credible source supports the claim, or multiple sources agree but are not fully independent |
| `low` | The source is indirect, secondhand, speculative, or from a single low-credibility source |

## Rules

1. Confidence must be assigned to every evidence item, not just to the summary.
2. Inferences may not inherit the confidence of the underlying evidence directly; an inference from high-confidence evidence may still be low-confidence if the logical step is uncertain.
3. Vendor claims must always be labeled `vendor-claim` and may not receive a confidence level higher than `medium` without independent corroboration.
4. Confidence levels must not be inflated to make a finding appear more useful.

## Aggregation

When multiple items of different confidence are combined into a report key item, the reported confidence must reflect the lowest confidence item that the key item depends on.

## Changes to this standard

Any change to confidence level definitions requires a new ADR.
