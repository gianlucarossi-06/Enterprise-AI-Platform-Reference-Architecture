# Identity and Trust Model

## Identity sources

The platform accepts identity from an enterprise identity provider using federation protocols such as OIDC, OAuth2, or SAML.

## Trusted actors

- end user
- orchestrator
- gateway
- executor
- tool adapter
- enterprise resource

## Trust boundaries

Each component validates:
- token signature or assertion
- token audience
- expiration
- tenant scope
- requested capability
- approval state
- policy decision context

## Chain of custody

The user identity becomes a delegated execution identity. It is never silently replaced by a broad service account. Instead, every step carries a bounded, auditable context.
