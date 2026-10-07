# ADR-005 — Use MapLibre for world visualization

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

The globe must support selection and thematic layers as functional navigation.

## Decision

Use MapLibre GL JS for rendering, camera, globe selection and routes; optimized map data stays separate from profile responses.

## Consequences

Verify version/globe compatibility and dataset attribution. Provide accessible selection and stable identifier mapping.

## Alternatives considered

Decorative globes fail the interaction goal; a custom renderer duplicates work.
