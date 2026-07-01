# Long-Running Workflows

Some capabilities cannot complete in one interaction. They require checkpoints, durable state, and eventual completion.

## Required features

- workflow state persistence
- idempotency keys
- retry policies
- compensation actions
- pause and resume
- human approval gates
- replay for troubleshooting

## State model

The runtime service stores the workflow state, while the gateway and executors remain stateless enough to scale horizontally.

## Design guidance

Long-running workflows should never rely on in-memory executor state alone. Durability is mandatory for recoverability and governance.
