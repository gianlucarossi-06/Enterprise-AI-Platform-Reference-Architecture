# Integration Principles

## Principle 1 - Capability before implementation
The orchestrator and registry reason over business capabilities, not technical agent details.

## Principle 2 - One execution contract
All execution paths use the same canonical request, response, and callback model.

## Principle 3 - Gateway enforces, executors execute
The gateway validates, routes, and correlates; executors perform the work.

## Principle 4 - Tool and connector separation
A tool is the business-facing action; a connector is the technical integration.

## Principle 5 - Integration is a first-class service
Enterprise connectivity is handled by an AI Integration Service, not embedded inside the orchestrator.

## Principle 6 - Support both sync and async
Interactive requests, callbacks, queues, and workflow handoffs are all first-class.

## Principle 7 - Runtime state is managed
Long-running work requires checkpoints, retries, idempotency, and compensation.

## Principle 8 - MCP is optional
Model Context Protocol can be used where it fits, but it is not a platform dependency.

## Principle 9 - Observability and audit are mandatory
Every execution hop must remain traceable from user intent to resource access.

## Principle 10 - OCI is the reference implementation
The logical model stays vendor neutral; OCI services realize the physical deployment.
