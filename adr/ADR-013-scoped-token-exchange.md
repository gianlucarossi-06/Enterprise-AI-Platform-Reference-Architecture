# ADR-013 Scoped token exchange

## Status
Accepted

## Context
The platform requires down-scoped access between layers.

## Decision
Each hop receives a token with reduced audience and privilege.

## Consequences
- The blast radius of a compromised component is reduced.
