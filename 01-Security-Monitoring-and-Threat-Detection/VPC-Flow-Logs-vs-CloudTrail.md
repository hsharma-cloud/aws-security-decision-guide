# VPC Flow Logs vs CloudTrail

## Purpose

Amazon VPC Flow Logs and AWS CloudTrail provide visibility into AWS environments from different perspectives. VPC Flow Logs capture network traffic metadata flowing into and out of network interfaces, while AWS CloudTrail records API activity performed by users, services, and applications within an AWS account.

| Feature | Amazon VPC Flow Logs | AWS CloudTrail |
|---------|----------------------|----------------|
| Primary Purpose | Network Traffic Monitoring | API Activity Auditing |
| Focus | Network connections | AWS API calls |
| Records | IP traffic metadata | User and service actions |
| Captures Packet Payload | No | No |
| Shows Who Performed an Action | No | Yes |
| Typical Use Cases | Network troubleshooting, threat detection | Auditing, compliance, forensic investigations |
| Typical Users | Network Engineers, Security Analysts | Security Teams, Auditors, Incident Responders |

## Key Differences

- VPC Flow Logs answer **"What network traffic occurred?"**
- CloudTrail answers **"Who performed an AWS action?"**
- VPC Flow Logs monitor network communication.
- CloudTrail monitors AWS management and data plane API activity.
- Both services complement each other during incident investigations.

## When to Choose VPC Flow Logs

Use VPC Flow Logs when you need to:

- Analyze network traffic.
- Investigate suspicious connections.
- Troubleshoot connectivity issues.
- Detect unusual communication patterns.

## When to Choose CloudTrail

Use CloudTrail when you need to:

- Audit AWS API activity.
- Investigate user actions.
- Meet compliance requirements.
- Track resource changes.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Analyze network traffic | **Amazon VPC Flow Logs** |
| Audit AWS API activity | **AWS CloudTrail** |
| Troubleshoot connectivity | **Amazon VPC Flow Logs** |
| Identify who made a change | **AWS CloudTrail** |
| Detect unusual network behavior | **Amazon VPC Flow Logs** |
| Investigate account activity | **AWS CloudTrail** |
