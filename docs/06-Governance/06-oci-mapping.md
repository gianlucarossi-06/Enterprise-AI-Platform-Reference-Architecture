# OCI Mapping

The governance domain maps to OCI using managed services and supporting platform components.

| Logical capability | OCI service |
| --- | --- |
| lifecycle metadata | Autonomous Database |
| approvals and workflow | OCI Functions, OCI Events, or workflow services on OKE |
| policy storage | OCI Object Storage or database-backed policy store |
| governance evidence | OCI Object Storage |
| audit trail | OCI Audit and OCI Logging |
| identity and access | OCI IAM and Identity Domains |

Where additional policy engines or approval workflow engines are required, they can run on OKE or OCI VMs.
