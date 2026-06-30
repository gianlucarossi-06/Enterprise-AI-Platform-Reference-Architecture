# ADR - Orchestration-Boundary Telemetry

## Status

Proposed

## Context

Telemetry should be emitted at the orchestration boundary and propagated downstream with shared execution identifiers.

## Decision

The orchestrator, gateway, executors, and tools all use run ID, task ID, capability ID, and trace context.

## Consequences

End-to-end correlation becomes possible with minimal ambiguity, but producers must follow a common telemetry contract.
