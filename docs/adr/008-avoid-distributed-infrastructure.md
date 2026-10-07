# ADR-008 — Avoid distributed infrastructure until justified

**Status:** Accepted baseline
**Date:** 2026-10-07
**Source:** World Observatory specification v0.1

## Context

There are no measured requirements for extra stores, brokers, dedicated search or orchestration.

## Decision

Start without Redis, Kafka, RabbitMQ, Elasticsearch, Kubernetes or microservices. Use PostgreSQL snapshots/search and same-repository sync work; process-local cache is optional.

## Consequences

Operational surface stays limited. New infrastructure requires concrete limitations and a superseding ADR where constraints change.

## Alternatives considered

Speculative distributed components increase failure modes before delivering product value.
