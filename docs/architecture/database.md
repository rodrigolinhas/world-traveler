# Database

PostgreSQL is the primary system of record. PostGIS supplies geographic storage and queries. Use explicit SQL, pgx, sqlc and golang-migrate. Do not add multiple databases or an ORM by default.

Canonical country data is synchronized into local tables with stable identifiers and appropriate unique codes. Keep the challenge collection distinct from the geographic catalogue. Add regions, places, objectives, visits, trips, stops, legs, templates and user records as milestones need them, not in one speculative migration.

Use relational constraints for identity, references and valid ranges. Authorization must ensure user ownership, and legs must reference stops within their trip. Use transactions for operations whose partial completion would corrupt ordering or related records. Spatial indexes are justified by actual spatial queries.

Persist external snapshots with source metadata separately from canonical and editorial records. Monetary amounts require precise numeric storage and explicit currency; time-bearing legs eventually require local datetime/timezone pairs. Never model all user progress as a country.visited column.

M0 must document clean migration up/down workflows and sqlc generation. M1 imports validated real canonical country data reproducibly and idempotently, preserving attribution and import provenance. Import failures must not leave a partially refreshed catalogue without an explicit policy.

Begin search with PostgreSQL full-text/relational indexes and spatial filtering where needed. A dedicated search engine requires measured limitations.
