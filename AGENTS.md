# Repository instructions

## Before changing code

Read README.md, the relevant docs/product and docs/architecture pages, applicable ADRs and the issue acceptance criteria. Inspect the existing implementation and all relevant callers before editing. The v0.1 baseline is in docs/product/specification-v0.1.md.

This repository is currently a documentation baseline. Do not describe proposed tooling or product features as implemented. Build M0 first, then the M1 globe → country vertical slice. Do not bootstrap future modules merely to populate a directory tree.

## Architecture constraints

- Preserve the Go modular monolith and PostgreSQL as the primary system of record.
- PostGIS owns geographic queries; MapLibre owns interactive globe rendering.
- Call external providers through backend adapters, never directly from frontend code.
- Keep editorial travel knowledge in versioned data, never hardcoded in React components. Preserve original research separately.
- Preserve provider, source URL, retrieval time, source update time when available and freshness for external information.
- Dynamic information must have explicit freshness; provider failures must degrade independently to suitable stale data or unavailable.
- OpenAPI 3.1 is the HTTP contract. Update it when HTTP contracts change and generate frontend types deterministically.
- Keep canonical, dynamic, editorial and user data distinct. Do not collapse visits into country.visited.
- Major architectural changes require an ADR that supersedes the relevant decision.

## Working practices

Prefer focused vertical slices and reuse existing code, the standard library and native features. Add dependencies only with technical justification. Do not introduce Redis, Kafka, RabbitMQ, Elasticsearch, Kubernetes, microservices, multiple databases or AI without a demonstrated requirement and an ADR where architectural constraints change.

Preserve working behaviour. Avoid unrelated refactors, speculative abstractions and formatting noise. Add meaningful tests for non-trivial behaviour; provider tests use fixtures or local mock servers, never live services. Update documentation when architecture or product behaviour changes.

Validate trust boundaries; use parameterized SQL and explicit database permissions. Keep secrets on the backend. Never log passwords, session tokens, keys or sensitive profile data. Minimize user data; passport numbers/scans and continuous location tracking are outside initial scope.

Consider error paths, accessibility and responsive behaviour. Run the applicable formatting, lint, type, test and build checks actually configured in the repository. Report unavailable checks honestly. Do not commit or publish unrelated local files.
