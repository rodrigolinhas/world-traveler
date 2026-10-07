# Geographic model

The 195-country challenge remains separate from all other trackable destinations and from the set of ISO codes. Document collection membership and sourcing during canonical data import; do not infer sovereignty from a map polygon or provider record.

| Category | Examples | Counts toward 195? |
| --- | --- | --- |
| Sovereign state collection member | Portugal, Japan | Yes |
| Territory/special-status destination | Greenland, Puerto Rico, French Polynesia, Cook Islands, Niue, Guam, Curaçao, Aruba, Faroe Islands | No automatic inclusion |
| Region | Patagonia, Yucatán, Galápagos, Atacama, US coasts, Antarctic Peninsula | No |
| Place | Machu Picchu, Petra, Angkor, CN Tower, Tikal, Taj Mahal, cities and UNESCO sites | No |
| Exceptional destination | Antarctica, Arctic, Svalbard | No automatic inclusion |
| Objective | North Pole 90°N, South Pole 90°S, Arctic/Antarctic Circles, Equator | No |

These are product categories, not assertions about legal status. A destination may need multiple relationships; cross-border regions must not be forced into a single-country assumption. Svalbard and Antarctica require explicit modelling choices when their features are implemented.

Use stable internal identities and appropriate canonical codes when available. Objectives must not be stored as countries. A country can have visits while regions remain unexplored. Map selection resolves a supported identifier; large geometries travel through dedicated map datasets or tiles, not country-profile responses.
