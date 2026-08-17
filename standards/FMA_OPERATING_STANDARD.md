# File Manager Agent (FMA) Universal Operating Standard

_Last updated: 2026-08-17_

## Authority

This file is the shared operating contract for every project-scoped File Manager Agent named `<Project> FMA`.

Every current and future FMA inherits this standard automatically. Project-local FMA files may add configuration and stricter rules, but may not weaken this standard without explicit adjudication by Durand.

The machine-readable registry at `data/FMA_REGISTRY.yaml` is the authoritative list of registered FMA instances and their decision queues.

An FMA instance is not considered operationally registered until its registry entry includes, at minimum:

- project name;
- FMA instance name;
- repository or source system;
- decision queue location;
- issue tracker;
- adjudication label;
- escalation threshold;
- escalation cadence.

## Project Isolation

Each FMA operates only within its configured project unless Durand explicitly authorizes a cross-project action. Project data, rules, queues, mirrors, and issue histories remain isolated even though shared FMA behavior is universal.

## Gated Decisions

An FMA must gate and record operations involving destructive changes, identity-sensitive renames or placement, ambiguous lifecycle classification, multiple plausible destinations or interpretations, possible mirror regression, or any action that could materially alter authority, provenance, traceability, or history.

A gated operation does not pause unrelated safe work. The FMA records the decision, skips only dependent work, preserves context, and continues reversible maintenance.

## Decision Queue Contract

Every registered FMA must maintain its own decision queue. Each entry must preserve:

- stable queue ID;
- `created_at` timestamp including timezone;
- category;
- decision required;
- affected paths/resources;
- blocked operation;
- safe work already completed;
- available interpretations/options when known;
- status;
- issue number and URL after escalation;
- final resolution when received.

Required status values include `pending`, `escalated`, and `resolved`. Queue history is never deleted merely because an item is resolved.

## Universal 24-Hour Escalation

Every registered FMA decision queue is checked hourly.

For every FMA-gated queue entry whose status is `pending` and whose `created_at` is at least 24 hours old:

1. Search that project's configured issue tracker for an existing issue covering the same decision.
2. If a matching issue exists, do not create a duplicate.
3. If no matching issue exists, create an issue that states:
   - the decision required;
   - affected files, paths, systems, or assets;
   - the blocked operation;
   - safe work already completed;
   - available interpretations or options;
   - relevant validation findings or provenance where available.
4. Apply the project's configured adjudication label and any clearly relevant existing labels.
5. Record the issue number and canonical link in the FMA decision queue.
6. Change the queue item's status to `escalated` while leaving the substantive decision unresolved.
7. Continue processing every other eligible entry across every registered FMA.

Later hourly checks must not create duplicate issues for already-escalated items.

## Notification Rule

Durand is notified only when:

- at least one queue item is escalated; or
- an error prevents an otherwise eligible escalation from being completed.

If nothing qualifies, the escalation run remains silent.

## Registration Rule for Future FMAs

Creation of a new `<Project> FMA` must include registration in `data/FMA_REGISTRY.yaml` in the same setup change that creates or designates its decision queue. The registry entry inherits this standard by reference; the hourly 24-hour escalation check therefore applies without creating a separate per-project scheduler.

If an FMA is discovered without a registry entry or without a decision queue, that is a configuration defect and must be corrected before the FMA is considered fully registered.

## Existing Detailed Project Standard

The original detailed FMA behavior was developed in `kendur/BBEG-tSAC` at `AI_CONTEXT/fma_operating_standard.md`. Project-specific validation, transfer, mirror, and asset-handling rules remain valid where they do not conflict with this shared standard.
