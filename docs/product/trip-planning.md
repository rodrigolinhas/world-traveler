# Trip planning

A trip relates ordered stops, travel legs, budget, experiences, visits and geographic goals. Proposed trip fields: id, user_id, title, status, start_date, end_date, base_currency, created_at and updated_at. Potential statuses: DRAFT, PLANNED, BOOKED, IN_PROGRESS, COMPLETED, CANCELLED; implement only those needed initially.

## Stops and legs

Stops have id/trip_id, optional country/region/place references, display_name, optional location, position, arrival_date, departure_date and notes. Later roles include DESTINATION, BASE, GATEWAY and TRANSIT; Ushuaia may be an expedition gateway rather than the journey's objective.

Legs link from_stop_id to_stop_id within the same trip, with mode, planned_cost, currency, optional departure/arrival local times and notes. Modes: TRAIN, BUS, FLIGHT, FERRY, CAR, WALK, OTHER. Enforce trip ownership and stop consistency. Reordering must leave a valid ordered journey and have deterministic semantics.

Date-only trip fields do not imply one global timezone. Future timed legs must support departure_local_datetime/departure_timezone and arrival_local_datetime/arrival_timezone independently, including International Date Line crossings. Multiple flight segments are deferred.

## Budget

M4 may start with a trip total. Later distinguish estimated, planned and actual amounts and categories: accommodation, food, local/intercity transport, flights, activities, visa, insurance, equipment, miscellaneous and contingency. Use precise numeric money representation and explicit currencies. Do not silently sum unlike currencies or treat estimates as current quotes.

M4 delivers persistent trips, ordered stops, legs, basic budgets, dates and route visualization. Templates arrive in M5 as copyable starting points, not bookings. Complex inventory and real-time collaboration remain outside v1.
