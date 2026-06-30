# 04 Logical Architecture

## Logical flow

User -> AI Orchestrator -> AI Platform Kernel -> AI Agent Gateway -> Agent Executors -> Tool Adapters -> Enterprise Resources

## Logical layers

### User Experience Plane
Entry points for human and application consumers.

### AI Platform Control Plane
Determines what capability is needed, what policy applies, and what execution context should be created.

### AI Execution Plane
Performs the actual agent and tool execution.

### Enterprise Resource Plane
Contains the protected enterprise systems that expose data or operations.

### Platform Services Plane
Provides cloud infrastructure services that host and support the platform.

## Architectural behavior

- The orchestrator selects a capability.
- The registry resolves one or more eligible implementations.
- The security service authorizes the request and propagates delegated identity.
- The gateway mediates execution, routing, and protocol translation.
- The executor runs the agent.
- Tool adapters access enterprise resources using scoped permissions.
- The observability service records the full execution chain.
