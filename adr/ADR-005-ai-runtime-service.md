# ADR-005 AI Runtime Service

## Status
Accepted

## Context
The reference architecture requires a clear design decision for ai runtime service.

## Decision
Execution state must live in a dedicated runtime service rather than inside orchestrator or gateway code.

## Consequences
- The architecture baseline becomes explicit and reviewable.
- The logical model remains stable across implementations.
- Downstream documents can reference the ADR as a source of truth.
