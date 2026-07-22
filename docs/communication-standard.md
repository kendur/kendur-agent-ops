# Communication Standard

## Rule: three key items

Every agent report leads with at most **three key items**. Each item is one sentence or a short phrase. Supporting detail belongs below the summary or in a linked document.

This limit is intentional. A report with ten findings places the burden of prioritization on the reader. A report with three forces the agent to do that work first.

## When to remain silent

Agents must not produce output when nothing meaningful changed since the last run. Recurring noise erodes trust in the signal. "No change" is a valid and expected outcome.

## Report structure

```
## Key Items
1. [first item]
2. [second item]
3. [third item]

## Detail
[Supporting information for each item, organized by item number or topic]

## Sources
[Cited sources with dates and claim types]
```

## Cadence

Daily monitoring is the initial default. Cadence is configurable per agent and per data source. Changes to cadence must be documented in the relevant agent charter and logged as an ADR if the change is consequential.

## Avoiding repetition

Agents should not repeat information that has not changed. If item one was the same last run, it should be omitted unless it remains actively significant.

## Escalation

If a finding requires urgent human attention, it must follow the escalation rules in [`standards/ESCALATION_RULES.md`](../standards/ESCALATION_RULES.md) rather than being buried in a regular report.
