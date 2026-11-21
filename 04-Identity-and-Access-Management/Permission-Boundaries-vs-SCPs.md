# Permission Boundaries vs Service Control Policies (SCPs)

## Purpose

Permission Boundaries and Service Control Policies (SCPs) both limit permissions in AWS, but they operate at different levels. Permission Boundaries define the maximum permissions that an IAM user or role can receive, while SCPs define the maximum permissions available to AWS accounts within an AWS Organization. Neither grants permissions—they only establish permission boundaries.

| Feature | Permission Boundaries | Service Control Policies (SCPs) |
|---------|-----------------------|---------------------------------|
| Primary Purpose | Limit IAM Identity Permissions | Limit AWS Account Permissions |
| Scope | IAM Users and Roles | AWS Accounts and Organizational Units |
| Grants Permissions | No | No |
| Restricts Permissions | Yes | Yes |
| Requires AWS Organizations | No | Yes |
| Applied To | IAM Identities | Accounts and OUs |
| Best For | Delegated Administration | Organization Governance |
| Typical Users | IAM Administrators | Organization Administrators |

## Key Differences

- Permission Boundaries restrict **individual IAM identities**.
- SCPs restrict **entire AWS accounts**.
- Permission Boundaries are commonly used when delegating IAM administration.
- SCPs enforce organization-wide security guardrails.
- A request must be allowed by the SCP, Permission Boundary (if present), and IAM Policy to succeed.

## When to Choose Permission Boundaries

Use Permission Boundaries when you need to:

- Delegate IAM administration safely.
- Limit permissions that developers can assign.
- Prevent privilege escalation.
- Control the maximum permissions of IAM users or roles.

## When to Choose SCPs

Use SCPs when you need to:

- Govern multiple AWS accounts.
- Enforce enterprise-wide security policies.
- Block high-risk AWS services.
- Restrict actions across Organizational Units (OUs).

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Limit what a developer-created role can do | **Permission Boundary** |
| Restrict every account in an OU | **SCP** |
| Delegate IAM administration | **Permission Boundary** |
| Enforce organization-wide guardrails | **SCP** |
| Prevent privilege escalation | **Permission Boundary** |
| Govern multiple AWS accounts | **SCP** |
