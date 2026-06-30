# 09 Foundation ADR Summary

## ADR-001 Capability-oriented orchestration
The orchestrator invokes business capabilities rather than specific agent implementations.

## ADR-002 Separate AI Agent Gateway
Execution mediation is isolated from orchestration and agent logic.

## ADR-003 AI Platform Kernel
Shared platform state and services are centralized in a logical kernel.

## ADR-004 AI Capability Registry
Capabilities are cataloged independently from execution runtimes.

## ADR-005 AI Runtime Service
Execution state is owned by a dedicated runtime service.

## ADR-006 AI Security Service
Authentication, authorization, delegation, and policy are central platform functions.

## ADR-007 AI Observability Service
Telemetry, lineage, audit correlation, and cost tracking are first-class platform services.

## ADR-008 Contract-first integration
All component interfaces use explicit canonical envelopes.

## ADR-009 Vendor-neutral logical architecture
Logical services remain independent from implementation products.

## ADR-010 OCI-first physical implementation
OCI is the default reference implementation for the physical deployment model.
