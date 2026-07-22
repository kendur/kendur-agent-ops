# Source Policy

Every finding produced by an agent must be traceable to a source. This policy defines what counts as an acceptable source and what must be recorded alongside it.

## Required source fields

| Field | Description |
|---|---|
| `url` | Direct URL to the source |
| `title` | Title of the page, article, or document |
| `access_date` | ISO 8601 date the source was accessed |
| `claim_type` | One of: `evidence`, `inference`, `vendor-claim`, `opinion` |
| `author` | Author name(s) if known; omit if not available |
| `publication` | Publisher, platform, or outlet if applicable |

## Acceptable sources

- Published articles, papers, or studies with identifiable authorship
- Official product documentation and changelogs
- Community forum posts and discussions (with URL and date)
- News coverage from identifiable outlets

## Not acceptable as evidence

- Paraphrase or summary without a primary source URL
- Memory or general knowledge without citation
- A vendor's claim about their own product presented as independent evidence (must be labeled `vendor-claim`)

## Claim type definitions

| Type | Definition |
|---|---|
| `evidence` | Observable data with a cited, verifiable source |
| `inference` | A conclusion the agent drew from evidence |
| `vendor-claim` | A statement a vendor makes about their own product or service |
| `opinion` | An assessment not derived from cited sources |

## Conflicting sources

If two sources contradict each other, both must be recorded. The conflict must be surfaced in the report rather than resolved silently.
