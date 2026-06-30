# MCP and Event-Driven Patterns

## MCP pattern

Model Context Protocol is useful where tools need a standardized way to expose context, resources, and actions. In this architecture, MCP is treated as an optional connector protocol rather than a mandatory platform foundation.

## Event-driven pattern

Agents can subscribe to business or technical events and react by invoking a capability. Event handling should remain separate from direct request/response orchestration.

## Callback pattern

Asynchronous work returns a callback registration and later posts a completion event to the runtime service or orchestrator.

## Design guidance

- use events for decoupling
- use callbacks for durable completion
- keep the callback payload canonical
- correlate every event with the same run identifier
