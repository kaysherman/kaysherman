# SecureTech IAM Strategy — Zero Trust Security Proposal

A written Zero Trust IAM strategy proposal developed for a hybrid cloud environment (coursework, Capella University). No screenshots — this is a strategic/policy document, not a hands-on console lab.

## Executive Summary

Hybrid cloud environment spanning AWS, Azure, and on-premises infrastructure, where identity is the primary attack surface. Proposes a combined Zero Trust, passwordless, and MFA strategy.

## Key IAM Challenges Identified

- Identity enumeration and credential abuse
- Privilege sprawl
- Fragmented identity stores
- Implicit trust in internal networks
- Vendor and API risk
- Limited monitoring

## Recommendations

**Zero Trust identity controls** — passwordless authentication (FIDO2), biometric authentication, Conditional Access, continuous authentication, a unified identity provider.

**Privileged access modernization** — least-privilege access, Just-in-Time (JIT) access, automated access reviews, identity-based segmentation.

**Centralized identity governance** — a federated identity provider, standardized policies, unified risk scoring, improved visibility.

**Micro-segmentation strategy** — identity-based access control, IoT VLAN isolation, mutual TLS for internal traffic.

**Vendor and API security** — decentralized identity (DID), verifiable credentials, certificate-based authentication.

**AI-driven IAM monitoring** — User and Entity Behavior Analytics (UEBA), SIEM integration, continuous monitoring, ML baseline updates.

## Implementation Roadmap

1. **Phase 1** — Identity consolidation + MFA
2. **Phase 2** — Zero Trust + segmentation
3. **Phase 3** — JIT access + AI-driven monitoring

## Business Impact

Reduced identity-based attacks, a stronger compliance posture, improved visibility, and secure hybrid cloud operations.

## Skills Demonstrated

Security architecture analysis, identity governance, IoT security controls, threat modeling, incident response planning, policy development, compliance alignment, implementation roadmap design.

