# Traceability Matrix

This matrix provides a compact line of sight from architecture principles to volumes, decisions, and implementation artifacts.

| Principle | Primary volumes | Primary ADR themes | Primary implementation artifacts |
|---|---|---|---|
| Capability driven architecture | Foundation, Canonical Models, Implementation Patterns | Capability-oriented orchestration, capability registry | Capability registry, orchestrator, gateway |
| Control plane / execution plane separation | Foundation, Security, OCI, Operations | Gateway separation, runtime separation | AI Platform Kernel, AI Agent Gateway, Agent Executors |
| Zero trust security | Security, OCI, Observability | Delegated identity, token exchange, policy enforcement | IAM, Vault, policy engine, trust boundaries |
| Observability by design | Observability, Operations, Finalization | Telemetry correlation, audit correlation | OTel collectors, logging, metrics, dashboards |
| Governance by design | Governance, Finalization, Operations | Lifecycle, approvals, policy governance | Governance service, approval workflows, audit |
| Contract first integration | Canonical Models, Integration Patterns | Canonical request/response contracts | JSON schemas, tool contracts, execution contracts |
| OCI first physical architecture | OCI Reference Implementation | Landing zone, deployment profiles | OCI services, compartments, networking |

## Traceability rule

Any new feature, service, schema, or diagram must map back to one or more of these principles or to an approved ADR.

