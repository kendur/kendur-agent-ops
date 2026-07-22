# Capture Ecosystem Product Scoring

Each dimension is scored from 0 to 5. The weighted score is calculated from the current weights below.

| Dimension | Weight |
|---|---:|
| Capture reliability | 15% |
| Activation friction | 12% |
| Data portability | 12% |
| API, webhook, or MCP openness | 12% |
| Transcription and diarization | 10% |
| Developer momentum | 8% |
| Community health | 8% |
| User experience | 7% |
| Business viability | 6% |
| Cost pressure | 5% |
| Battery and storage continuity | 3% |
| Privacy and local-processing options | 2% |

For dimensions where a high raw condition is undesirable—such as activation friction or cost pressure—the stored score represents the favorable outcome: lower friction or lower cost pressure receives the higher score.

## Movement

- `rising`
- `stable`
- `watch`
- `declining`
- `legacy`
- `exit-risk`

## Recommended actions

- `monitor`
- `research`
- `test-export`
- `test-api`
- `buy-or-borrow`
- `deprioritize`
- `legacy-import-only`

## Historical rule

A reassessment creates a new product-score record with `prior_score_id`, `score_change`, and `change_from_prior`. Prior scores remain unchanged.

## Confidence

Public documentation and vendor claims may support an initial score, but confidence should remain low or medium until independent evidence or hands-on testing exists.