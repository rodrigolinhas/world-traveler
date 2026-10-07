# My World

Visits are first-class personal records, not a boolean on a country. Proposed fields: id, user_id, country_id, optional region_id/trip_id, started_on, ended_on, visit_type, notes, created_at and updated_at. Types: STAY, DAY_TRIP, TRANSIT and LAYOVER. Validation and ownership rules must be defined when introduced in M3.

This supports multiple Japan visits, total travel days and first/last visit dates. A configurable rule for which visits count toward personal totals may arrive later; do not silently decide that every transit counts.

Goals are independent of visits and may target countries, territories, regions, points or collections. Examples: all 195 countries, seven continents, Antarctica, poles, Arctic Circle, EU collection and selected UNESCO collections.

Progress measures remain independent: countries/195, continents/7, territory count, explored regions, travel days, polar destinations/objectives and UNESCO visits. Do not collapse all progress into the country total.

M3 includes account/session authentication, only preferences required by current functionality, visits, wishlist, planned destinations, visited globe layer and personal statistics. Every personal API must enforce ownership. Future trip/visit visibility needs explicit privacy controls.

A later traveler profile may include nationality, residence, currency, languages, style, pace and accommodation preferences. Dietary, accessibility, religious or other sensitive considerations need explicit value, consent and privacy design; they are outside MVP. No passport numbers/scans or continuous location tracking.
