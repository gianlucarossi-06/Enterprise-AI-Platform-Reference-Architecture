# Alerting and Detection

Alerting should be driven by user impact, platform health, and security risk.

Typical alert categories:

- failed authentication or authorization patterns
- policy violations or repeated denials
- agent failures or tool failure spikes
- unusual latency or saturation
- cost anomalies or token spikes
- missing telemetry from critical services

Detection rules should be managed centrally and tied to the same execution identifiers used by traces and logs.
