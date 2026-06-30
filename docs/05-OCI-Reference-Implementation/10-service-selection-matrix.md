# Service Selection Matrix

This matrix summarizes the preferred OCI service choices for the reference implementation.

| Logical capability | Preferred OCI service | Alternative / extension |
| --- | --- | --- |
| User authentication and SSO | IAM with Identity Domains | Enterprise federation source |
| Governed API ingress | OCI API Gateway | OCI Functions or custom gateway logic |
| Agent and control-plane runtime | OKE or OCI-hosted application runtime | Compute VM when required |
| Capability registry | Autonomous Database | Oracle Database on VM |
| Runtime state | Autonomous Database and cache services | Self-managed datastore on OKE |
| Secrets and keys | OCI Vault | External key management integration |
| Logging | OCI Logging | External log analytics sink |
| Metrics and alarms | OCI Monitoring | External observability stack |
| Audit | OCI Audit | Immutable archive in Object Storage |
| Messaging and decoupling | OCI Streaming | Kafka or other event backbone |
| Enterprise AI services | OCI Generative AI | Approved third-party model endpoints |

## Selection guidance

Prefer the managed OCI option where it satisfies the requirement, preserves the logical architecture, and reduces operational burden.
