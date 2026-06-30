# ADR - Centralized Observability Plane

## Status

Proposed

## Context

The platform should expose observability as a centralized control-plane capability rather than as an agent-specific concern.

## Decision

A single observability service provides consistent traces, metrics, logs, lineage, and audit correlation across all agents and tools.

## Consequences

Simpler troubleshooting, better auditability, and consistent telemetry formats. Some components will need instrumentation changes.
