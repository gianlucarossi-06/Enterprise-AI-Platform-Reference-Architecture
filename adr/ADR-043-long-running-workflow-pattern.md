# ADR-043 - Long-Running Workflow Pattern

## Status

Accepted

## Context

Some agent interactions exceed a single request-response cycle and require durable state.

## Decision

The runtime service stores checkpoints, retries, callbacks, and completion state for long-running workflows.

## Consequences

The platform can safely resume, cancel, or audit long-lived executions.
