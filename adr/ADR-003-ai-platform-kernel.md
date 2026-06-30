# ADR-003 AI Platform Kernel

## Status
Accepted

## Context
The reference architecture requires a clear design decision for ai platform kernel.

## Decision
Shared platform services such as registry, runtime, security, metadata, observability, and audit belong to a logical kernel.

## Consequences
- The architecture baseline becomes explicit and reviewable.
- The logical model remains stable across implementations.
- Downstream documents can reference the ADR as a source of truth.
