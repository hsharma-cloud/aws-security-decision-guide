# CloudTrail vs CloudWatch

## Purpose

AWS CloudTrail and Amazon CloudWatch are complementary services that provide visibility into AWS environments. CloudTrail focuses on auditing AWS API activity, while CloudWatch focuses on monitoring the health, performance, and operational status of AWS resources and applications.

| Feature | AWS CloudTrail | Amazon CloudWatch |
|---------|----------------|-------------------|
| Primary Purpose | Audit AWS API activity | Monitor AWS resources and applications |
| Data Collected | AWS API calls and account activity | Metrics, logs, events, and alarms |
| Focus | Who performed an action | What is happening to resources |
| Data Source | AWS API requests | AWS services, applications, operating systems, and custom metrics |
| Monitoring | Near real-time event logging | Real-time monitoring |
| Alerts | Requires integration with EventBridge or CloudWatch | Native CloudWatch Alarms |
| Primary Users | Security, Compliance, Auditors | Operations, DevOps, Cloud Engineers |

## Key Differences

- CloudTrail records **who did what, when, and from where**.
- CloudWatch monitors **resource health, performance, and operational metrics**.
- CloudTrail supports auditing, compliance, and forensic investigations.
- CloudWatch provides dashboards, alarms, and operational monitoring.
- Both services are commonly used together as part of a comprehensive monitoring strategy.

## When to Choose CloudTrail

Choose CloudTrail when you need to:

- Audit AWS account activity.
- Investigate security incidents.
- Track configuration changes.
- Meet compliance and governance requirements.

## When to Choose CloudWatch

Choose CloudWatch when you need to:

- Monitor application and infrastructure health.
- Create alerts based on metrics or logs.
- Visualize performance using dashboards.
- Monitor operational trends over time.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Know who performed an AWS action | **CloudTrail** |
| Monitor application or infrastructure health | **CloudWatch** |
| Investigate AWS API activity | **CloudTrail** |
| Generate alerts from metrics or logs | **CloudWatch** |
| Support auditing and compliance | **CloudTrail** |
| Build dashboards and monitor performance | **CloudWatch** |
