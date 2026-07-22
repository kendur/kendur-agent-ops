# Change Detection

This document defines what counts as a meaningful change that should trigger a report from an agent.

## General threshold

A change is meaningful if it would affect a decision, a design choice, or the human maintainer's awareness of the environment. Noise—minor edits, unchanged metrics, routine updates—should not trigger a report.

## Agent-specific thresholds

### Capture Ecosystem Analyst

| Trigger | Threshold |
|---|---|
| New product in space | Any new tool that could serve as a competitor or integration |
| Pricing change | Any change to pricing or licensing of a tracked product |
| Significant update | A major version release or feature addition relevant to capture workflows |
| Product shutdown or acquisition | Any confirmed shutdown or acquisition of a tracked product |
| Community sentiment shift | Sustained negative or positive shift in community discussion |

### Behavioral Research Analyst

| Trigger | Threshold |
|---|---|
| New study | A published study with findings directly relevant to attention, interruptions, or executive function |
| Significant meta-analysis | A review that changes or refines the evidence base |
| Contradiction of prior finding | New evidence that challenges an assumption the project is built on |

### Market and Community Analyst

| Trigger | Threshold |
|---|---|
| Competitor update | Significant product update for a comparable product |
| New entrant | A new product that addresses the same user needs |
| Community signal | A notable discussion surfacing unmet needs relevant to the project |
| Pricing change | Competitor pricing change that affects market positioning |

### Project Historian

| Trigger | Threshold |
|---|---|
| Unrecorded decision | A consequential decision was made but has no ADR |
| ADR conflict | A recent change contradicts an accepted ADR |
| Missing timeline entry | A significant event has not been added to the timeline |

## No-change behavior

If no threshold is crossed since the last run, the agent returns status `no-change` and produces no notification.
