# 07 Canonical Contracts

The platform uses canonical contracts to avoid coupling between components.

## Control contract
Between the user experience layer and the orchestrator. Carries intent, request context, and business purpose.

## Execution contract
Between the orchestrator, gateway, and executor. Carries task state, capability reference, identity context, and policy context.

## Tool contract
Between an executor and a tool adapter. Carries operation, target resource, allowed scope, and expected outcome.

## Resource contract
Between the tool adapter and the enterprise resource. Carries the resource request, authorization scope, and response envelope.

## Telemetry contract
Every component emits telemetry events with run, task, agent, tool, and correlation identifiers.

## Audit contract
Security and compliance relevant events are emitted as immutable audit records.
