# External providers

All third-party calls pass through backend adapters. Intelligence services depend on capability contracts such as ExchangeRateProvider, WeatherProvider, NewsProvider, TravelAdviceProvider, CountryStatisticsProvider and PlacesProvider, added incrementally.

Adapters normalize responses, validate upstream data and carry source metadata. Vendor structs must not leak into frontend contracts. Replacing a news vendor should change adapter wiring, not country pages.

Candidate sources are provisional: Frankfurter exchange rates; Open-Meteo weather; World Bank statistics; GDELT news; government/FCDO advisories; Wikimedia/Wikidata/Wikivoyage/UNESCO places and knowledge. Canonical country data may use REST Countries or another validated source. OpenFreeMap and later PMTiles/Protomaps are rendering options; NASA GIBS is an optional future thematic layer.

Before implementation, verify coverage, terms, licence, attribution, quotas, pricing, update cadence and failure behaviour. See [source register](../data-sources/README.md). No candidate is an integration commitment.

Use fixed approved endpoints, backend secrets, context cancellation, finite deadlines and bounded fan-out. Rate limits/retries must respect provider policies and request budgets. Test with recorded fixtures and local mock servers. Persist normalized snapshots; return suitable stale data or unavailable independently on failure.

M2 starts with currency to exercise the complete adapter → normalization → snapshot → provenance → UI path before wider aggregation.
