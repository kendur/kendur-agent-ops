# Evidence Schema

This document defines how evidence is structured when agents record observations or findings.

## Evidence object

```json
{
  "claim": "string — the specific assertion being made",
  "claim_type": "evidence | inference | vendor-claim | opinion",
  "confidence": "high | medium | low",
  "source": {
    "url": "string",
    "title": "string",
    "access_date": "YYYY-MM-DD",
    "author": "string or null",
    "publication": "string or null"
  },
  "conflicts_with": ["reference to prior finding id or null"]
}
```

## Claim types

| Type | When to use |
|---|---|
| `evidence` | The claim is directly supported by the cited source |
| `inference` | The claim is a conclusion drawn from one or more evidence items |
| `vendor-claim` | The claim comes from the vendor of the product being discussed |
| `opinion` | The claim is an assessment not supported by cited evidence |

## Confidence levels

| Level | When to use |
|---|---|
| `high` | Multiple independent sources corroborate the claim |
| `medium` | A single credible source supports the claim |
| `low` | The source is indirect, secondhand, or uncertain |

## Inferences

When claim_type is `inference`, the agent must identify which evidence items support the inference. Inferences must be labeled as inferences in the report and must not be presented as if they were direct observations or findings from a cited source.

## Conflicts

When a claim conflicts with a prior finding, the `conflicts_with` field must reference the prior finding. The conflict must be surfaced in the report.
