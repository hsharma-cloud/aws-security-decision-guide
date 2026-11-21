# CloudTrail vs AWS Config

## Purpose

AWS CloudTrail and AWS Config are governance and security services that provide visibility into your AWS environment, but they capture different types of information. CloudTrail records AWS API activity, showing who performed an action, when it occurred, and from where. AWS Config records the configuration of AWS resources over time, allowing you to track configuration changes, evaluate compliance, and determine the state of resources at any point in time.

| Feature | AWS CloudTrail | AWS Config |
|---------|----------------|------------|
| Primary Purpose | Audit AWS API Activity | Track Resource Configuration |
| Records API Calls | Yes | No |
| Tracks Resource Configuration | No | Yes |
| Tracks Configuration Changes | Limited | Yes |
| Compliance Evaluation | No | Yes |
| Historical Resource State | No | Yes |
| Best For | Security Auditing | Configuration Management |
| Typical Users | Security & Compliance Teams | Cloud Engineers & Compliance Teams |

## Key Differences

- CloudTrail records **who performed an action**.
- AWS Config records **what changed in the resource configuration**.
- CloudTrail focuses on API activity and user actions.
- AWS Config focuses on resource inventory, configuration history, and compliance.
- The two services are commonly used together during security investigations.

## When to Choose CloudTrail

Use CloudTrail when you need to:

- Audit AWS API activity.
- Investigate security incidents.
- Track IAM and administrative actions.
- Meet audit and compliance requirements.
- Identify who performed a specific action.

## When to Choose AWS Config

Use AWS Config when you need to:

- Track resource configuration changes.
- Evaluate compliance against rules.
- Maintain a resource inventory.
- Determine the configuration of a resource at a specific point in time.
- Detect configuration drift.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Identify who deleted an EC2 instance | **CloudTrail** |
| Determine when a security group rule changed | **AWS Config** |
| Audit IAM user activity | **CloudTrail** |
| Evaluate compliance with configuration rules | **AWS Config** |
| Investigate API calls | **CloudTrail** |
| View the configuration history of an S3 bucket | **AWS Config** |
