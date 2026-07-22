# ADR-0004: Human Maintainer Holds Final Approval

**Date:** 2026-07  
**Status:** Accepted

## Context

AI agents can produce useful drafts, proposals, and recommendations. Without a clear boundary, there is a risk that agent output is treated as a decision rather than a proposal, or that agents gradually accumulate scope they were not intended to have.

## Decision

The human maintainer holds final approval over all consequential decisions. Agents may propose but may not accept, publish, commit, or act on any consequential decision independently.

Consequential decisions include but are not limited to:

- Changes to the product charter or project direction
- Selection of an automation platform, LLM provider, or database
- Addition or removal of a license
- Publication of any content on behalf of the project
- Acceptance of any paid subscription or contract
- Merging changes to ADRs or operating principles

## Rationale

- AI output is a draft. Treating it as a decision creates accountability gaps.
- The project record must reflect human judgment at consequential points.
- Trust in agent output is built incrementally; starting with human approval at all boundaries is the safer baseline.

## Constraints

- This boundary is documented in `docs/human-approval-boundaries.md` and referenced in all agent charters.
- Changes to this boundary require a new ADR and explicit human acceptance.

## Alternatives considered

- **Agents may act within predefined categories** — creates ambiguity about what is predefined; deferred until trust and operational patterns are established.
- **No formal boundary** — unacceptable; the project record and accountability model depend on this constraint.
