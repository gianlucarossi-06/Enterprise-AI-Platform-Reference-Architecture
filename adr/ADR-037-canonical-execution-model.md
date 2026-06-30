# ADR-037 - Canonical Execution Model

## Status

Proposed

## Context

Agent runs, tasks, retries, and callbacks require a stable execution vocabulary.

## Decision

The platform models execution as conversation, run, task, subtask, and callback entities.

## Consequences

Execution state can be traced, correlated, and resumed consistently.
