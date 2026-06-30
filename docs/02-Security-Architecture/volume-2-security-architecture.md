# Volume 2 - Security Architecture

## Table of contents

1. Executive summary
2. Security principles and assumptions
3. Identity and trust model
4. Authentication flow
5. Authorization model
6. Token exchange and propagation
7. Policy enforcement points
8. Tool and resource authorization
9. OCI security mapping
10. Security ADRs

## Executive summary

The security architecture establishes how a user request is authenticated at the platform edge and how identity, authorization state, and security context are propagated through the AI Orchestrator, AI Agent Gateway, AI Agent Executors, AI Tools, and enterprise resources.

The design uses delegated identity, short-lived scoped tokens, policy enforcement points at each hop, and immutable audit events for all security-relevant decisions.

## Security principles and assumptions

- Zero Trust: no layer trusts the previous layer without verification.
- Least privilege: every token carries the smallest required scope.
- Explicit delegation: downstream access is granted only by scoped delegation, never by implicit inheritance.
- Policy as code: authorization decisions are deterministic and auditable.
- Defense in depth: orchestration, gateway, executor, tool, and resource all enforce controls.
- Auditability: every allow, deny, retry, and escalation is recorded.
- Separation of duties: security policy is distinct from orchestration logic.

## Identity and trust model

A user authenticates once through the enterprise identity provider. The orchestrator receives a validated identity assertion and translates it into an execution context. The gateway and executors then consume a delegated token or signed context that identifies:

- subject
- tenant
- groups and roles
- requested capability
- data classification
- approval state
- trace and run identifiers

The trust chain is therefore:

User -> Identity Provider -> Orchestrator -> Gateway -> Executor -> Tool -> Resource

Each hop revalidates the security context before acting.

## Authentication flow

The orchestrator accepts a request only after validating the user identity token. The token can be an OIDC ID token, OAuth2 access token, or a federated SSO assertion.

Authentication outcome:
- authenticated subject
- tenant membership
- coarse-grained roles
- session validity
- MFA strength, if present
- token expiry

Authentication is not sufficient for execution. It is the starting point for authorization.

## Authorization model

Authorization is evaluated at multiple levels:

- **Platform authorization** - is the user allowed to use the AI platform?
- **Capability authorization** - is the user allowed to invoke the capability selected by the orchestrator?
- **Agent authorization** - is the user allowed to use the concrete implementation resolved by the registry and gateway?
- **Tool authorization** - is the user allowed to call this tool for this action?
- **Resource authorization** - is the user allowed to read or mutate the backing data or API?

The effective access decision is the intersection of user entitlement, tenant policy, capability policy, tool policy, and resource policy.

## Token exchange and propagation

The security chain relies on short-lived tokens:
- user token
- orchestration execution token
- gateway token
- executor token
- tool token
- resource token

Each token is audience-restricted, time-bound, and scope-limited. Token exchange is used to down-scope privilege as the request moves deeper into the platform.

## Policy enforcement points

Policy enforcement is distributed across the stack.

- The orchestrator enforces coarse task eligibility.
- The gateway enforces capability routing and delegated access.
- The executor enforces task-level tool selection.
- The tool adapter enforces operation-level constraints.
- The resource layer enforces database, API, or SaaS-native permissions.

## Tool and resource authorization

A tool adapter is never allowed to bypass the underlying resource policy.

Examples:
- a database tool may query only approved schemas, views, and columns
- a REST tool may invoke only approved endpoints and HTTP methods
- a file tool may access only approved buckets, folders, or objects
- a SaaS connector may access only approved business objects

This prevents an overly-permissioned tool from becoming a security backdoor.

## OCI security mapping

The logical security architecture can be realized on OCI with:
- OCI IAM / Identity Domains for federation and authentication
- OCI API Gateway for secure northbound ingress and request mediation
- OCI Vault for secrets, keys, and certificates
- OCI Certificates for certificate lifecycle
- OCI Logging and Audit for centralized auditability
- OCI Security Zones and network segmentation for boundary control
- OCI OKE for policy-aware gateway or executor services when needed

## Security ADRs

The security ADRs formalize decisions on delegated identity, scoped token exchange, layered authorization, tool isolation, audit, and OCI mapping.
