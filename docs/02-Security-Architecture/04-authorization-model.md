# Authorization Model

Authorization is evaluated as an intersection of policies.

## Layers

- user entitlement
- tenant entitlement
- capability entitlement
- agent implementation entitlement
- tool entitlement
- resource entitlement

## Decision types

- allow
- deny
- allow with conditions
- require approval
- require step-up authentication

## Policy inputs

- user subject
- groups and roles
- tenant
- capability
- data classification
- environment
- time
- region
- risk score
- approval state
