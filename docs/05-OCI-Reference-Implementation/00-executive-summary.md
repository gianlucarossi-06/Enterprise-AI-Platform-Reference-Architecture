# Executive Summary

The OCI reference implementation volume describes how the Enterprise AI Platform Reference Architecture can be deployed on Oracle Cloud Infrastructure. The objective is to preserve the logical architecture while selecting OCI services that minimize operational overhead and provide strong enterprise controls.

The reference implementation follows four practical rules:

1. Prefer managed services before self-managed services.
2. Prefer SaaS or PaaS before Kubernetes.
3. Use OKE only when containerized platform components are required.
4. Keep the platform logically capability-oriented and physically deployable across OCI regions and environments.

This volume maps the AI Platform Kernel, AI Agent Gateway, AI Capability Registry, AI Runtime Service, AI Security Service, AI Metadata Service, AI Observability Service, and Audit Service to OCI services and deployment patterns.
