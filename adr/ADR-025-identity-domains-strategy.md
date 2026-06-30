# ADR-025 - Identity Domains Strategy

## Status

Accepted

## Context

The OCI physical architecture should use IAM with Identity Domains as the primary identity and SSO control plane for OCI-aligned deployments.

## Decision

Standardize on identity domains for authentication, SSO, identity lifecycle, and delegated administration, while allowing federation to enterprise identity providers.

## Consequences

Authentication and administration are centralized. Enterprise federation remains possible, but identity operations must be aligned to the OCI control plane.
