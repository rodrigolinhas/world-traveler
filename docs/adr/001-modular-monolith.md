# ADR-001 — Use a modular monolith

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

The product has related domains without demonstrated independent scaling needs.

## Decision

Keep domain modules in one Go backend/repository and one primary database. Server/sync/worker binaries may share modules.

## Consequences

Simpler transactions, development and deployment; maintain domain boundaries. Split services only for demonstrated requirements.

## Alternatives considered

Microservices add coordination and operational cost before solving a measured problem.
