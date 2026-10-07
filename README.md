# World Observatory

An interactive globe-based travel intelligence platform combining geographic data, live external sources, trip planning, personal travel history and curated global itineraries with source provenance.

**Status:** documentation baseline, v0.1 (2026-10-07). Application implementation has not started. Repository name: `world-traveler`.

## Product journey

Explore a destination → understand it → decide whether and when to go → plan a trip → complete it → record the experience.

The globe is the primary navigation interface. The project supports a distinct 195-country challenge alongside territories, regions, places and geographic objectives.

## Planned architecture

Next.js / React / TypeScript / MapLibre → REST / OpenAPI 3.1 → Go / Chi / pgx → PostgreSQL / PostGIS.

A modular monolith with backend provider adapters, persisted snapshots, explicit freshness and graceful partial failure. Editorial travel knowledge is versioned data; personal visits are records, not country booleans.

## Start here

- [Product baseline and documentation index](docs/product/specification-v0.1.md)
- [Scope and milestones](docs/product/scope.md)
- [Architecture overview](docs/architecture/overview.md)
- [Architectural decisions](docs/adr/README.md)
- [M0/M1 backlog and GitHub setup](docs/project/backlog.md)
- [Contributing](CONTRIBUTING.md) · [Agent instructions](AGENTS.md) · [Security](SECURITY.md)

## Development

No application, database setup or runnable development commands exist yet. M0 establishes the toolchain, Compose database, migrations, API, web application and CI. Its issues must add exact installation, environment, migration and startup commands here as those become available.

Target workflow: configure environment → start PostgreSQL/PostGIS with Compose → migrate → start Go API → start Next.js. First product slice: globe → select Portugal → API → PostgreSQL → country panel. Authentication follows in M3.

## Licence

Application code uses the [MIT licence](LICENSE). Third-party geographic, provider and editorial source content retains its own licensing and attribution requirements.
