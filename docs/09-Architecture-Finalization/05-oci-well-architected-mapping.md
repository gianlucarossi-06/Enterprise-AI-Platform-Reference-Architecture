# OCI Well-Architected Mapping

The OCI mapping is organized as a practical deployment guide aligned to well-architected cloud principles.

| OCI principle | EARA realization |
|---|---|
| Security first | IAM, Vault, Certificates, Security Zones, WAF, Cloud Guard |
| Reliability and resilience | Multi-AD, multi-region, backup, disaster recovery, object storage |
| Operational excellence | Logging, Monitoring, Audit, APM, alarms, runbooks, GitOps |
| Performance and scalability | OKE autoscaling, streaming, caching, managed database services |
| Cost optimization | FinOps dashboards, usage tracking, chargeback, rightsizing |
| Service consistency | Managed OCI services preferred before third-party components |

## Deployment posture

The reference implementation prefers:
1. Managed OCI services
2. OCI-native container services
3. Open-source components on OKE when native services do not meet the requirement
4. VMs only for exceptional legacy or third-party needs

