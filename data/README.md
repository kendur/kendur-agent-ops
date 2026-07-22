# Data

This directory contains synthetic reference data for schema validation and implementation testing.

## Examples

`data/examples/` includes valid examples for:

- observation;
- standard report;
- no-change report;
- decision proposal;
- capture ecosystem product score;
- no-change agent run.

The examples use dates on or after repository creation and were validated against the corresponding JSON Schema Draft-07 definitions before commit.

## Rules

- Use synthetic data only.
- Do not store credentials, personal data, private recordings, or proprietary third-party information.
- Production run records and reports belong in their configured append-only storage location.
- Reference examples may change when schemas change; update and revalidate them in the same pull request.