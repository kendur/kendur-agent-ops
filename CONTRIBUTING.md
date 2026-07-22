# Contributing

Thank you for your interest in contributing to KenDur Agent Operations.

## What belongs here

This repository is documentation-first. Contributions should be:

- Clarifications or corrections to existing documents
- New agent charters or role definitions approved through an ADR
- Updated schemas or standards
- History records and decision records
- Issue templates or workflow improvements

**Do not add application code, production agent implementations, or database schemas here.**

## How to contribute

1. Open an issue using the appropriate template:
   - `agent-change.yml` — propose a change to an agent charter, prompt, or schema
   - `research-finding.yml` — submit a finding for review
   - `decision-proposal.yml` — propose a consequential decision for human review
2. For small corrections (typos, broken links), a pull request without an issue is fine.
3. For structural or policy changes, open a discussion or issue first.

## Pull request checklist

- [ ] Changes are limited to what the issue describes.
- [ ] No production code, credentials, or personal data is included.
- [ ] Historical records are appended, not overwritten.
- [ ] If a new ADR is needed, it has been added to `docs/decisions/`.
- [ ] The PR description explains the reason for the change.

## Human approval

All changes to agent charters, operating principles, ADRs, or schemas require human review before merging. See [`docs/human-approval-boundaries.md`](docs/human-approval-boundaries.md).
