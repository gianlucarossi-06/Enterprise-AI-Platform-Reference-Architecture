# Policy Enforcement Points

## Orchestrator
Checks whether the user can request the capability.

## Gateway
Checks whether the selected capability and implementation are eligible for the user and tenant.

## Executor
Checks whether the selected task may use the required tool or adapter.

## Tool
Checks whether the requested operation is allowed on the target resource.

## Resource
Checks row, column, object, API, or action permissions using native security controls.

The policy enforcement architecture follows a PEP/PDP pattern, where the policy decision point can be implemented as a centralized service and the enforcement points remain distributed.
