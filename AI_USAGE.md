# AI Usage

This document describes how AI is used in this project.

## Role of AI in this repository

AI agents are used to:

- Monitor sources (tools, research, communities, markets) on a recurring schedule
- Summarize and structure findings into standardized report formats
- Draft decision proposals for human review
- Maintain and update the historical record

## What AI does not do

AI agents in this project may **not**:

- Independently publish content on behalf of the project
- Purchase services or commit to contracts
- Change the product charter or accepted project direction without human approval
- Overwrite historical data or prior conclusions
- Select a specific LLM, automation platform, or database provider

## Output status

All AI-generated output is treated as a draft. It is subject to human review and accountability before it is acted upon. Agent output that has been reviewed and accepted is marked accordingly in each document.

## Provider agnosticism

Agent prompts and schemas are written to be provider-agnostic. This repository does not commit to a specific LLM, automation platform, or cloud service. Those decisions will be made separately and documented as ADRs.

## Evidence standards

Agents must distinguish between:

- **Evidence** — observable data with a cited source
- **Inference** — a conclusion drawn from evidence
- **Vendor claim** — a statement from a vendor about their own product
- **Opinion** — an assessment not derived from cited sources

See [`standards/EVIDENCE_SCHEMA.md`](standards/EVIDENCE_SCHEMA.md) and [`standards/SOURCE_POLICY.md`](standards/SOURCE_POLICY.md).
