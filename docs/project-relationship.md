# Project Relationship

## Executive Support System

Canonical product repository: <https://github.com/kendur/kendur-executive-support>

The Executive Support System is the first bounded and potentially monetizable module on the path toward Nexus. It is Notion-centered, AI-optional, and capture-source agnostic.

The product repository is the source of truth for:

- product vision and scope;
- product decisions and ADRs;
- product history and roadmap;
- Notion, capture, automation, AI, licensing, and service design.

## KenDur Agent Operations

This repository governs the AI team supporting the product. It is the source of truth for:

- agent roles and charters;
- prompts and output contracts;
- evidence, confidence, reporting, and escalation standards;
- agent-run history;
- agent-governance ADRs;
- generated research and market reports.

## Cross-repository history

The Project Historian reviews both repositories. It proposes links, timeline entries, and ADRs in the repository that owns the decision.

Records should be cross-referenced rather than copied and silently edited in two places. Product decisions belong in the product repository; agent-governance decisions belong here.

## Nexus

Nexus is the broader long-term system. The Executive Support System must remain useful independently while preserving integration points for later Nexus modules.

```text
Nexus
  └── Executive Support System
        ├── Product source of truth: kendur-executive-support
        └── Agent governance: kendur-agent-ops
              ├── Project Historian and Decision Steward
              ├── Capture Ecosystem Analyst
              ├── Behavioral Research Analyst
              └── Market and Community Analyst
```