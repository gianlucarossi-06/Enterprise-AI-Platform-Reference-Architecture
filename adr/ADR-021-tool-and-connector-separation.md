# ADR-021 Tool and connector separation

## Status
Accepted

## Context
The architecture needs a stable business-facing action model without exposing technical integration details to orchestrators.

## Decision
A tool represents the business action and a connector implements the technical integration.

## Consequences
- business language remains visible in orchestration
- connector changes do not force orchestration changes
- integration logic can be standardized
