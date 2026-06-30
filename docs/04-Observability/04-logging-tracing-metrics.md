# Logging, Tracing, and Metrics

## Logging
Structured logs capture state transitions, errors, denials, retries, and policy decisions. Logs should be JSON and should include correlation identifiers.

## Tracing
Distributed traces capture the end-to-end execution path across orchestration, gateway, execution, tools, and resource access.

## Metrics
Metrics capture platform health and demand: request rate, success rate, latency, tool utilization, retries, denials, queue depth, and memory or token consumption.

A centralized observability service can export telemetry to OCI Logging, OCI Monitoring, OCI APM, or third-party tools such as Grafana, Loki, Tempo, or Prometheus when required.
