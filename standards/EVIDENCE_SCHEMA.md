# Evidence Schema

Each observation records one claim and one or more sources.

```json
{
  "observation_id": "stable-id",
  "claim": "specific assertion",
  "claim_type": "evidence | inference | vendor-claim | opinion",
  "confidence": "high | medium | low",
  "sources": [
    {
      "url": "https://example.com/source",
      "title": "Source title",
      "access_date": "YYYY-MM-DD",
      "claim_type": "evidence",
      "author": null,
      "publication": null
    }
  ],
  "supporting_evidence_ids": [],
  "conflicts_with": [],
  "lifecycle": "generated"
}
```

## Claim types

- `evidence` — directly supported by cited material or observable data;
- `inference` — a conclusion drawn from evidence;
- `vendor-claim` — a vendor statement about its own product;
- `opinion` — an assessment not represented as sourced fact.

## Lineage

An inference must reference at least one supporting evidence observation by ID. A conflict references the prior observation IDs it challenges.

Sources are retained with each observation so later reports can be reconstructed even when conclusions change.

## Confidence

Confidence reflects evidence quality and the uncertainty of the reasoning step. An inference does not automatically inherit the confidence of its sources.

## History

Corrections and reassessments create new observations. Prior records remain and may be superseded through lifecycle metadata.