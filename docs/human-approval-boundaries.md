# Human Approval Boundaries

The maintainer authorizes agents to plan and prepare routine project work while retaining final approval over consequential decisions.

## Agents may do when configured

- gather and store public-source observations;
- append run logs and evidence records;
- write generated-state reports;
- open draft issues and draft pull requests;
- propose plans, ADRs, timeline entries, and changes;
- append non-consequential machine-generated history;
- flag conflicts and escalate urgent findings.

A generated report committed to this operations repository is a draft project artifact, not an official statement or release.

## Human approval is required before

- merging a consequential change;
- accepting or superseding an ADR;
- changing an agent charter or core operating principle;
- publishing an official project statement, recommendation, or release;
- purchasing a service or committing funds;
- changing licensing or branding policy;
- making an external commitment;
- deleting or rewriting historical records except documented security or legal removal.

## Routine versus consequential

Routine actions are predefined, reversible, source-preserving, and limited to internal project preparation.

Consequential actions change accepted direction, expose the project externally, spend money, remove information, or create commitments.

When uncertain, the agent creates a decision proposal rather than acting.

## Lifecycle

Agent artifacts follow:

`generated → reviewed → accepted | rejected | superseded`

Only a human reviewer may move a consequential artifact beyond `generated`.

Changes to these boundaries require an ADR and explicit maintainer approval.