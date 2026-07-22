# Output Schema: Capture Ecosystem Analyst

The structured output produced by this agent must conform to the following schema. See also `schemas/observation.schema.json` and `schemas/report.schema.json`.

## Fields

| Field | Type | Required | Description |
|---|---|---|---|
| `agent` | string | Yes | Must be `"capture-ecosystem-analyst"` |
| `run_id` | string | Yes | Unique identifier for this run |
| `run_date` | string (ISO 8601 date) | Yes | Date this run was executed |
| `status` | string | Yes | `"report"` or `"no-change"` |
| `key_items` | array[string] | Yes if status=report | At most three key items |
| `detail` | object | No | Supporting detail per item |
| `observations` | array[object] | No | Individual tool/service observations using `observation.schema.json` |
| `sources` | array[object] | Yes if status=report | Cited sources with URL, access date, and claim type |

## Claim type values

- `evidence` — observable data with a cited source
- `inference` — conclusion drawn from evidence
- `vendor-claim` — vendor's statement about their own product
- `opinion` — assessment not derived from cited sources

## Example (status: no-change)

```json
{
  "agent": "capture-ecosystem-analyst",
  "run_id": "2026-07-15T09:00:00Z-capture-ecosystem-analyst",
  "run_date": "2026-07-15",
  "status": "no-change"
}
```
