# ADR-004 — Use PostgreSQL + PostGIS

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

Relational personal journeys and geographic queries share one data model.

## Decision

Use PostgreSQL as the primary record store and PostGIS for geographic storage/queries. Use explicit SQL, constraints and justified indexes.

## Consequences

One database covers spatial and relational needs; choose coordinate systems and geometry formats as features arrive.

## Alternatives considered

Multiple stores or application-only spatial calculations add synchronization and domain complexity.
