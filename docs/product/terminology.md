# Terminology and data classes

| Term | Meaning |
| --- | --- |
| Country challenge | Explicit collection of 195 sovereign states; territories do not increase its count |
| Destination | Useful travel geography, which need not be a sovereign country |
| Region | Geographic area such as Patagonia, Galápagos or a US travel region |
| Place | Addressable city, site, trailhead or attraction |
| Geographic objective | Coordinate or milestone such as a pole, circle or Equator |
| Visit | Dated personal record, optionally related to a trip and region |
| Goal | Desired outcome independent of visit records |
| Trip | User-owned planned or completed journey |
| Stop | Ordered destination/base/gateway/transit location in a trip |
| Leg | Travel between two stops |
| Template | Versioned editorial journey, never a booking or availability promise |
| Snapshot | Normalized persisted external-provider data and provenance |
| Briefing | Country intelligence composed from independently available components |

## Data classes

1. Canonical: locally synchronized names, identifiers, capitals, currencies, languages, boundaries, continents and subregions. Relatively stable does not mean immutable.
2. Dynamic: weather, exchange rates, news, advisories, entry information and border status. Explicit freshness and provenance required.
3. Editorial: researched templates, durations, estimates, experiences, recommended periods and deferred routes. Version-controlled and dated.
4. User: visits, trips, lists, budgets and later journals/photos. Owned and authorized separately.

Community-generated content is a future additional class. Do not mix editorial availability, source advisories and personal decisions into one status.
