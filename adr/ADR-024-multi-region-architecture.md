# ADR-024 - Multi-Region Architecture

## Status

Accepted

## Context

The platform should support a reference multi-region architecture, even if the initial deployment is single-region.

## Decision

Design the OCI deployment so that it can be extended to active/passive or active/active regional topologies when business requirements justify it.

## Consequences

The architecture remains resilient to future growth. Multi-region readiness adds design discipline around data replication, failover, and regional dependencies.
