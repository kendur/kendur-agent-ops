# ADR-0003: Three-Item Limit for Agent Reports

**Date:** 2026-07  
**Status:** Accepted

## Context

Agent reports risk becoming large, undifferentiated lists of findings that shift the burden of prioritization onto the reader. A communication standard is needed that forces agents to do the prioritization work.

## Decision

Every agent report leads with at most three key items. Supporting detail is placed below the summary section or in a linked document. Agents must not surface more than three items in the lead section regardless of how many findings exist.

## Rationale

- Forcing a three-item limit requires the agent to rank and select rather than list everything.
- It keeps reports scannable in the time available to a reader with limited attention.
- Supporting detail remains accessible but does not compete with the key findings for attention.

## Constraints

- The three-item limit applies to the lead section only. Detail sections may be longer.
- If more than three items genuinely require immediate attention, the excess items must trigger the escalation process described in `standards/ESCALATION_RULES.md`.

## Alternatives considered

- **No limit** — produces reports that are difficult to process quickly.
- **Five items** — still manageable but removes the forcing function that makes agents prioritize aggressively.
- **One item** — too restrictive; agents should be able to surface more than one finding when warranted.
