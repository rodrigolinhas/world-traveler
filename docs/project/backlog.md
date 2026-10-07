# M0/M1 backlog

Stable keys below are local references, not assumed GitHub issue numbers. Full acceptance criteria and proposed labels are in [github-backlog.json](github-backlog.json).

## Milestones

- **M0 — Engineering Foundation:** Reproducible web/API/PostgreSQL/PostGIS/CI repository before production features.
- **M1 — World Explorer:** Interactive globe → country selection → real canonical profile from Go and PostgreSQL. Authentication follows in M3.

No deadlines or M2–M6 issue inventory are assigned. See the [roadmap](../product/scope.md).

## Issues

| Key | Title | Dependencies |
| --- | --- | --- |
| M0-01 | Establish repository structure and engineering conventions | None |
| M0-02 | Bootstrap Next.js web application | M0-01 |
| M0-03 | Bootstrap Go HTTP API with health endpoint | M0-01 |
| M0-04 | Add PostgreSQL + PostGIS local development environment | M0-01 |
| M0-05 | Establish golang-migrate and sqlc workflow | M0-03, M0-04 |
| M0-06 | Define initial OpenAPI contract | M0-02, M0-03 |
| M0-07 | Establish canonical country seed/import strategy | M0-01 |
| M0-08 | Add CI baseline for frontend and backend | M0-02, M0-03, M0-05, M0-06 |
| M0-09 | Add initial architecture documentation and ADRs | M0-01 |
| M1-01 | Import canonical country catalogue into PostgreSQL | M0-05, M0-07, M0-08 |
| M1-02 | Expose canonical country list and profile endpoints | M1-01, M0-06 |
| M1-03 | Build interactive MapLibre globe with country selection | M0-02, M0-07, M1-02 |
| M1-04 | Connect country selection to a real country information panel | M1-02, M1-03 |
| M1-05 | Verify the globe-to-country vertical slice end to end | M1-04, M0-08 |

M0-01 and M0-09 can be completed by review of this baseline once committed through the project workflow. Leave them open until review; local edits are not merged work. Finish M0 before M1.

## Labels

| Label | Colour | Purpose |
| --- | --- | --- |
| type:feature | #1D76DB | Product or engineering functionality |
| type:docs | #0075CA | Documentation and conventions |
| type:chore | #6A737D | Tooling and repository maintenance |
| area:web | #5319E7 | Next.js frontend and globe |
| area:api | #0052CC | Go backend and HTTP contracts |
| area:data | #0E8A16 | Database, geography and datasets |
| area:infra | #D4C5F9 | Development environment and CI |

## GitHub setup

The authenticated GitHub CLI is available. Labels and M0/M1 milestones have been created and associated with the existing issues; [GitHub status](github-status.md) records the remote organization.

Inspect existing labels/milestones/issues first and reuse matches. Create missing labels with defined names/colours/descriptions; create/reuse M0 and M1 milestones; associate published issues with their phase and labels. The status mapping prevents duplicates. Preserve unrelated objects and assign no owners without agreement.

Dependencies use stable keys and links, not assumed issue-number ordering. The JSON supplies concrete reviewable definitions without custom automation infrastructure.
