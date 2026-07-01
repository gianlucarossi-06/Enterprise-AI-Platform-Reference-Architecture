# Platform Engineering and GitOps

GitOps is the preferred model for platform change. Platform configuration, deployment manifests, policy files, and release promotion metadata are versioned in Git and reconciled to the target environment by automation.

Recommended elements:
- source control for manifests and policy
- pull-request based approvals
- environment overlays
- automated validation
- drift detection
- promotion gates
- auditable release history
