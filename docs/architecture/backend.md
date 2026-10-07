# Backend

Planned stack: Go (specification target 1.27+, availability to verify during M0), Chi, pgx/pgxpool, sqlc, golang-migrate, log/slog and REST. Pin a verified toolchain during bootstrap; document any baseline adjustment explicitly.

Organize by domain under api/internal, not global controllers/services/repositories/models. A module such as trips may contain model.go, service.go, repository.go and http.go when those responsibilities exist. Do not create empty layers or interfaces for hypothetical implementations.

Provider boundaries are required by the product: intelligence services depend on capability interfaces and normalized contracts, never vendor response types. They use context-aware HTTP clients, bounded concurrency, deadlines and independent failures. User input cannot select arbitrary provider URLs.

cmd/server runs HTTP. cmd/sync provides reproducible country/statistics/UNESCO synchronization when those integrations exist. A worker process can be added later within the same repository; no external queue is initially required.

Handlers validate requests and use explicit DTOs; services enforce domain rules; database access uses parameterized SQL. Log request IDs, provider names, latency/failure status and sync outcomes without credentials or sensitive user data. Authentication arrives in M3 with Argon2id and server-side sessions, not JWTs by default.
