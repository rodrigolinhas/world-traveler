# World Observatory — v0.1 baseline

**Status:** Draft baseline. **Date:** 2026-10-07. **Source:** the supplied World Observatory Product & Engineering Specification v0.1. **Repository:** rodrigolinhas/world-traveler.

This documentation set records the requirements and decisions derived from that specification. Examples describe intended models, not implemented APIs or promised current travel facts. The original supplied specification remains the source baseline; these pages organize it for engineering work.

## Product requirements

| Topic | Authoritative working document |
| --- | --- |
| Vision, differentiation and principles | [Vision](vision.md) |
| v1 scope, non-goals and M0–M6 roadmap | [Scope](scope.md) |
| Shared vocabulary and data classes | [Terminology](terminology.md) |
| Countries, territories, regions, places and objectives | [Geographic model](geographic-model.md) |
| Intelligence, freshness and partial failure | [Country intelligence](country-intelligence.md) |
| Visits, goals, progress and privacy | [My World](my-world.md) |
| Trips, stops, legs, budgets and dates | [Trip planning](trip-planning.md) |
| Templates, experiences, seasonality and constraints | [Travel knowledge](travel-knowledge.md) |
| Deferred community and later capabilities | [Future community](future-community.md) |

## Engineering requirements

| Topic | Working document |
| --- | --- |
| Modular monolith and target repository layout | [Overview](../architecture/overview.md) |
| Go modules, concurrency and sync commands | [Backend](../architecture/backend.md) |
| Feature organization, globe and state | [Frontend](../architecture/frontend.md) |
| PostgreSQL/PostGIS, migrations and constraints | [Database](../architecture/database.md) |
| Map data and geographic identifiers | [Geography](../architecture/geography.md) |
| External adapters and candidate providers | [Providers](../architecture/providers.md) |
| Snapshots and freshness policies | [Caching](../architecture/caching.md) |
| Attribution and source metadata | [Provenance](../architecture/provenance.md) |
| OpenAPI and incremental HTTP surface | [API contract](../architecture/api.md) |
| Local/production topology and observability | [Deployment](../architecture/deployment.md) |
| Tests and CI | [Testing](../architecture/testing.md) |
| Architecture decisions | [ADR index](../adr/README.md) |
| Source evaluation | [Data sources](../data-sources/README.md) |
| Original research preservation | [Research](../research/README.md) |
| Security and privacy | [Security baseline](../security/baseline.md) |
| Immediate engineering work | [M0/M1 backlog](../project/backlog.md) |

## Non-negotiable baseline

The system is a modular monolith. External providers are backend-only. PostgreSQL is the system of record; PostGIS handles geographic queries and MapLibre handles rendering. OpenAPI is the HTTP contract. Editorial knowledge is versioned data. External data retains provenance and explicit freshness. Provider failure degrades gracefully. Personal data is minimized. Infrastructure requires a demonstrated problem. Functional vertical slices take priority over architecture for its own sake.

The 195-country challenge is a product collection, separate from ISO assignments and additional destinations. Visits are first-class records. Editorial template availability is independent of official advisory information. Dynamic entry and safety information must not imply guaranteed entry or a universal safety score.

## Immediate sequence

Establish README, AGENTS, CONTRIBUTING, SECURITY, product/architecture documentation, nine ADRs and a scoped GitHub backlog. Then implement M0. M1 proves globe → PT → Go API → PostgreSQL → country panel. M2 begins with currency intelligence before adding more providers. Authentication starts in M3.

## Change policy

Future product revisions must be explicit. Major architectural decisions change through a superseding ADR rather than a silent rewrite. Technology versions, provider terms, quotas and licences must be verified at implementation time. The proposed Go 1.27+ requirement is an unverified target, not an installed or available toolchain claim; resolve its availability during M0 without silently substituting a version.
