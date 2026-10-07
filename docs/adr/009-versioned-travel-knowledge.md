# ADR-009 — Treat editorial travel knowledge as versioned data

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

Research contains estimates, notes and deferred journeys distinct from canonical and dynamic data.

## Decision

Preserve originals in docs/research and curate data/travel-knowledge. Validate difficult schema cases before bulk conversion; import incrementally.

## Consequences

Dates/sources/status remain editorial; personal trips must not be rewritten by template updates. Tooling follows M5.

## Alternatives considered

React hardcoding couples editorial changes to UI; replacing originals with structured exports loses nuance.
