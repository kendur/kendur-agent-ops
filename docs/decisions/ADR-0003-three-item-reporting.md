# ADR-0003: Three-Item Limit for Agent Reports

**Date:** 2026-07-22  
**Status:** Accepted

## Context

The maintainer reported that attention begins to skip ahead after roughly three list items. Long reports return the prioritization burden to the reader.

## Decision

Every human-facing report leads with at most three key items. Supporting detail remains below or in linked records.

## Alternatives considered

- No item limit
- Five key items
- One key item

## Consequences

- Agents must rank findings before reporting.
- Detail remains available without competing for initial attention.
- Additional urgent findings use the escalation path.