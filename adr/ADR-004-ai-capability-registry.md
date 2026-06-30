# ADR-004 AI Capability Registry

## Status
Accepted

## Context
The reference architecture requires a clear design decision for ai capability registry.

## Decision
Capabilities are modeled separately from agent implementations to preserve flexibility and support replacement or multiple implementations.

## Consequences
- The architecture baseline becomes explicit and reviewable.
- The logical model remains stable across implementations.
- Downstream documents can reference the ADR as a source of truth.
