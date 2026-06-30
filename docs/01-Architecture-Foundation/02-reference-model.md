# 02 Reference Model and Terminology

## Architectural domains

### User Experience Plane
Human users, client applications, copilots, and API consumers.

### AI Platform Control Plane
AI Orchestrator, AI Capability Registry, AI Runtime Service, AI Security Service, AI Metadata Service, AI Observability Service, and Audit Service.

### AI Execution Plane
AI Agent Gateway, Agent Executors, Domain Agents, and Tool Adapters.

### Enterprise Resource Plane
Enterprise databases, SaaS systems, REST APIs, files, knowledge sources, and other systems of record.

### Platform Services Plane
Cloud services, networking, identity, storage, security, and observability primitives.

## Core terminology

- **Capability** - a business outcome or functional service the platform can deliver.
- **Capability implementation** - one concrete agent runtime that can realize a capability.
- **Execution context** - the runtime envelope that carries user identity, task state, trace identifiers, and policy decisions.
- **Agent executor** - the runtime responsible for executing a selected agent implementation.
- **Tool adapter** - the abstraction that connects an agent to a database, API, or enterprise system.
- **Resource** - the protected enterprise asset accessed by a tool.
