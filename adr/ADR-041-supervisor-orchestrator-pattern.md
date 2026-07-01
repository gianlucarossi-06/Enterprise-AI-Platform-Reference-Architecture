# ADR-041 - Supervisor Orchestrator Pattern

## Status

Accepted

## Context

The platform needs centralized planning without embedding execution logic in the orchestrator.

## Decision

The orchestrator plans against capabilities and dispatches execution to the gateway and runtime services.

## Consequences

The orchestrator stays replaceable and execution boundaries remain explicit.
