# KenDur Agent Operations

Charters, operating rules, research workflows, and shared memory for the AI agents supporting the **Executive Support System**.

---

## Why an AI team?

Managing a project well requires continuous attention across several domains: market trends, user behavior, competing tools, and evolving product decisions. Doing this manually—especially while managing executive-function challenges such as rapid idea loss, context switching, and interrupted work—is not sustainable. A structured AI agent team captures and structures that attention so the human maintainer can focus on decisions rather than data gathering.

## What this repository controls

This repository defines:

- the roles, charters, and operating principles for each AI agent;
- the standards agents must follow when gathering, scoring, and reporting information;
- the schemas agents use to produce structured, consistent output;
- the decision record for all consequential choices about the agent team itself;
- the historical archive of how the project evolved.

**This repository does not contain production agent code, application logic, or database schemas.** It is a documentation-first foundation.

## The four initial agent roles

| Agent | Responsibility |
|---|---|
| **Project Historian and Decision Steward** | Records decisions, preserves context, maintains the historical record |
| **Capture Ecosystem Analyst** | Monitors tools and services for capturing thoughts and preserving context |
| **Behavioral Research Analyst** | Researches how people manage attention, interruptions, and knowledge work |
| **Market and Community Analyst** | Tracks market positioning, community signals, and comparable products |

See [`agents/TEAM_CHARTER.md`](agents/TEAM_CHARTER.md) for full role definitions.

## Communication rule: three key items

Every agent report leads with at most **three key items**. Supporting detail lives below or in a linked document. Agents remain silent when nothing meaningful changed.

See [`docs/communication-standard.md`](docs/communication-standard.md).

## Monitoring cadence

Daily monitoring is the initial default. Cadence is configurable per agent and per data source.

## Historical preservation

Scores, conclusions, and observations are never overwritten. Each run appends a new record. Source provenance is preserved alongside every finding.

See [`standards/HISTORICAL_DATA_POLICY.md`](standards/HISTORICAL_DATA_POLICY.md).

## Human approval boundaries

Agents may propose decisions, plans, and drafts. They may not independently publish, purchase, change the product charter, alter licensing, or accept any commitment on behalf of the project. A human maintainer holds final approval over all consequential decisions.

See [`docs/human-approval-boundaries.md`](docs/human-approval-boundaries.md).

## Relationship to the Executive Support System and Nexus

The **Executive Support System** is the first bounded and potentially monetizable module on the path toward Nexus. It is a Notion-centered, AI-optional product that helps users capture thoughts, preserve context, identify next actions, and recover from interruptions.

This repository governs the AI team that supports that project. It does not implement the product itself.

See [`docs/project-relationship.md`](docs/project-relationship.md).

---

## Repository layout

```
README.md               this file
ROADMAP.md              planned milestones and future work
CHANGELOG.md            notable changes to this repository
CONTRIBUTING.md         how to contribute
AI_USAGE.md             how AI is used in this project
SECURITY.md             reporting security concerns

docs/                   narrative documentation
  history/              origin story, timeline, milestones
  decisions/            architecture decision records (ADRs)

agents/                 per-agent charters, prompts, and output schemas
standards/              rules agents must follow
schemas/                JSON schemas for structured agent output
reports/                agent-generated reports (daily / monthly / quarterly)
data/                   reference data and examples
.github/                issue templates and PR template
```
