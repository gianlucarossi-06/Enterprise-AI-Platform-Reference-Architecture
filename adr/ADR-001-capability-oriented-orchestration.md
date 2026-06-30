# ADR-001 Capability-oriented orchestration

## Status
Accepted

## Context
The reference architecture requires a clear design decision for capability-oriented orchestration.

## Decision
The orchestrator selects and invokes business capabilities. Concrete agent implementations are resolved at runtime by the capability registry and gateway.

## Consequences
- The architecture baseline becomes explicit and reviewable.
- The logical model remains stable across implementations.
- Downstream documents can reference the ADR as a source of truth.
