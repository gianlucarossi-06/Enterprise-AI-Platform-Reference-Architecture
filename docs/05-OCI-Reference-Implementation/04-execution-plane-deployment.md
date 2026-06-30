# Execution Plane Deployment

The execution plane hosts agent runtimes, tool adapters, and integration components that perform business work on behalf of the control plane.

## Deployment targets

- OKE for containerized agent executors and tool adapters
- OCI Functions for lightweight event-driven logic
- OCI Integration or self-managed connectors when integration complexity requires it
- OCI Compute only when a third-party component cannot be containerized

## Execution-plane responsibilities

- Execute agent tasks
- Invoke tools and connectors
- Mediate access to enterprise resources
- Propagate execution context
- Emit telemetry and audit events
- Apply policy decisions received from the control plane

## Design guidance

Keep agents stateless where possible. Persist long-running state in the AI Runtime Service or an approved backing store rather than embedding it inside the executor.
