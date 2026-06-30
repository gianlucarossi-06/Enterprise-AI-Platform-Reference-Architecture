# 08 Initial OCI Mapping

This section provides a high-level mapping from the logical architecture to OCI services.

| Logical capability | OCI reference implementation |
|---|---|
| Identity federation | OCI IAM Identity Domains |
| API ingress | OCI API Gateway |
| Control plane orchestration | OCI Container Engine for Kubernetes (OKE) or OCI Functions for lightweight services |
| Capability registry | Autonomous Database or OCI Database service |
| Runtime state | Autonomous Database, OCI Cache, OCI Streaming |
| Security services | OCI IAM, Vault, Certificates, WAF |
| Observability | OCI Logging, Monitoring, Audit, and optionally OpenTelemetry Collector on OKE |
| Audit archive | OCI Audit and Object Storage |
| Domain agent runtime | OKE, OCI Functions, or OCI Compute |
| Resource integrations | Service connectors, private endpoints, and secure network paths |

The OCI mapping is intentionally indicative at this stage. The authoritative logical architecture is cloud neutral.
