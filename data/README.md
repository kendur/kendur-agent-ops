# Data

This directory holds reference data and example records used for development and validation.

## Structure

- `examples/` — example JSON records conforming to the schemas in `schemas/`. Use these to test schema validation and understand expected output formats.

## Rules

- Data files in this directory are reference material, not production data.
- No real user data, credentials, or proprietary third-party data should be stored here.
- Production agent output belongs in `reports/`, not here.
- Files in this directory may be edited; they are not subject to the append-only policy that applies to `reports/`.
