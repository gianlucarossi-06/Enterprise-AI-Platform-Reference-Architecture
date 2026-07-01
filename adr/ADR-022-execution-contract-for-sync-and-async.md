# ADR-022 Execution contract for sync and async

## Status
Accepted

## Context
The platform must support both immediate and long-running execution styles.

## Decision
The same canonical execution contract is used for synchronous requests, asynchronous callbacks, and workflow handoffs.

## Consequences
- the gateway can handle multiple execution modes consistently
- audit and telemetry remain correlated
- long-running work can be resumed and replayed
