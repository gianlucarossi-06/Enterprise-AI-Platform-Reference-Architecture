# ADR-024 Managed long-running workflows

## Status
Accepted

## Context
Some capabilities require durable state, retries, compensations, and human approvals.

## Decision
Workflow state is persisted in the AI Runtime Service instead of relying on executor memory.

## Consequences
- recovery and replay become possible
- execution remains auditable
- the platform can scale horizontally without losing state
