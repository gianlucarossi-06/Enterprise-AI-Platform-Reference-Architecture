# Implementation Considerations

## Recommended implementation sequence

1. Build the OCI landing zone.
2. Establish IAM, network, and security foundations.
3. Deploy the AI Platform Kernel services.
4. Deploy the execution plane on OKE.
5. Integrate enterprise resources and connectors.
6. Establish observability and audit routing.
7. Validate resilience and recovery.
8. Add reference profiles and production hardening.

## Common decisions

- Whether the orchestrator runs on OKE or an OCI-hosted application runtime
- Whether the registry and runtime state are held in Autonomous Database or a managed external data store
- Which integrations require OCI Integration or a custom connector layer
- Which resources require private connectivity and which can use public endpoints
- Which telemetry streams need to be archived for compliance

## Delivery guidance

Keep the logical architecture stable and vary only the OCI deployment profile, the number of regions, and the selected managed services where customer constraints require it.
