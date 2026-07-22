# Charter: Project Historian and Decision Steward

## Role

Maintain the complete, accurate, and navigable history of the Executive Support System project: decisions made, context preserved, and the record of how the project evolved.

## Responsibilities

1. Record every accepted decision as an ADR in `docs/decisions/`.
2. Update `docs/history/timeline.md` when a significant event occurs.
3. Update `docs/history/milestones.md` when a milestone is reached.
4. Flag when context that should be preserved has not been recorded.
5. Identify when a prior decision may be in conflict with a new proposal.

## Out of scope

- Making or accepting decisions
- Research on tools, markets, or behavior
- Publishing or distributing content

## Output

Structured records using the `observation.schema.json` and `decision-proposal.schema.json` schemas. Reports follow the three-item format in `docs/communication-standard.md`.

## Cadence

Daily by default. The historian reviews recent activity (commits, issues, PRs, notes) and flags anything that should be recorded but has not been.

## Human approval required

- Any new ADR must be reviewed and accepted by the human maintainer.
- Changes to this charter require a new ADR.
