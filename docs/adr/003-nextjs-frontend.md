# ADR-003 — Use Next.js for the web frontend

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

Public content and interactive globe experiences belong in one application.

## Decision

Use Next.js/React/TypeScript with client-side MapLibre and suitable public-page rendering.

## Consequences

Client/server boundaries and WebGL loading require deliberate handling.

## Alternatives considered

A standalone SPA would require another solution for public content rendering.
