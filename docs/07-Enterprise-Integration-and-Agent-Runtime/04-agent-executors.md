# Agent Executors

Agent executors are runtime-specific components that perform the work requested by the gateway.

## Executor types

- **Framework executor** - runs a framework such as LangGraph, Semantic Kernel, or CrewAI
- **Container executor** - runs a packaged agent in OCI OKE
- **Function executor** - runs a stateless agent step in OCI Functions
- **Workflow executor** - runs orchestrated steps with durable state
- **Connector executor** - wraps a technical integration with a stable contract

## Responsibilities

- load the execution context
- call tools in the required order
- preserve correlation and identity context
- support retry, timeout, and compensation rules
- publish intermediate state to the runtime service
- return normalized results to the gateway

## Design guidance

Executors should remain thin. They should not duplicate gateway policy or orchestrator planning. Their role is to execute a capability in a specific runtime with predictable behavior.
