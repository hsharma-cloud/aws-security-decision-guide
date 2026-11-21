# CloudTrail Insights vs Amazon GuardDuty

## Purpose

CloudTrail Insights and Amazon GuardDuty both help detect unusual activity in AWS environments, but they focus on different types of anomalies. CloudTrail Insights identifies unusual spikes or changes in AWS API activity by comparing current behavior to historical baselines. Amazon GuardDuty is a threat detection service that continuously analyzes AWS logs, network activity, DNS queries, and threat intelligence to identify malicious or unauthorized behavior.

| Feature | CloudTrail Insights | Amazon GuardDuty |
|---------|---------------------|------------------|
| Primary Purpose | Detect Unusual API Activity | Detect Security Threats |
| Data Source | CloudTrail Management Events | CloudTrail, VPC Flow Logs, DNS Logs, EKS Audit Logs, Runtime Signals |
| Detects API Anomalies | Yes | Limited |
| Detects Malware & Threats | No | Yes |
| Uses Threat Intelligence | No | Yes |
| Machine Learning | Yes | Yes |
| Best For | Auditing Administrative Activity | Continuous Threat Detection |
| Typical Users | Security & Compliance Teams | Security Operations Center (SOC) |

## Key Differences

- CloudTrail Insights detects **abnormal AWS API usage patterns**.
- GuardDuty detects **malicious activity and security threats**.
- CloudTrail Insights compares activity against historical API baselines.
- GuardDuty combines machine learning with AWS and third-party threat intelligence.
- Organizations commonly enable both services for comprehensive security monitoring.

## When to Choose CloudTrail Insights

Use CloudTrail Insights when you need to:

- Detect unusual API activity.
- Identify abnormal administrative behavior.
- Investigate unexpected management operations.
- Monitor API usage trends.
- Enhance CloudTrail auditing.

## When to Choose Amazon GuardDuty

Use Amazon GuardDuty when you need to:

- Detect compromised credentials.
- Identify cryptocurrency mining activity.
- Detect malware or suspicious network behavior.
- Monitor for unauthorized access.
- Continuously identify security threats.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Detect an unusual spike in `DeleteBucket` API calls | **CloudTrail Insights** |
| Detect communication with a known malicious IP address | **Amazon GuardDuty** |
| Identify abnormal IAM API activity | **CloudTrail Insights** |
| Detect compromised EC2 instances | **Amazon GuardDuty** |
| Investigate unexpected management activity | **CloudTrail Insights** |
| Continuously monitor for security threats | **Amazon GuardDuty** |
