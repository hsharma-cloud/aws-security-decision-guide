# IAM Access Analyzer vs IAM Policy Simulator

## Purpose

IAM Access Analyzer and IAM Policy Simulator are IAM validation tools, but they solve different problems. IAM Access Analyzer identifies resources that are accessible from outside your AWS account or organization and helps detect unintended access, while IAM Policy Simulator evaluates IAM policies to determine whether a specific action will be allowed or denied before deploying permissions.

| Feature | IAM Access Analyzer | IAM Policy Simulator |
|---------|---------------------|----------------------|
| Primary Purpose | Detect External Access | Test IAM Permissions |
| Focus | Resource Exposure | Policy Evaluation |
| Uses Existing Resources | Yes | No |
| Tests Before Deployment | No | Yes |
| Cross-Account Analysis | Yes | No |
| Evaluates IAM Policies | Limited | Yes |
| Best For | Security Audits | Permission Troubleshooting |
| Typical Users | Security Engineers | IAM Administrators |

## Key Differences

- IAM Access Analyzer identifies **who can access your resources**.
- IAM Policy Simulator determines **whether an action will be allowed**.
- Access Analyzer detects unintended external sharing.
- Policy Simulator validates IAM policies before deployment.
- Both help implement least privilege but at different stages.

## When to Choose IAM Access Analyzer

Use IAM Access Analyzer when you need to:

- Detect publicly accessible resources.
- Find unintended cross-account access.
- Audit resource sharing.
- Improve security posture.

## When to Choose IAM Policy Simulator

Use IAM Policy Simulator when you need to:

- Test IAM policies.
- Verify least-privilege permissions.
- Troubleshoot access denied errors.
- Validate permission changes before deployment.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Find publicly shared resources | **IAM Access Analyzer** |
| Test an IAM policy | **IAM Policy Simulator** |
| Detect unintended external access | **IAM Access Analyzer** |
| Verify whether an action is allowed | **IAM Policy Simulator** |
| Audit cross-account permissions | **IAM Access Analyzer** |
| Troubleshoot permission issues | **IAM Policy Simulator** |
