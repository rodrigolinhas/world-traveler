# Country intelligence

A country profile presents canonical information stored locally. A separate briefing aggregates normalized dynamic components through the backend. The browser does not call each provider independently.

Start M2 with exchange rates: preferred currency EUR → Japan's JPY → provider adapter → persisted cache → internal contract → source-aware UI. Add weather, advice, statistics and news after the pattern works.

Every component independently reports FRESH, STALE or UNAVAILABLE. Prefer fresh data, then suitable stale-but-valid snapshots, then unavailable. A failed news provider must not remove the canonical country profile or successful weather result.

Display provider/source, retrieval date, original update date when available, freshness and original source URL where appropriate. A weather point or statistic must communicate its geographic or temporal scope; a capital-city reading is not countrywide weather.

Safety information shows source advisories, regional warnings, notices, update dates and authoritative links. Do not synthesize an unexplained universal score. Crime, conflict, roads, natural hazards and legal restrictions are different risks.

Entry/visa intelligence is not foundational to the MVP. Initially expose official source links and relevant advisories; future commercial integrations require renewed provider review. Never guarantee entry. Source jurisdiction and applicability matter; one government's advice is not automatically every traveler's requirement.
