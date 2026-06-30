# ADR-016 Immutable security audit

## Status
Accepted

## Context
Security decisions must be traceable and reviewable.

## Decision
Every allow, deny, approval, and access event is emitted as an audit event.

## Consequences
- The platform supports forensics and compliance.
