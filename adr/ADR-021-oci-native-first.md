# ADR-021 - OCI Native First

## Status

Accepted

## Context

The OCI reference implementation should prefer OCI managed services wherever they satisfy the functional, security, and operational requirements.

## Decision

Default to OCI managed services for identity, gateway, logging, monitoring, vault, streaming, and data services before introducing self-managed components.

## Consequences

Lower operational overhead, clearer support boundaries, and simpler platform governance. A managed-service-first approach may reduce portability if customer requirements later change.
