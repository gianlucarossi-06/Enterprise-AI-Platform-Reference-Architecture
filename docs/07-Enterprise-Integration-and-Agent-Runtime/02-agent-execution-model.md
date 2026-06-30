# Agent Execution Model

A request starts as a user or application intent and becomes an execution request once the orchestrator selects a capability.

## Execution flow

1. User submits a request to the AI Orchestrator.
2. The orchestrator resolves the target capability and creates an execution request.
3. The AI Platform Kernel resolves policy, runtime state, and metadata.
4. The AI Agent Gateway validates the execution contract and chooses an executor.
5. The executor invokes one or more tools.
6. Tools call connectors or integration services.
7. Connectors access enterprise resources.
8. The response is normalized and returned to the orchestrator.

## Execution modes

- **Synchronous** - request/response for interactive work
- **Asynchronous** - callback or message-based completion
- **Event-driven** - reactions to events or state changes
- **Long-running** - checkpointed workflows with retries and compensation
- **Human-in-the-loop** - approval gates interrupt the flow before execution

## Runtime responsibilities

- preserve execution context and correlation IDs
- enforce delegated identity and policy scope
- track retries, idempotency, and timeout behavior
- emit telemetry and audit events at each hop
