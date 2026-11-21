# CloudTrail vs CloudWatch

## Purpose

AWS CloudTrail and Amazon CloudWatch are complementary monitoring services, but they focus on different aspects of AWS environments. CloudTrail records AWS API activity for governance, compliance, and security auditing, while CloudWatch monitors operational health through metrics, logs, events, dashboards, and alarms. Together, they provide complete visibility into both security and operational performance.

| Feature | AWS CloudTrail | Amazon CloudWatch |
|---------|----------------|-------------------|
| Primary Purpose | Audit AWS API Activity | Monitor AWS Resources and Applications |
| Records API Calls | Yes | No |
| Collects Metrics | No | Yes |
| Collects Logs | Limited (API Events) | Yes |
| Creates Alarms | No | Yes |
| Compliance Auditing | Yes | Limited |
| Operational Monitoring | Limited | Yes |
| Typical Users | Security & Compliance Teams | Operations & DevOps Teams |

## Key Differences

- CloudTrail records **who did what, when, and from where**.
- CloudWatch monitors **how AWS resources and applications are performing**.
- CloudTrail focuses on auditing and governance.
- CloudWatch focuses on monitoring, alerting, and operational visibility.
- CloudTrail logs can be sent to CloudWatch Logs for real-time monitoring and alerting.

## When to Choose CloudTrail

Use CloudTrail when you need to:

- Audit AWS API activity.
- Investigate security incidents.
- Meet compliance requirements.
- Track configuration changes.
- Monitor user and service actions.

## When to Choose CloudWatch

Use CloudWatch when you need to:

- Monitor CPU, memory, and application metrics.
- Collect application and system logs.
- Create alarms and dashboards.
- Detect operational issues.
- Monitor application performance.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Determine who deleted an S3 bucket | **CloudTrail** |
| Alert when EC2 CPU exceeds 80% | **CloudWatch** |
| Audit IAM activity | **CloudTrail** |
| Monitor application logs | **CloudWatch** |
| Meet compliance requirements | **CloudTrail** |
| Build operational dashboards | **CloudWatch** |
