# Observability

Observability is implemented as a platform capability spanning logging, metrics, tracing, and audit correlation.

## OCI observability services

- OCI Logging for tenancy-wide log collection
- OCI Monitoring for metrics and alarms
- OCI Audit for control-plane audit events
- OCI Streaming for event ingestion and decoupling
- Service Connector Hub or equivalent routing when metrics or logs need to flow into additional sinks

## Platform observability outcomes

- Trace agent and tool execution across the stack
- Correlate user requests with orchestration runs
- Monitor latency, error rates, retries, and saturation
- Track cost, token usage, and policy decisions
- Support operational dashboards and compliance evidence

## Collection strategy

Use a centralized collection and routing layer so the orchestrator, gateway, executors, tools, and backing resources emit telemetry into a consistent observability model.
