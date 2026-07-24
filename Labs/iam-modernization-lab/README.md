# SecurePay IAM Modernization — Zero Trust Identity Architecture (Design Lab)

A Zero Trust identity architecture designed in Microsoft Entra ID for a fictional global fintech (SecurePay). This is a design/architecture exercise — the diagrams below are the deliverable, not screenshots of a live tenant.

## Scenario

SecurePay is a global fintech payment processor operating across the US, EU, and APAC, handling sensitive financial and PII data under PCI DSS, GDPR, and SOC 2 compliance drivers.

## Identity & Access Risks Identified

- Excessive privileges across teams
- No centralized identity governance
- Credential-based attack exposure
- Legacy authentication still enabled
- No periodic access reviews

## IAM Strategy

Microsoft Entra ID as the identity control plane, built around a Zero Trust security model: role-based access control (RBAC), Conditional Access enforcement, and automated identity governance. Access flows as Users → Groups → Roles → Applications, with identity treated as the primary security perimeter.

## Architecture Design

**Identity structure** — department-based groups, region-based groups, and admin-tier groups, with group-based access provisioning rather than individual grants (e.g., `SecurePay-Finance`, `SecurePay-US-Employees`).

<img width="824" height="126" alt="image" src="https://github.com/user-attachments/assets/d7d1bc81-8990-4ba7-8e5b-8f6b626ddf0c" />

**RBAC model** — least-privilege enforcement with roles assigned to groups, not individuals: Fraud → Fraud systems, Support → CRM only, Compliance → Compliance systems.

<img width="412" height="183" alt="image" src="https://github.com/user-attachments/assets/724f7045-4c57-443c-8b07-961e852bf9e6" />

**Application access model** — enterprise apps (Payment Gateway, Fraud Platform, CRM, Compliance System) integrated with Entra ID using group-based assignments for consistency.

<img width="425" height="235" alt="image" src="https://github.com/user-attachments/assets/115516a6-92ce-4d58-a6c4-c4964dd09e91" />

## Zero Trust Principles Applied

Verify explicitly (MFA, risk-based access) → enforce least privilege → assume breach, with Conditional Access as the enforcement layer.

## Security Controls Implemented

- MFA required for all users
- Legacy authentication blocked
- Admin accounts protected with Privileged Identity Management (PIM)
- Risk-based Conditional Access
- Device-based access restrictions

## Business Outcomes

- Reduced unauthorized access
- Stronger protection of financial data
- PCI DSS alignment
- Improved audit readiness
- Streamlined access lifecycle

## Skills Demonstrated

Microsoft Entra ID IAM architecture, RBAC design, Conditional Access configuration, Zero Trust implementation, identity lifecycle governance, cloud authentication hardening.

