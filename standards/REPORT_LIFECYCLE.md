# Report and Artifact Lifecycle

Agent-created reports, observations, scores, and proposals use one of these lifecycle states:

| State | Meaning |
|---|---|
| `generated` | Created by an agent and not yet reviewed |
| `reviewed` | A human examined the artifact; no acceptance decision is implied |
| `accepted` | Approved for use as a current project record |
| `rejected` | Reviewed and declined; retained for history |
| `superseded` | Replaced by a newer accepted record; retained for history |

## Rules

1. Agents create artifacts only in `generated` state.
2. Human review changes lifecycle state for consequential artifacts.
3. A generated report may be committed to this repository when clearly labeled. It remains a draft, not an official public project statement.
4. Accepted records are not overwritten. Changes create a new record that references the record it supersedes.
5. Rejected and superseded records remain available unless removal is required for security or law; such removal is documented.
6. Every run receives an `agent-run` record, including no-change runs.
7. No-change runs produce no human notification.

## Official communication

A report becomes an official external recommendation, release statement, or product position only through a separate human-approved publication action.