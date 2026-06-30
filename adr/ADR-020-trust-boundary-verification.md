# ADR-020 Trust boundary verification

## Status
Accepted

## Context
Each boundary must independently verify the request context.

## Decision
Every hop validates context before execution.

## Consequences
- Trust is never implied by topology alone.
