# VPC Flow Logs vs CloudTrail

## Purpose

Amazon VPC Flow Logs and AWS CloudTrail are logging services that capture different types of activity in AWS. VPC Flow Logs record network traffic metadata flowing to and from network interfaces within a VPC, helping analyze network connectivity and security. AWS CloudTrail records AWS API activity, showing who performed an action, when it occurred, and from where. Together, they provide visibility into both network activity and management operations.

| Feature | VPC Flow Logs | AWS CloudTrail |
|---------|---------------|----------------|
| Primary Purpose | Monitor Network Traffic | Audit AWS API Activity |
| Captures Network Connections | Yes | No |
| Records AWS API Calls | No | Yes |
| Captures User Activity | No | Yes |
| Supports Security Investigations | Yes | Yes |
| Data Source | Elastic Network Interfaces (ENIs) | AWS Services |
| Best For | Network Analysis | Governance and Compliance |
| Typical Users | Network & Security Engineers | Security & Compliance Teams |

## Key Differences

- VPC Flow Logs record **network traffic metadata**.
- CloudTrail records **AWS API activity**.
- VPC Flow Logs help identify network communication patterns.
- CloudTrail helps determine who performed AWS management actions.
- Security investigations often use both services together.

## When to Choose VPC Flow Logs

Use VPC Flow Logs when you need to:

- Analyze network traffic.
- Troubleshoot connectivity issues.
- Detect suspicious network communication.
- Verify security group and NACL behavior.
- Investigate network-related incidents.

## When to Choose CloudTrail

Use CloudTrail when you need to:

- Audit AWS API activity.
- Identify who modified AWS resources.
- Meet compliance requirements.
- Investigate administrative actions.
- Track IAM activity.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Determine whether traffic reached an EC2 instance | **VPC Flow Logs** |
| Identify who deleted a security group | **CloudTrail** |
| Troubleshoot VPC connectivity | **VPC Flow Logs** |
| Audit IAM API calls | **CloudTrail** |
| Analyze network communication patterns | **VPC Flow Logs** |
| Investigate AWS management actions | **CloudTrail** |
