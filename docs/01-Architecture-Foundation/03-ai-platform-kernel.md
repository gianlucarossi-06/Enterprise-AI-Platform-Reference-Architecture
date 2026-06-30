# 03 AI Platform Kernel

The AI Platform Kernel is the logical foundation of the platform. It hosts shared platform capabilities that must be consistent across all agent implementations.

## Kernel services

- **AI Capability Registry** - stores capabilities, implementations, versions, trust level, owners, and supported tools.
- **AI Runtime Service** - stores run state, task graph, checkpoints, approvals, and correlation identifiers.
- **AI Security Service** - performs authentication, authorization, delegation, token exchange, and approval checks.
- **AI Metadata Service** - manages prompts, tool definitions, model metadata, semantic tags, and knowledge source metadata.
- **AI Observability Service** - correlates traces, logs, metrics, audit, lineage, and cost.
- **Audit Service** - stores immutable evidence of identity, access, policy, and execution events.

## Design intent

The kernel keeps the platform stable while allowing orchestrators, agents, and execution frameworks to evolve independently.

## Key rule

The orchestrator must not own persistent platform state that belongs in the kernel.
