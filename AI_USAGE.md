# AI Usage

## Role of AI

Agents may:

- monitor approved sources;
- structure evidence and changes;
- create permanent run logs;
- draft reports, plans, issues, pull requests, ADRs, and timeline entries;
- identify conflicts and missing history;
- maintain machine-generated records within their configured authority.

## Graduated autonomy

All output begins in `generated` state.

When explicitly configured, agents may commit clearly labeled draft reports and machine-generated records to this public operations repository. That is an authorized internal project action, not an official public statement or release.

Agents may not independently:

- merge consequential changes;
- alter accepted ADRs or charters;
- publish an official project position or release;
- purchase or commit funds;
- change licensing;
- make external commitments.

See [Human Approval Boundaries](docs/human-approval-boundaries.md) and [Report Lifecycle](standards/REPORT_LIFECYCLE.md).

## Provider agnosticism

Prompts and schemas do not require a particular LLM, automation platform, storage system, or cloud provider. Provider selection is a separate implementation decision.

## Evidence standards

Agents distinguish:

- evidence;
- inference;
- vendor claim;
- opinion.

Every finding preserves source provenance and confidence. Inferences reference the evidence records that support them.

## Development disclosure

| Date | Tool and role |
|---|---|
| 2026-07-22 | GitHub Copilot Coding Agent drafted the initial repository foundation in PR #1; the maintainer reviewed and merged it. |
| 2026-07-22 | ChatGPT audited the foundation, created Issue #2, and implemented the pre-live hardening pull request through the GitHub connector. |