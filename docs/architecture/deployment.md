# Development and deployment

No runnable deployment exists yet. M0 must document exact prerequisites/versions, environment configuration, database startup, migrations, API/web commands and hot reload. Pin verified compatible tool versions; do not copy proposed versions without checking availability.

Target local flow: clone → configure environment → Docker Compose PostgreSQL/PostGIS → migrations → Go API → Next.js. Add example environment files with placeholders and exclude real secrets from version control.

Initial production topology: HTTPS reverse proxy → Next.js and Go API under one origin → PostgreSQL/PostGIS. No Kubernetes. Hosting provider is deferred. Provider credentials stay backend-only; production session cookies are Secure and HttpOnly.

M6 includes tested backups/restoration, deployment and rollback documentation, security/accessibility review, performance analysis and release/versioning. Add object storage with user photos, not beforehand.

Initial observability uses structured slog logs, request IDs, provider names/latency/failure status, meaningful errors and sync results. Exclude passwords, session tokens, keys and sensitive profile data. Metrics and tracing follow demonstrated production needs.
