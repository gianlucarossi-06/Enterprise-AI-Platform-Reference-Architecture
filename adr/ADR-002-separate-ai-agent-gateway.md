# ADR-002 Separate AI Agent Gateway

## Status
Accepted

## Context
The reference architecture requires a clear design decision for separate ai agent gateway.

## Decision
A distinct gateway mediates execution, policy enforcement, routing, and telemetry between orchestrator and downstream agents.

## Consequences
- The architecture baseline becomes explicit and reviewable.
- The logical model remains stable across implementations.
- Downstream documents can reference the ADR as a source of truth.
