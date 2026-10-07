# Caching and freshness

No Redis initially. PostgreSQL persists provider snapshots; a process-local cache is optional when justified.

Request → valid snapshot? return FRESH. Otherwise fetch/validate/normalize provider data and persist a successful snapshot. On failure return a suitable older snapshot as STALE, or UNAVAILABLE with null data. Provider failures must not overwrite the last usable payload with an error. Observe failure separately.

TTL expiration and permission to serve stale data are separate policies. High-impact advice/entry information needs explicit stale suitability and visible warnings/source dates; there is no implied unlimited stale lifetime. Define those policies before each provider is exposed.

Freshness policies are centralized and configurable, not duplicated across handlers. Initial planning values:

| Resource | Proposed TTL |
| --- | --- |
| Country metadata | About 30 days |
| World Bank statistics | About 30 days |
| Exchange rates | 12–24 hours |
| Weather | 30–60 minutes |
| News | 15–30 minutes |
| Travel advisories | Several hours |
| UNESCO content | Several weeks |

Values are engineering starting points, not promises of current source accuracy. Retrieved recently and updated recently are different facts. Use a controllable clock in freshness tests. Bounded request/provider deadlines prevent one component from holding an entire briefing indefinitely.
