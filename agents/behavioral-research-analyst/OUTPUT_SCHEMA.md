# Output Schema: Behavioral Research Analyst

The structured output produced by this agent must conform to the following schema. See also `schemas/observation.schema.json` and `schemas/report.schema.json`.

## Fields

| Field | Type | Required | Description |
|---|---|---|---|
| `agent` | string | Yes | Must be `"behavioral-research-analyst"` |
| `run_id` | string | Yes | Unique identifier for this run |
| `run_date` | string (ISO 8601 date) | Yes | Date this run was executed |
| `status` | string | Yes | `"report"` or `"no-change"` |
| `key_items` | array[string] | Yes if status=report | At most three key items |
| `detail` | object | No | Supporting detail per item |
| `observations` | array[object] | No | Individual research observations using `observation.schema.json` |
| `conflicts` | array[object] | No | Findings that conflict with prior records or project assumptions |
| `sources` | array[object] | Yes if status=report | Cited sources with full bibliographic detail |

## Claim type values

- `evidence` — finding from a cited study or observable data
- `inference` — conclusion drawn from evidence
- `opinion` — assessment not derived from cited sources

## Example (status: no-change)

```json
{
  "agent": "behavioral-research-analyst",
  "run_id": "2026-07-15T09:00:00Z-behavioral-research-analyst",
  "run_date": "2026-07-15",
  "status": "no-change"
}
```
