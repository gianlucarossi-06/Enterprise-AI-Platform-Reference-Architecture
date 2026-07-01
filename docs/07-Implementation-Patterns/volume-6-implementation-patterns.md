# Volume 6 - Implementation Patterns

## Table of contents

1. Executive summary
2. Pattern selection principles
3. Supervisor and orchestrator pattern
4. Hierarchical and federated agent patterns
5. Event-driven agent pattern
6. Human-in-the-loop pattern
7. Long-running workflow pattern
8. Multi-tenant pattern
9. Tool and connector pattern
10. Deployment automation references
11. Pattern selection matrix
12. Implementation considerations

## Executive summary

The implementation patterns volume captures repeatable design choices for building the platform in a consistent way. It translates the logical architecture into practical patterns for orchestration, execution, integration, and deployment automation.

## Pattern selection principles

- Prefer a small set of standard patterns.
- Keep the orchestrator capability-oriented.
- Use the gateway as the execution boundary.
- Separate tools from connectors.
- Select patterns that preserve observability and auditability.
- Default to automation and reproducibility.

## Supervisor and orchestrator pattern

The supervisor/orchestrator pattern centralizes planning, task decomposition, and capability selection. The orchestrator does not execute tools directly; it dispatches execution to the gateway and runtime services.

Use this pattern when tasks require multi-step reasoning, policy checks, and explicit traceability.

## Hierarchical and federated agent patterns

Hierarchical agents delegate specialized subtasks to subordinate agents. Federated agents collaborate across domains while maintaining their own runtime boundaries and tool access.

Use this pattern for complex domains that require specialization, such as finance, HR, supply chain, or operations.

## Event-driven agent pattern

Event-driven agents react to streaming events, state changes, or external triggers. The execution plane consumes messages from the platform event fabric and produces correlated outcomes and telemetry.

Use this pattern for asynchronous workflows, alerts, or background automation.

## Human-in-the-loop pattern

Sensitive requests may require approval before execution. The platform records approval requests, approvals, denials, and escalation outcomes as part of the canonical security and governance model.

Use this pattern for privileged data access, write actions, high-risk operations, or regulated workflows.

## Long-running workflow pattern

Long-running tasks are checkpointed and resumed through the runtime service. The platform stores state, retries, cancellation, and callback metadata separately from orchestration logic.

Use this pattern for workflows that exceed a single request-response cycle.

## Multi-tenant pattern

Multi-tenant deployments separate identity, policy, telemetry, and data access by tenant or business unit. The platform uses tenant-aware metadata and scoped resource boundaries.

Use this pattern when several business units share the same control plane.

## Tool and connector pattern

Tools expose business actions to agents. Connectors implement the technical access path to enterprise resources. This keeps agent logic independent from the details of each SaaS API, database driver, or event stream.

## Deployment automation references

Deployment automation uses repeatable artifacts for platform setup, environment promotion, configuration management, and release orchestration. The repository should contain the following automation references:

- documentation build scripts
- deployment profile examples
- OCI mapping tables
- policy libraries
- schema validation checks
- diagram generation hooks

The implementation pattern should always be reproducible and reviewable.

## Pattern selection matrix

| Pattern | Best used for | Main benefit |
|---|---|---|
| Supervisor and orchestrator | multi-step reasoning | central planning |
| Hierarchical agents | specialized subdomains | delegation |
| Event-driven agents | async triggers | decoupling |
| Human-in-the-loop | risky actions | safety |
| Long-running workflow | durable tasks | resilience |
| Multi-tenant | shared platform | isolation |
| Tool and connector | enterprise integration | portability |

## Implementation considerations

Implementation patterns should be introduced through ADRs so that the architecture stays stable while delivery teams can adopt different patterns intentionally.
