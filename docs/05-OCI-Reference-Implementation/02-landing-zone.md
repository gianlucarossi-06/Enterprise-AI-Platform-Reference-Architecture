# OCI Landing Zone

The landing zone defines the platform foundation for environments, identity, network segmentation, governance, and operational controls.

## Core building blocks

- Tenancy and compartments
- Identity Domains
- Network topology
- Security zones and network security groups
- Tagging and cost management
- Logging, Monitoring, and Audit
- Vault and certificate management
- Notifications and event routing

## Recommended compartment model

- Root tenancy
- Platform compartment
- Shared services compartment
- Control plane compartment
- Execution plane compartment
- Security and observability compartment
- Application or workload compartments
- Sandbox or non-production compartments

## Landing zone design goals

- Separate shared platform services from workload-specific resources
- Make policy boundaries explicit
- Support delegated administration
- Enable environment isolation for DEV / TEST / UAT / PROD
- Support future multi-region expansion
