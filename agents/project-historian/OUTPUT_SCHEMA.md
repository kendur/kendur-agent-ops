# Output Schema: Project Historian and Decision Steward

The structured output produced by this agent must conform to the following schema. See also `schemas/observation.schema.json` and `schemas/report.schema.json` for the base types.

## Fields

| Field | Type | Required | Description |
|---|---|---|---|
| `agent` | string | Yes | Must be `"project-historian"` |
| `run_id` | string | Yes | Unique identifier for this run (ISO 8601 timestamp + agent name) |
| `run_date` | string (ISO 8601 date) | Yes | Date this run was executed |
| `status` | string | Yes | `"report"` or `"no-change"` |
| `key_items` | array[string] | Yes if status=report | At most three key items; each a single sentence |
| `detail` | object | No | Supporting detail keyed by item number or topic |
| `proposed_adrs` | array[object] | No | Draft ADR records for human review |
| `proposed_timeline_entries` | array[object] | No | Proposed additions to `docs/history/timeline.md` |
| `conflicts_identified` | array[object] | No | Conflicts between recent activity and existing decisions |
| `sources` | array[object] | Yes if status=report | See `standards/SOURCE_POLICY.md` |

## Example (status: no-change)

```json
{
  "agent": "project-historian",
  "run_id": "2026-07-15T09:00:00Z-project-historian",
  "run_date": "2026-07-15",
  "status": "no-change"
}
```
