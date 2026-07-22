# Agent Output Schemas

These JSON Schema Draft-07 files are executable contracts for agent runs and artifacts.

| Schema | Purpose |
|---|---|
| `agent-run.schema.json` | Permanent record of every execution |
| `observation.schema.json` | Source-linked evidence, inference, vendor claim, or opinion |
| `report.schema.json` | Human-facing report, no-change result, or escalation |
| `decision-proposal.schema.json` | Agent-generated proposal awaiting human review |
| `product-score.schema.json` | Point-in-time capture-ecosystem assessment |

## Rules

- Validate generated JSON before storing or opening a draft pull request.
- `report` and `escalation` require key items and sources.
- `no-change` remains minimal and sends no notification.
- Agent-created decision proposals begin only in `proposed` / `generated` state.
- Inferences reference supporting evidence-observation IDs.
- Prior observations and product scores are never overwritten.
- Example records are in [`data/examples/`](../data/examples/).