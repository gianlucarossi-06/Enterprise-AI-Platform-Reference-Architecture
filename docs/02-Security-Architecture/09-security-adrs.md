# Security ADRs

## ADR-011 Security by design
Security controls are treated as platform requirements, not application additions.

## ADR-012 Delegated identity propagation
User identity is propagated through the stack as delegated, scoped context.

## ADR-013 Scoped token exchange
Each layer receives a short-lived token with reduced audience and privilege.

## ADR-014 Layered authorization
Authorization is enforced at orchestrator, gateway, executor, tool, and resource layers.

## ADR-015 Tool isolation
Tools must not bypass resource-native access controls.

## ADR-016 Immutable security audit
All security decisions are emitted as audit events.

## ADR-017 OCI security reference implementation
OCI IAM, API Gateway, Vault, Logging, Audit, and OKE form the reference implementation surface.

## ADR-018 Separate authentication and authorization
Authentication validates identity; authorization evaluates permission.

## ADR-019 Central policy with distributed enforcement
The policy decision point may be centralized, while enforcement remains close to execution.

## ADR-020 Trust boundary verification
Every hop validates context before execution.
