# ADR-014 Layered authorization

## Status
Accepted

## Context
Authorization must occur at multiple boundaries.

## Decision
The platform evaluates allow/deny decisions at each layer.

## Consequences
- Policy is explicit and composable.
