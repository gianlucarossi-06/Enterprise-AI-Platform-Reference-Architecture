# OCI Design Principles

The OCI implementation strategy is guided by the following principles.

## Managed service first

Use OCI managed services wherever they satisfy the requirement. This reduces operational complexity and improves standardization.

## Control plane and execution plane separation

Keep orchestration, security, registry, runtime state, and observability separated from agent execution and resource access.

## Identity propagation without credential leakage

Propagate delegated identity and scoped execution context rather than forwarding user passwords or broad bearer credentials downstream.

## Least privilege

Grant each hop only the minimum permissions needed to perform its function.

## Contract-first integration

Use explicit request, response, identity, and policy contracts between services.

## Observable by default

Emit logs, metrics, traces, and audit events from every platform layer.

## Multi-region ready

Design the platform so that availability, recovery, and regional placement can be adapted to customer requirements.

## OCI optimized, but not OCI locked

Use OCI as the physical reference implementation while keeping the logical architecture portable.
