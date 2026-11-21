# AWS Config vs CloudTrail

## Purpose

AWS Config and AWS CloudTrail provide visibility into AWS environments but answer different questions. AWS Config tracks the configuration and compliance state of AWS resources over time, while AWS CloudTrail records API activity and user actions performed within an AWS account.

| Feature | AWS Config | AWS CloudTrail |
|---------|------------|----------------|
| Primary Purpose | Configuration Management | API Auditing |
| Focus | Resource configuration and compliance | User and service activity |
| Records | Resource configurations and changes | AWS API calls |
| Tracks Who Made Changes | No | Yes |
| Compliance Evaluation | Yes | No |
| Historical Configuration | Yes | No |
| Typical Users | Governance, Compliance, Security Teams | Security, Auditors, Incident Response |

## Key Differences

- Config answers **"What changed?"**
- CloudTrail answers **"Who changed it?"**
- Config continuously evaluates compliance.
- CloudTrail records API activity for auditing and investigations.
- Both services are commonly used together for governance and forensic analysis.

## When to Choose AWS Config

Use AWS Config when you need to:

- Monitor resource configuration changes.
- Evaluate compliance against policies.
- Track configuration history.
- Detect configuration drift.

## When to Choose CloudTrail

Use CloudTrail when you need to:

- Audit AWS API activity.
- Investigate security incidents.
- Identify who created, modified, or deleted resources.
- Meet auditing requirements.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Track resource configurations | **AWS Config** |
| Audit API activity | **AWS CloudTrail** |
| Monitor compliance | **AWS Config** |
| Identify who made a change | **AWS CloudTrail** |
| Detect configuration drift | **AWS Config** |
| Investigate account activity | **AWS CloudTrail** |
