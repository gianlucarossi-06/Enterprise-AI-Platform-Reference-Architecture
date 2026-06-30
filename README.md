# Enterprise AI Platform Reference Architecture

This repository contains the working reference architecture for a secure, governable, observable multi-agent AI platform.

## Contents

- `docs/01-Architecture-Foundation` - architecture vision, principles, logical model, AI Platform Kernel
- `docs/02-Security-Architecture` - authentication, authorization, identity propagation, token exchange
- `docs/04-Observability` - centralized telemetry, logging, tracing, lineage, alerting, audit correlation
- `docs/05-OCI-Reference-Implementation` - OCI mapping and physical implementation guidance
- `docs/06-Governance` - AI governance, lifecycle management, approvals, model and prompt governance
- `adr` - architecture decision records
- `schemas` - canonical JSON schemas
- `diagrams/drawio` - editable diagrams
- `diagrams/plantuml` - sequence and flow diagrams

## Architecture baseline

The architecture is capability-oriented and kernel-based:

User -> AI Orchestrator -> AI Platform Kernel -> AI Agent Gateway -> Agent Executors -> Tools -> Enterprise Resources

The control plane contains:
- AI Orchestrator
- AI Capability Registry
- AI Runtime Service
- AI Security Service
- AI Metadata Service
- AI Observability Service
- Audit Service

The execution plane contains:
- AI Agent Gateway
- Agent Executors
- Domain Agents
- Tool Adapters
- AI Integration Service

The platform uses centralized observability and cross-cutting governance so that telemetry, audit, policies, lifecycle controls, and approvals are managed consistently across all agents and tools.

The kernel provides shared enterprise services and keeps orchestration logic stateless and replaceable.

## Build

This repo is docs-as-code. Use Markdown as the source of truth.
