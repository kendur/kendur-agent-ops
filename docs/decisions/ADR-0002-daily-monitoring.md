# ADR-0002: Daily Monitoring as Initial Default Cadence

**Date:** 2026-07  
**Status:** Accepted

## Context

Agents need a default monitoring cadence. The cadence determines how often each agent runs and how often reports may be produced.

## Decision

Daily monitoring is the initial default cadence for all agents. This means each agent checks its sources once per day unless configured otherwise.

## Rationale

- Daily cadence balances freshness against noise. Most sources do not change meaningfully more than once per day.
- It is easier to reduce frequency than to justify increasing it once a pattern is established.
- Agents must remain silent when nothing meaningful changed, so a daily trigger does not mean a daily report.

## Constraints

- Cadence is configurable per agent and per data source.
- Any change to the default cadence requires a new ADR.
- Changes to individual agent cadences must be documented in the relevant agent charter.

## Alternatives considered

- **Weekly** — too slow for a market and tools monitoring context where significant changes can happen quickly.
- **Hourly** — too frequent for most sources; would produce excessive noise.
- **On-demand only** — removes the benefit of consistent background monitoring.
