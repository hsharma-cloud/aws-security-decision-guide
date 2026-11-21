# IAM Policies vs Service Control Policies (SCPs)

## Purpose

IAM Policies and Service Control Policies (SCPs) both define permissions in AWS, but they operate at different levels. IAM Policies grant or deny permissions to IAM users, groups, and roles within an AWS account, while SCPs establish the maximum permissions available to AWS accounts in an AWS Organization. SCPs do not grant permissions; they define the boundaries within which IAM permissions can operate.

| Feature | IAM Policies | Service Control Policies (SCPs) |
|---------|--------------|---------------------------------|
| Primary Purpose | Grant Permissions | Set Maximum Permissions |
| Scope | IAM Users, Groups, Roles | AWS Accounts and Organizational Units |
| Grants Permissions | Yes | No |
| Restricts Permissions | Yes (Explicit Deny) | Yes |
| Requires AWS Organizations | No | Yes |
| Applied To | IAM Identities | Accounts and OUs |
| Best For | Daily Access Management | Organizational Governance |
| Typical Users | IAM Administrators | Organization Administrators |

## Key Differences

- IAM Policies define **what identities can do**.
- SCPs define **what accounts are allowed to do**.
- IAM Policies grant permissions.
- SCPs never grant permissions—they only limit them.
- An action must be allowed by both the SCP and the IAM Policy to succeed.

## When to Choose IAM Policies

Use IAM Policies when you need to:

- Grant permissions to users or roles.
- Apply least privilege.
- Control access to AWS resources.
- Manage permissions within an AWS account.

## When to Choose SCPs

Use SCPs when you need to:

- Restrict permissions across multiple AWS accounts.
- Enforce organizational security standards.
- Prevent privileged actions.
- Govern accounts within AWS Organizations.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Grant S3 access to a user | **IAM Policy** |
| Prevent account administrators from deleting CloudTrail | **SCP** |
| Control permissions for a role | **IAM Policy** |
| Enforce organization-wide restrictions | **SCP** |
| Apply least privilege | **IAM Policy** |
| Govern multiple AWS accounts | **SCP** |
