# OCI Mapping

## Logical to OCI mapping

- AI Agent Gateway -> OCI API Gateway, OCI Functions, or OKE-hosted gateway service
- Agent Executors -> OKE, OCI Functions, or container workloads
- AI Integration Service -> OCI Integration, OCI Functions, OKE-hosted connectors, and OCI Streaming
- Tool and connector telemetry -> OCI Logging and OCI Monitoring
- Workflow state -> Autonomous Database or OCI NoSQL Database
- Event-driven execution -> OCI Streaming and OCI Events
- Approvals and notifications -> OCI Notifications and OCI Events

## Reference note

OCI services are used to realize the logical execution plane while preserving the vendor-neutral architecture contract.
