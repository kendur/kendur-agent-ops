# Human Approval Boundaries

Agents in this team operate within defined boundaries. This document states what requires explicit human approval before action is taken.

## Agents may do without approval

- Gather and store observations
- Produce draft reports
- Draft decision proposals
- Flag changes or conflicts for human review
- Update their own run logs
- Append new records to historical data

## Agents must not do without approval

- **Publish** anything on behalf of the project to any external platform
- **Purchase** or commit to any paid service, subscription, or contract
- **Alter the product charter** or any accepted statement of project direction
- **Change licensing** or add, remove, or modify a license
- **Accept a consequential decision** on behalf of the maintainer
- **Delete or overwrite** any historical record
- **Merge a pull request** that changes an ADR or operating principle

## Decision proposals

When an agent identifies a decision that requires human judgment, it must create a decision proposal using the `decision-proposal.yml` issue template or produce a `decision-proposal` schema record. The proposal sits in draft status until a human maintainer explicitly accepts or rejects it.

## Changes to this document

Any change to the boundaries defined here requires a new ADR and explicit human approval.
