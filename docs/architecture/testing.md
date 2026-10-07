# Testing and CI

Test important behaviour, not a coverage percentage. No application checks exist at the documentation stage; M0 configures runnable commands and records them in README.

Go tests cover normalization, rules, cache policy, provider parsing and trip calculations. HTTP tests cover validation, auth, authorization, error contracts and independent provider failures. Database integration tests exercise migrations, relational constraints and actual PostGIS queries.

Provider CI tests use fixtures/local mock HTTP servers, not live upstream availability. Frontend tests cover country panels/forms/state/loading/errors. End-to-end workflows grow incrementally: globe selection → panel; login → visit → visited layer; trip → ordered stops → save.

M0 CI adds format, vet/static checks, Go tests/build and race checks where practical; frontend lint/typecheck/tests/build as configured. Add actionable govulncheck, dependency auditing and secret scanning. Introduce OpenAPI validation, migration checks and travel schema validation as their artefacts exist. Keep permissions minimal and versions pinned according to verified tooling.

For M1, prove PT lookup through a real migrated/seeded database and visible Portugal panel; include malformed/unknown identifiers, empty/error/loading states, direct URLs, navigation and accessible selection. Tests must fail on broken behaviour rather than merely mirror implementation.
