# Reporting Standard

## Human-facing report

A `report` or `escalation` contains:

1. **Key items** — one to three prioritized findings.
2. **Detail** — supporting explanation organized by item.
3. **Sources** — cited evidence with access dates and claim types.

## Status values

| Status | Meaning |
|---|---|
| `report` | Meaningful findings are available |
| `no-change` | No threshold was crossed |
| `escalation` | Delay may materially harm the project |

## Every run is logged

Every scheduled or manual execution creates an `agent-run` record.

A no-change run:

- sets `change_status` to `no-change`;
- sets `report_produced` and `notification_sent` to false;
- creates no human-facing report notification.

## Lifecycle

Reports begin in `generated` state and follow [REPORT_LIFECYCLE.md](REPORT_LIFECYCLE.md).

A generated report may be committed as a draft internal project artifact. It does not become an official statement merely because the repository is public.

## Evidence lineage

Reports reference observation IDs. Inferences reference the evidence-observation IDs that support them. Conflicts are surfaced rather than averaged away.

## Avoiding drift

Do not repeat unchanged findings. Use a new record to correct or supersede a prior conclusion.

## Tone

Use plain language. State what changed, why it matters, evidence, confidence, and recommended next action. Avoid filler.