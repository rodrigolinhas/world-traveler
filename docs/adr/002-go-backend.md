# ADR-002 — Use Go for the backend

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

Country briefings aggregate cancellable external I/O and require predictable operations.

## Decision

Use Go, Chi, pgx/pgxpool, sqlc and slog with bounded context-aware concurrency. Verify the specification target Go 1.27+ during M0 before pinning.

## Consequences

A separate backend toolchain needs explicit contracts and deadlines.

## Alternatives considered

Next.js-only server functions consolidate tools but do not follow the chosen backend direction.
