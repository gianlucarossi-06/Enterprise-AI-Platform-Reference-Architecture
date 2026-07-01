# Security Review Checklist

- [ ] User authentication is delegated to the identity provider and propagated as scoped context
- [ ] Orchestrator-to-gateway traffic is mutually authenticated
- [ ] Gateway enforces capability-level authorization
- [ ] Executor receives only short-lived delegated permissions
- [ ] Tools cannot bypass gateway or policy controls
- [ ] Resource access is constrained by database, SaaS, or API permissions
- [ ] All authentication and authorization decisions are logged
- [ ] Token exchange follows least privilege and audience restriction
- [ ] Sensitive payloads are masked or redacted where required
- [ ] Audit events are immutable and retained according to policy
- [ ] Approval workflows are triggered for sensitive or high-risk actions
- [ ] Security controls are versioned and mapped to ADRs

## Security review outcome

The architecture is ready for release when each item is demonstrably covered by logical design and OCI implementation guidance.

