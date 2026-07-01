# Terminology Normalization

## Why normalization matters

The repository uses a consistent vocabulary so that architecture, security, operations, and implementation teams do not maintain parallel terms for the same concept.

## Canonical terminology

| Preferred term | Avoid | Definition |
|---|---|---|
| AI Platform Kernel | core platform services, shared runtime | Logical shared-services layer for the platform |
| AI Capability Registry | Agent Registry | Catalog of capabilities and implementations |
| AI Runtime Service | execution context service | Runtime state, workflow state, checkpoints, and replay |
| AI Security Service | policy service | Identity, authorization, approval, and token exchange services |
| AI Metadata Service | configuration repository | Canonical metadata for prompts, tools, capabilities, and models |
| AI Observability Service | telemetry stack | Correlated logs, traces, metrics, lineage, and cost |
| AI Agent Gateway | gateway only | Execution mediation, routing, and policy enforcement |
| Tool Adapter | tool wrapper | Agent-facing abstraction for external operations |
| Connector | integration connector | Technical integration with enterprise resources |
| Enterprise Resource | backend system | Database, SaaS, API, file, or event resource |

## Usage rule

The preferred terms are used throughout the final release notes, review pack, ADRs, and mappings.

