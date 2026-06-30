# Network Architecture

The network design should isolate the control plane, execution plane, and enterprise resources while allowing controlled east-west and north-south traffic.

## Reference network zones

- Public ingress zone for API entry points and WAF
- Control plane private zone
- Execution plane private zone
- Shared services zone
- Data and resource zone
- Administrative access zone

## OCI network services and patterns

- OCI VCNs for isolated network domains
- Subnets for traffic segmentation
- Network Security Groups for workload-level controls
- DRG for hybrid connectivity
- Service Gateway for private access to OCI services
- NAT Gateway for controlled outbound access
- Bastion or equivalent controlled administrative access

## Network design goals

- No direct internet exposure for sensitive services
- Segregate ingress from internal execution traffic
- Restrict service-to-service access to least privilege
- Make private connectivity the default pattern
