# High Availability

The OCI deployment should be designed so that availability can be increased as the platform matures.

## Baseline resilience

- Use fault-tolerant managed services where available
- Deploy control plane services independently from execution workloads
- Keep workloads stateless where possible
- Externalize state into managed data services
- Use health checks, autoscaling, and rolling updates

## Advanced options

- Multi-availability-domain deployment where the region supports it
- Multi-region active/passive or active/active patterns where required
- Backup and restore for managed and self-managed state
- Separate production and non-production environments
- Immutable deployment artifacts and repeatable infrastructure provisioning

## Resilience design goal

The platform should be able to recover orchestrator and executor capacity without losing the canonical execution state or audit record.
