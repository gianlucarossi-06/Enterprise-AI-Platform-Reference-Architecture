# Observability Principles

1. Observe at the orchestration boundary.
2. Correlate all signals with shared execution identifiers.
3. Capture logs, metrics, traces, lineage, and audit separately but join them logically.
4. Prefer structured telemetry over unstructured text.
5. Retain immutable audit evidence for compliance and forensics.
6. Redact sensitive payloads before export.
7. Make telemetry a platform service, not an agent-specific concern.
