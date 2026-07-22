# Escalation Rules

Some findings require immediate human attention rather than waiting for a scheduled report. This document defines when and how agents escalate.

## Escalation triggers

An agent must escalate when:

1. A finding directly contradicts an accepted ADR or core project assumption.
2. A source indicates a time-sensitive risk to the project (a competitor launched, a key tool is shutting down, a security issue was identified).
3. The number of meaningful changes in a single run exceeds three—the three most important go into the report; if additional items are also urgent, they trigger escalation.
4. A conflict is found in historical data that suggests a prior decision was based on incorrect information.

## Escalation does not mean the agent acts

Escalation means the agent flags the finding for immediate human review. The agent does not take action. The agent does not push changes, publish content, or make commitments.

## Escalation format

An escalation is a report with `status: "escalation"`. The key items section must contain the single most urgent item first, followed by at most two additional urgent items. The detail section explains why each item is urgent.

The escalation must be delivered through a channel configured by the human maintainer. If no channel is configured, the escalation is included in the next scheduled report with a note that it was not delivered in real time.

## Non-escalation

Routine findings, even if they are the most interesting finding of the week, do not escalate. Escalation is reserved for situations where delay could cause meaningful harm to the project.
