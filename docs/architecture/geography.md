# Rendering and geographic domain

MapLibre handles the camera, globe interaction, visual layers, polygon selection and route rendering. PostGIS handles geometry storage, relations, spatial queries and geographic calculations. Do not implement spatial domain rules in map styling code.

Country profile responses contain ordinary metadata, not enormous polygons. Deliver optimized geographic datasets or tiles separately, with recorded licence/attribution and reproducible preparation. Map feature identifiers must map reliably to the local country catalogue; unsupported territories and disputed geometry must not be silently counted toward the challenge.

First slice: polygon or accessible country selector → ISO2 PT → GET /api/v1/countries/PT → local PostgreSQL record → Portugal panel. Document mapping exceptions and boundary source limitations in the data-source evaluation.

Later spatial uses include points in regions, nearby places, trip stop coordinates, memories and routes. Introduce spatial indexes and calculations as the relevant queries exist. Objectives such as poles and circles must not masquerade as sovereign countries.
