# ADR-0004: Human Maintainer Holds Final Approval

**Date:** 2026-07-22  
**Status:** Accepted

## Context

Agents are useful only when they can proactively prepare work. Requiring approval for every log, draft, or proposed plan creates unnecessary burden, while allowing consequential autonomous action creates accountability risk.

## Decision

The maintainer holds final approval over consequential decisions. Agents may perform explicitly configured routine, reversible project-preparation actions.

Agents may:

- append run logs and evidence;
- write generated-state reports;
- open draft issues and pull requests;
- propose plans, ADRs, and timeline entries.

Human approval is required before:

- merging consequential changes;
- accepting or superseding ADRs;
- changing charters, licensing, or project direction;
- publishing official statements or releases;
- spending money or making external commitments.

## Alternatives considered

- Human approval for every agent action
- Broad autonomous authority
- No formal boundary

## Consequences

- Routine operations can proceed without approval fatigue.
- Generated artifacts remain drafts until reviewed.
- Consequential accountability stays with the maintainer.
- Authority changes require a superseding ADR.