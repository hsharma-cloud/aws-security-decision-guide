# IAM Roles vs AWS STS

## Purpose

IAM Roles and AWS Security Token Service (STS) work together to provide secure, temporary access to AWS resources, but they are not the same. IAM Roles define **what permissions are available**, while AWS STS issues the **temporary security credentials** that allow trusted identities to assume those roles.

| Feature | IAM Roles | AWS STS |
|---------|-----------|----------|
| Primary Purpose | Define Permissions | Issue Temporary Credentials |
| Contains Permissions | Yes | No |
| Issues Credentials | No | Yes |
| Credential Type | N/A | Temporary Access Key, Secret Key, Session Token |
| Expiration | N/A | Configurable (Temporary) |
| Supports Cross-Account Access | Yes | Yes |
| Used By | Users, AWS Services, Applications | IAM Roles, Federation, Cross-Account Access |
| Typical Users | Security Administrators | AWS Services, Applications |

## Key Differences

- IAM Roles define **what actions are allowed**.
- AWS STS provides the **temporary credentials** used to perform those actions.
- Roles cannot be used until they are assumed.
- STS enables identities to assume roles securely.
- Nearly every IAM Role assumption involves AWS STS behind the scenes.

## When to Choose IAM Roles

Use IAM Roles when you need to:

- Define permissions for AWS services.
- Enable cross-account access.
- Grant least-privilege permissions.
- Eliminate long-term credentials.

## When to Choose AWS STS

Use AWS STS when you need to:

- Generate temporary credentials.
- Support federated identities.
- Enable secure role assumption.
- Provide short-lived access tokens.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Define permissions | **IAM Role** |
| Generate temporary credentials | **AWS STS** |
| Grant EC2 permissions | **IAM Role** |
| Enable role assumption | **AWS STS** |
| Control what an identity can do | **IAM Role** |
| Issue short-lived access keys | **AWS STS** |
