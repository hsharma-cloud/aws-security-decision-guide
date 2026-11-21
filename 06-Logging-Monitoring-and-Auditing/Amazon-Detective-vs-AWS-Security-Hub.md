# Amazon Detective vs AWS Security Hub

## Purpose

Amazon Detective and AWS Security Hub are complementary AWS security services, but they serve different functions. Amazon Detective helps security teams investigate and analyze security incidents by automatically collecting and correlating data from AWS resources. AWS Security Hub provides a centralized view of security findings from AWS services and third-party tools, helping organizations monitor their overall security posture and prioritize remediation.

| Feature | Amazon Detective | AWS Security Hub |
|---------|------------------|------------------|
| Primary Purpose | Security Investigation | Security Posture Management |
| Focus | Incident Investigation | Centralized Security Findings |
| Aggregates Findings | No | Yes |
| Correlates Security Data | Yes | Limited |
| Root Cause Analysis | Yes | No |
| Compliance Standards | No | Yes |
| Integrates with GuardDuty | Yes | Yes |
| Best For | Threat Investigation | Security Visibility |
| Typical Users | Security Analysts | Security Operations Teams |

## Key Differences

- Amazon Detective helps **investigate security incidents**.
- AWS Security Hub helps **manage and prioritize security findings**.
- Detective automatically correlates security data to accelerate investigations.
- Security Hub aggregates findings from services such as GuardDuty, Inspector, Macie, IAM Access Analyzer, and partner products.
- Security Hub often identifies a finding, while Detective helps explain **why** it occurred.

## When to Choose Amazon Detective

Use Amazon Detective when you need to:

- Investigate suspicious activity.
- Analyze relationships between AWS resources.
- Perform root cause analysis.
- Trace attacker behavior.
- Accelerate incident response.

## When to Choose AWS Security Hub

Use AWS Security Hub when you need to:

- Centralize security findings.
- Assess security posture.
- Monitor compliance standards.
- Prioritize remediation activities.
- Aggregate findings across AWS accounts.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Investigate how an EC2 instance became compromised | **Amazon Detective** |
| View findings from GuardDuty, Inspector, and Macie in one dashboard | **AWS Security Hub** |
| Analyze relationships between users, roles, and resources | **Amazon Detective** |
| Assess compliance with AWS Foundational Security Best Practices | **AWS Security Hub** |
| Perform root cause analysis | **Amazon Detective** |
| Monitor your organization's overall security posture | **AWS Security Hub** |
