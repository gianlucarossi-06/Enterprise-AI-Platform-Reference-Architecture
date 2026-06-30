# AI Integration Service

The AI Integration Service is the enterprise connectivity layer for the execution plane.

## Responsibilities

- route calls to enterprise systems
- translate agent tool requests into technical integrations
- handle protocol transformations
- standardize retries, circuit breakers, and compensation
- support sync and async integration styles
- manage event publication and callback registration
- isolate system-specific complexity from the agent runtime

## Integration styles

- REST and GraphQL
- JDBC and database APIs
- SaaS APIs
- file exchange
- streaming and pub/sub
- event callbacks
- message queues
- MCP-based integration

## Architectural placement

The integration service sits between tools and enterprise resources. It is shared by multiple executors and tools, so the same connector logic can be reused across agents and capabilities.
