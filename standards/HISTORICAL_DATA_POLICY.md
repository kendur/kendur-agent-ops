# Historical Data Policy

Agent-produced records are permanent. This policy governs how they are stored and updated.

## Core rule

**No historical record may be deleted or overwritten.**

When a score, conclusion, or observation changes, a new record is created. The prior record remains intact. The sequence of records over time is itself meaningful data.

## What this means in practice

- If an agent previously scored a product as `medium` relevance and now scores it `high`, a new `product-score` record is created with the updated score and the date of the change. The prior `medium` record is not modified.
- If a conclusion turns out to be wrong, a new observation record notes the correction and cites the evidence. The original conclusion record remains.
- If an ADR is superseded, the new ADR references the old one. The old ADR is not edited.

## Append-only storage

Reports and observations in `reports/` and `data/` are append-only. Files are not edited after they are written. New files are created for new runs.

## Rationale

- The history of how conclusions evolved is part of the project record.
- It enables reconstruction of the reasoning that led to a decision at any point in time.
- It prevents silent drift in how findings are interpreted.

## Exceptions

The only acceptable reason to remove a record is if it contains credentials, personal data, or other content that must be removed for legal or security reasons. Such removals must be documented in `docs/history/timeline.md` with an explanation.
