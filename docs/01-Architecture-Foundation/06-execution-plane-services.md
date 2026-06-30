# 06 Execution Plane Services

## AI Agent Gateway
Single execution entry point for downstream agent runtimes. It validates requests, enforces policy, resolves routing, and emits execution telemetry.

## Agent Executors
Runtime components that execute agent logic in a specific framework or runtime.

## Domain Agents
Independent agents owned by different domains, teams, or platforms.

## Tool Adapters
Protocol and semantic adapters that connect agents to enterprise resources such as databases, APIs, SaaS systems, file stores, or knowledge services.

## Execution rules

- Every request is bound to a run identifier.
- Every tool invocation is bound to the delegated identity and policy context.
- Every response is normalized before it is returned to the orchestrator.
