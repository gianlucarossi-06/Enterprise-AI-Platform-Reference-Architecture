# Control Plane Deployment

The control plane hosts the management and governance capabilities of the AI Platform Kernel.

## Logical services and OCI placement

- AI Orchestrator: OKE service or OCI-hosted application runtime
- AI Capability Registry: Autonomous Database or Oracle Database service
- AI Runtime Service: Autonomous Database plus OCI Cache and Streaming where appropriate
- AI Security Service: IAM with Identity Domains, Vault, Certificates, and policy automation
- AI Metadata Service: Autonomous Database or managed metadata store
- AI Observability Service: Logging, Monitoring, and an OpenTelemetry collection layer
- Audit Service: OCI Audit with immutable archival in Object Storage

## Deployment intent

The control plane should be deployed in private subnets and protected by OCI API Gateway, WAF where required, and strict compartment and policy boundaries.

## Operational characteristics

- Highly available
- Deployed independently from execution workloads
- Versioned and managed like a platform product
- Protected by strong IAM and policy controls
