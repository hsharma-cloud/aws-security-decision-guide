# Security Hub vs Detective

## Purpose

AWS Security Hub and Amazon Detective are complementary security services that support different phases of the security lifecycle. Security Hub centralizes and prioritizes security findings from AWS services and third-party tools, while Amazon Detective helps security teams investigate those findings by analyzing relationships, timelines, and resource activity.

| Feature | AWS Security Hub | Amazon Detective |
|---------|------------------|------------------|
| Primary Purpose | Centralized Security Management | Security Investigation |
| Focus | Aggregate and prioritize findings | Analyze and investigate incidents |
| Data Sources | GuardDuty, Inspector, Macie, Config, Partner Products | CloudTrail, VPC Flow Logs, GuardDuty Findings |
| Compliance Checks | Yes | No |
| Investigation | Limited | Advanced |
| Visualization | Security dashboards | Interactive investigation graphs |
| Automation | Supports EventBridge and workflow automation | Investigation only |
| Typical Users | Security Operations, Compliance Teams | Incident Response, Security Analysts |

## Key Differences

- Security Hub provides a centralized view of security findings across AWS.
- Detective helps determine how and why a security event occurred.
- Security Hub answers **"What security issues exist?"**
- Detective answers **"How did this incident happen?"**
- Both services work together to improve security operations.

## When to Choose Security Hub

Use Security Hub when you need to:

- Aggregate findings from multiple AWS security services.
- Monitor your overall security posture.
- Track compliance with security standards.
- Prioritize and automate security findings.

## When to Choose Detective

Use Detective when you need to:

- Investigate suspicious activity.
- Perform root cause analysis.
- Analyze relationships between AWS resources.
- Understand attacker behavior and timelines.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Centralize security findings | **AWS Security Hub** |
| Investigate security incidents | **Amazon Detective** |
| Monitor compliance posture | **AWS Security Hub** |
| Perform root cause analysis | **Amazon Detective** |
| Automate security workflows | **AWS Security Hub** |
| Analyze attack activity | **Amazon Detective** |
