# ADR-0002: Daily Monitoring as Initial Default Cadence

**Date:** 2026-07-22  
**Status:** Accepted

## Context

The maintainer wants early visibility into whether the monitoring system works and considers weekly feedback too slow during the initial phase.

## Decision

Daily monitoring is the initial default. Cadence remains configurable per agent and source.

Every run is logged. A daily trigger does not require a daily human-facing report: no-change runs remain silent.

## Alternatives considered

- Weekly monitoring
- Hourly monitoring
- On-demand checks only

## Consequences

- Freshness can be evaluated immediately.
- Change thresholds and silence rules protect attention.
- Cadence may be reduced after operating evidence is available.