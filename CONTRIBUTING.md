# Contributing

Start with the [baseline](docs/product/specification-v0.1.md), [architecture](docs/architecture/overview.md) and [ADRs](docs/adr/README.md). Use a scoped issue and branch such as `docs/1-foundation` or `feat/12-country-panel`. Use Conventional Commits, for example `docs: establish product baseline` or `feat(world): expose country profile`.

## Scope

Finish M0 before production feature code. Then prioritize the M1 globe → country slice. Add dependencies only when they solve a demonstrated problem. Major architectural changes require an ADR; ordinary implementation choices do not. Preserve working behaviour and avoid unrelated refactors.

## Pull requests

Explain the concrete problem and resulting behaviour, link the issue, and describe relevant validation and limitations. Include API contracts, migrations, attribution and documentation when affected. Never include secrets or unrelated local artefacts.

## Definition of done

- Acceptance criteria implemented; expected errors handled.
- Meaningful behaviour covered by relevant tests; provider tests deterministic and offline.
- Responsive behaviour and accessibility considered.
- OpenAPI updated and generated frontend types refreshed for HTTP changes.
- Migrations included for schema changes; documentation updated for behaviour or architecture changes.
- Applicable formatting, lint, type checking, tests and build pass.
- Unrelated changes excluded.

Coverage percentage is not the objective. See [testing](docs/architecture/testing.md). Until M0 adds tooling, validation is limited to documentation consistency, local links and diff checks; no application checks are available.

## Data contributions

Keep original research in docs/research. Curate structured travel knowledge separately, preserving source references and as-of dates. Validate difficult cases before bulk conversion; see [travel knowledge](docs/product/travel-knowledge.md). External sources have independent licences.

Report vulnerabilities through the process in [SECURITY.md](SECURITY.md).
