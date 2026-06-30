# OCI Mapping

The observability model maps to OCI as follows:

| Logical capability | OCI service |
| --- | --- |
| telemetry ingestion | OCI Logging and custom endpoints |
| metrics and alarms | OCI Monitoring |
| distributed tracing | OCI APM or OpenTelemetry collectors on OKE |
| archival evidence | OCI Object Storage |
| event-driven alerts | OCI Events and Notifications |
| operational analytics | OCI Logging Analytics where applicable |

The recommended approach is to keep telemetry collection centralized in the platform and export to OCI services as the default observability backend.
