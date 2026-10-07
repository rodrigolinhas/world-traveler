# ADR-007 — Preserve source provenance and freshness metadata

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

Travel information becomes outdated and applicability depends on source and dates.

## Decision

Retain provider/source, URL, retrieval time, original update time when available and freshness. Persist snapshots; components independently return fresh, suitable stale or unavailable.

## Consequences

Contracts/storage/UI carry metadata and per-resource stale policy. Failed refreshes preserve valid data and remain observable.

## Alternatives considered

Undated dynamic values obscure uncertainty and failure behaviour.
