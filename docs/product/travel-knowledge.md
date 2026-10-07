# Editorial travel knowledge

Preserve original research in docs/research. Curate versioned structured files under data/travel-knowledge, grouped into europe, asia, africa, americas, oceania and polar. Prefer one logical phase per file and optional continent metadata/deferred files. Never hardcode this material into frontend components.

Pipeline: original research → curated data → validation → database import → API → UI. Research is not yet supplied; do not invent itineraries, prices or citations to populate the dataset.

## Proposed records

Trip templates: id, slug, title, description, min_days/max_days, budget_min/budget_max/budget_currency, status and as_of_date; related stops, regions, experiences and sources. States DRAFT, ACTIVE, DEFERRED, ARCHIVED are editorial availability, independent of official travel advice. Users may later create personal trips from versioned templates; changes must not silently rewrite personal plans.

Experiences have CORE, RECOMMENDED or OPTIONAL priority. Future removal of optional experiences may affect estimates.

Cost estimates contain amount_min/amount_max, currency, confidence, as_of_date and source_id. Confidence distinguishes CONFIRMED_SOURCE, ESTIMATED and USER_REPORTED. A published price and a planning range must look different.

Seasonality supports country/region/place scope, month ranges, description, severity and source. Categories include RECOMMENDED, HIGH_SEASON, RAINY_SEASON, MONSOON, HURRICANE, CYCLONE, EXTREME_HEAT, WILDFIRE, SNOW and MOUNTAIN_ACCESS. Wrapping periods such as November–January must be representable.

Travel constraints describe type, optional origin/target destination, condition, effect, validity period, severity, source_id and verified_at. Relationships, closed borders, transit and previous-travel implications are potentially dynamic; preserve authoritative provenance and surface a verification prompt before booking. An editorial note is not a permanent immigration rule.

## Schema gate before conversion

Validate with: Morocco (single country); Thailand + Laos; US East/West Coast, Alaska and Hawaii as separate trips; Ecuador/Galápagos; Haiti deferred; Cuba → possible later USA entry implication; planned/excluded regions within one country; Antarctica; North Pole 90°N. These are modelling cases, not verified current travel guidance.

The validator must catch invalid ISO codes/currencies, duplicate IDs, inverted budget/duration ranges, invalid months, missing source references, unknown places, broken destinations and invalid geographic relations. Final schema and import idempotence follow these tests, not speculative exhaustive modelling. Convert regional research incrementally only after this gate.
