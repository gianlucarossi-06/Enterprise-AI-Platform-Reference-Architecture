# ADR-022 - Managed Service First

## Status

Accepted

## Context

The reference implementation should prefer managed services over self-managed infrastructure for control-plane and platform capabilities.

## Decision

Use OKE only when containerization is required for platform logic, connectors, or third-party components that do not have a managed OCI alternative.

## Consequences

Improved reliability and reduced patching burden. Some specialized workloads may still require OKE or VM-based deployment.
