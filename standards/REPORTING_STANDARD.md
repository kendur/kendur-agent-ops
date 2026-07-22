# Reporting Standard

All agent reports must follow this standard. See also `docs/communication-standard.md` for the three-item rule.

## Required report sections

### 1. Key Items (required if status is "report")

At most three items. Each is one sentence or a short phrase. No supporting detail in this section.

### 2. Detail (optional)

Supporting information for each key item. Organized by item number or topic. May link to separate documents for very long content.

### 3. Sources (required if status is "report")

A list of all cited sources. Each source follows the schema in `standards/SOURCE_POLICY.md`.

## Status values

| Status | Meaning |
|---|---|
| `report` | The agent has meaningful findings to share |
| `no-change` | Nothing meaningful changed since the last run |
| `escalation` | A finding requires urgent human attention; follow `ESCALATION_RULES.md` |

## No-change behavior

When status is `no-change`, the agent produces only the minimal record:

```json
{
  "agent": "agent-name",
  "run_id": "...",
  "run_date": "YYYY-MM-DD",
  "status": "no-change"
}
```

No notification is sent for a no-change result.

## Avoiding drift

Agents must not repeat information that has not changed since the last report. If an item was reported in the last run and has not changed, omit it unless it is still actively significant and the maintainer needs to be reminded.

## Tone

Plain language. No filler phrases ("it is important to note that…", "in conclusion…"). State the finding, state the source, move on.
