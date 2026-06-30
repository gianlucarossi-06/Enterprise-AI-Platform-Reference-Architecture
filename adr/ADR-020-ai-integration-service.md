# ADR-020 AI Integration Service

## Status
Accepted

## Context
The execution plane needs a shared connectivity layer for SaaS, databases, APIs, streaming, files, and MCP-based integrations.

## Decision
The architecture introduces an AI Integration Service between tools and enterprise resources.

## Consequences
- connector logic becomes reusable across multiple agents
- orchestration stays isolated from technical integration details
- integration patterns can evolve independently of executor frameworks
