# Authentication Flow

1. The user signs in to the enterprise identity provider.
2. The user receives a federated token or session assertion.
3. The orchestrator validates the token and creates an execution context.
4. The orchestrator records the user subject, tenant, and session.
5. The orchestrator starts policy evaluation for the requested capability.

Authentication answers the question: **who is the user?**
