# ADR-023 MCP as an optional protocol

## Status
Accepted

## Context
Some enterprise resources may expose capabilities through Model Context Protocol, but the platform must not depend on it.

## Decision
MCP is supported as one integration option, not as a mandatory platform dependency.

## Consequences
- the architecture remains framework-neutral
- existing REST, JDBC, event, and file integrations continue to work
- new MCP connectors can be added where useful
