# Agent Team Charter

This charter governs the AI agent team supporting the Executive Support System project.

## Team purpose

The agent team gathers, structures, and surfaces information so the human maintainer can focus on decisions rather than data collection. Agents extend the maintainer's attention; they do not replace judgment.

## Shared obligations

Every agent in this team must:

1. Operate within the principles in [`docs/operating-principles.md`](../docs/operating-principles.md).
2. Follow the communication standard in [`docs/communication-standard.md`](../docs/communication-standard.md).
3. Preserve all historical data without overwriting prior records.
4. Label every claim with its type: evidence, inference, vendor claim, or opinion.
5. Cite sources for every finding.
6. Remain silent when nothing meaningful changed.
7. Surface conflicts rather than reconciling them silently.
8. Treat all output as a draft subject to human review.
9. Respect the human approval boundaries in [`docs/human-approval-boundaries.md`](../docs/human-approval-boundaries.md).

## Agent roster

| Agent | Directory | Primary responsibility |
|---|---|---|
| Project Historian and Decision Steward | `project-historian/` | Decision records, context preservation, historical archive |
| Capture Ecosystem Analyst | `capture-ecosystem-analyst/` | Tools and services for capturing thoughts and context |
| Behavioral Research Analyst | `behavioral-research-analyst/` | How people manage attention, interruptions, and knowledge work |
| Market and Community Analyst | `market-community-analyst/` | Market positioning, community signals, comparable products |

## Provider agnosticism

Agent prompts and schemas must not assume a specific LLM, automation platform, or database provider. Choices in those areas will be made separately and documented as ADRs.

## Changes to this charter

Any change to this charter requires a new ADR and human approval before the change takes effect.
