# Token Exchange and Propagation

The platform uses short-lived scoped tokens to move from broad platform access to fine-grained execution permissions.

## Token chain

- user token
- orchestration token
- gateway token
- executor token
- tool token
- resource token

## Rules

- each token is audience-restricted
- each token expires quickly
- each exchange reduces scope
- each token is traceable to the original user subject
- each token is linked to a policy decision identifier

## Result

The platform preserves identity while minimizing privilege.
