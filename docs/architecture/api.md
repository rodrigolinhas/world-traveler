# HTTP contract

OpenAPI 3.1 is the canonical contract, introduced incrementally under openapi/openapi.yaml. Generate TypeScript types/client deterministically and document regeneration/drift checks. Do not maintain disconnected handwritten frontend/backend contract copies.

## Planned endpoint groups

| Milestone | Surface |
| --- | --- |
| M0 | GET /api/v1/healthz |
| M1 | GET /api/v1/countries; GET /api/v1/countries/{iso2} |
| M2 | GET /api/v1/countries/{iso2}/briefing |
| M3 | POST /api/v1/auth/register, /login, /logout; GET /api/v1/me; GET/POST /api/v1/me/visits; PATCH/DELETE /api/v1/me/visits/{id} |
| M4 | GET/POST /api/v1/trips; GET/PATCH/DELETE /api/v1/trips/{id}; POST /api/v1/trips/{id}/stops; PATCH/DELETE /api/v1/trips/{id}/stops/{stopId} |
| M5 | GET /api/v1/trip-templates; GET /api/v1/trip-templates/{slug} |

These are planned surfaces, not an existing API. Legs, goals and other writes receive contracts when their features are scoped. Specify validation, error responses, authentication, ownership and date/money semantics with each operation.

A briefing returns canonical country identity and independently typed components with status FRESH/STALE/UNAVAILABLE. Unavailable data is null; fresh/stale data retains provenance. Define actual payload schemas during M2 rather than using unspecified objects as a permanent contract. Valid canonical data should remain usable when one provider fails.

Profile responses exclude large geometries. Country selection must resolve a stable supported ISO2; define malformed/unknown-code responses and normalization deliberately in M1.
