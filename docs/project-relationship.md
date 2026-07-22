# Project Relationship

## Executive Support System

The Executive Support System is the first bounded and potentially monetizable module on the path toward Nexus. It is defined by a focused scope:

- Notion-centered: Notion is the primary interface and data store for the initial version.
- AI-optional: the product functions without AI assistance; AI enhances but does not replace core functionality.
- Capture-focused: the central value proposition is capturing thoughts, preserving context, identifying next actions, and recovering from interruptions.

## This repository

This repository governs the AI agent team that supports the Executive Support System project. It does not contain the product itself. Its purpose is to define how agents research, monitor, report, and propose plans in service of that product.

## Nexus

Nexus is the broader system that the Executive Support System is a step toward. It is not defined here beyond its existence as a long-term destination. The Executive Support System must be a useful, self-contained product before Nexus work begins.

## Development history

The entire development process—from initial concept through operational decisions—must remain historically understandable. This repository is part of that record. Decisions made here are logged in `docs/decisions/`. Context about the project's origin is in `docs/history/`.

## Relationship diagram

```
Nexus (future)
  └── Executive Support System (current focus)
        └── KenDur Agent Operations (this repository)
              ├── Project Historian and Decision Steward
              ├── Capture Ecosystem Analyst
              ├── Behavioral Research Analyst
              └── Market and Community Analyst
```
