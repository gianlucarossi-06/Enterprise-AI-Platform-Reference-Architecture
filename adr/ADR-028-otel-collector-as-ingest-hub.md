# ADR - OpenTelemetry Collector as Ingest Hub

## Status

Proposed

## Context

OpenTelemetry Collector should serve as the primary ingest and routing component for platform telemetry.

## Decision

The collector receives telemetry from the platform and routes it to logging, metrics, tracing, and archive backends.

## Consequences

A vendor-neutral ingest layer reduces backend coupling and allows multiple observability backends.
