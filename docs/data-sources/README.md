# Source register

All sources below are candidates, not verified current integrations. Re-evaluate before implementation; do not treat this register as current pricing, legal advice or an availability guarantee.

| Capability | Candidate |
| --- | --- |
| Map rendering | MapLibre GL JS |
| Basemap | OpenFreeMap; future PMTiles/Protomaps |
| Canonical country data | REST Countries or other validated canonical sources |
| Exchange rates | Frankfurter |
| Weather | Open-Meteo |
| Statistics | World Bank |
| News | GDELT; alternatives if requirements justify |
| Travel advice | Government sources such as FCDO |
| Places and knowledge | Wikimedia, Wikidata, Wikivoyage, UNESCO |
| Optional Earth observation | NASA GIBS |

For each selected source, add a dated evaluation identifying official documentation, licence and redistribution rights, attribution text, terms, quotas/pricing, geographic coverage, identifier mapping, source-update semantics, retrieval cadence, retention/caching rules, request authentication and failure behaviour. Record the decision and known limitations; CI must not rely on the live source.

M1 requires a reviewed canonical catalogue and map-boundary source, stable identifier mapping and an explicit sourced 195-country challenge collection. Do not invent missing membership or ignore disputed/territorial mapping exceptions.
