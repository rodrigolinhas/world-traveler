# Scope and roadmap

## v1 outcome

A user can explore the globe, open every supported country, view canonical information and selected current intelligence with provenance, create an account, record visits, view a personalized world, create trips, order stops, track a basic budget and use curated trip templates.

## Milestones

| Milestone | Goal | Scope |
| --- | --- | --- |
| M0 — Engineering Foundation | Reproducible web/API/database/CI baseline | Structure, Next.js, Go health API, PostgreSQL/PostGIS, migrations, sqlc, incremental OpenAPI, country import strategy and engineering docs |
| M1 — World Explorer | Globe → country profile | Interactive Earth, stable country selection, real locally stored country data, API, generated types, accessible panel and end-to-end verification |
| M2 — World Intelligence | Source-aware dynamic data | Currency first; then weather, advisories, statistics and news with adapters, snapshots, freshness and partial failure |
| M3 — My World | Personal globe | Registration/login, required preferences, visits, wishlist, planned destinations, visited layer and personal statistics |
| M4 — Travel Planning | Persisted multi-stop journeys | Trips, ordered stops, legs, dates, basic budgets and routes |
| M5 — Travel Knowledge | Research becomes product data | Validate schema first; templates, experiences, seasonality, costs, constraints and incremental regional datasets |
| M6 — Production Release | Deployable flagship system | Hosting, backup/restore, observability, performance, security/accessibility reviews and release documentation |

Milestones are sequential product goals, not commitments to dates. Do not create an enormous later-feature backlog before the first vertical slice works.

## v1 non-goals

No hotel/flight booking or live ticket inventory; social feeds, followers, likes or direct messages; automatic GPS tracking; native Android/iOS apps; AI assistant or ML recommendations; guaranteed visa/entry decisions; unexplained universal safety scores; real-time collaborative planning; insurance brokerage; replacement of official government information.

## Deferred decisions

Production hosting, object storage, later authentication strategies, native mobile architecture, moderation, commercial visa/flight providers, notifications, AI, dedicated search, Redis, brokers and Kubernetes remain undecided until requirements exist. User photos introduce S3-compatible storage later, potentially MinIO locally.
