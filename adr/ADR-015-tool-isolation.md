# ADR-015 Tool isolation

## Status
Accepted

## Context
Tools can become over-privileged if they bypass resource controls.

## Decision
Tools must consume resource-native permissions rather than replace them.

## Consequences
- The resource remains the ultimate authority.
