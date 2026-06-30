# ADR-023 - AI Platform Kernel Deployment

## Status

Accepted

## Context

The AI Platform Kernel should be deployed as a set of logically separated services rather than as one monolithic platform application.

## Decision

Implement the kernel as distinct OCI-deployed services for registry, runtime, security, metadata, observability, and audit.

## Consequences

Improves lifecycle independence, scaling, and replacement flexibility. Requires stronger service contracts and more deliberate inter-service orchestration.
