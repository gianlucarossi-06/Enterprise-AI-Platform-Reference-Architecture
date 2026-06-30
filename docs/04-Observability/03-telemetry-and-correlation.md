# Telemetry and Correlation

Every execution begins with a run ID and a trace ID at the orchestrator. The gateway propagates the context downstream, and each executor and tool adapter creates child spans or correlated events.

The key correlation identifiers are:

- tenant ID
- user ID
- session ID
- run ID
- task ID
- capability ID
- agent ID
- tool ID
- resource ID
- policy decision ID

Correlation allows the platform to reconstruct the full chain of custody for a request, including who asked, which capability was selected, which agent executed it, which tools were invoked, and which resource was accessed.
