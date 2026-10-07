# ADR-006 — Integrate external APIs through provider adapters

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

Vendor contracts and availability differ and can change independently.

## Decision

Call providers only through backend capability adapters and normalize to internal contracts. Secrets remain backend-only.

## Consequences

Adapters need deterministic tests; replacing a vendor does not rewrite frontend pages. Introduce capabilities incrementally.

## Alternatives considered

Direct frontend calls introduce vendor coupling and inconsistent secret handling/aggregation.
