# ADR-038 - Canonical Identity Model

## Status

Accepted

## Context

Identity must propagate through orchestrator, gateway, executor, tool, and resource access paths.

## Decision

The platform standardizes user, tenant, session, run, scopes, and approval state as shared identity metadata.

## Consequences

Authorization decisions and audit evidence remain aligned across the stack.
