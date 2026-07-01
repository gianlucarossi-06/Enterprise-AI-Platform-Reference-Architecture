# Volume 3 - Canonical Models

## Table of contents

1. Executive summary
2. Canonical model principles
3. Reference entity model
4. Execution and conversation model
5. Identity and delegation model
6. Capability and agent model
7. Tool and connector model
8. Security model
9. Observability model
10. Governance model
11. Schema catalog and usage
12. Implementation considerations

## Executive summary

The canonical models volume defines the shared language of the Enterprise AI Platform Reference Architecture. It prevents each service, agent framework, or integration layer from inventing its own representation of execution, identity, policy, telemetry, or governance state.

## Canonical model principles

- Define once, reuse everywhere.
- Model business intent separately from execution mechanics.
- Keep identifiers stable and human-readable where appropriate.
- Represent security and audit context as first-class data.
- Keep schemas versioned and backward compatible.

## Reference entity model

The platform centers on a small set of entities:

- User
- Conversation
- Run
- Task
- Capability
- Agent
- Agent Implementation
- Tool
- Connector
- Policy Decision
- Approval
- Telemetry Event
- Audit Event
- Resource Access

These entities are linked by execution context and security context so that the platform can trace who asked for what, which capability was selected, what was executed, and what resource was accessed.

## Execution and conversation model

A user request creates a conversation, which may contain multiple runs. Each run may contain one or more tasks. Tasks may decompose into subtasks, retries, approvals, and asynchronous callbacks.

The canonical execution model uses the following lifecycle:

Request -> Accept -> Plan -> Authorize -> Dispatch -> Execute -> Observe -> Correlate -> Complete

## Identity and delegation model

The canonical identity model preserves the user identity, the orchestrator identity, the gateway identity, the executor identity, and the tool identity. Each hop receives only the minimum context required to complete the next action.

Important fields include:

- user identifier
- tenant identifier
- session identifier
- run identifier
- delegated scopes
- authentication strength
- approval state
- expiration
- audience

## Capability and agent model

Capabilities describe business intent. Agents implement capabilities. Implementations may vary by vendor, model, framework, region, or runtime.

This separation keeps the orchestrator capability-oriented and allows the registry to map capabilities to one or more implementations.

## Tool and connector model

Tools represent business operations exposed to agents. Connectors represent the technical path to external systems.

A tool may use one or more connectors, and a connector may support multiple tools if the contract is compatible.

## Security model

Security is represented as data, not as an assumption. The canonical security model includes:

- authenticated identity
- delegated identity
- authorization decision
- scope
- approval
- trust boundary
- token exchange
- resource access request

## Observability model

Observability entities include trace envelopes, metric events, log events, audit correlation identifiers, and lineage markers for prompts, capabilities, tools, and resources.

## Governance model

Governance entities include capability lifecycle state, model governance metadata, prompt governance metadata, policy changes, and approval decisions.

## Schema catalog and usage

The JSON schemas under `schemas/canonical-models` define the machine-readable version of the canonical model. They are the source for API contracts, event payloads, and implementation patterns.

## Implementation considerations

Canonical models should be:

- versioned
- validated
- documented
- stable across services
- compatible with backward migration

The repository uses these models to avoid semantic drift across documents, diagrams, schemas, and automation.
