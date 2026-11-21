# Detective vs Security Hub

## Purpose

Amazon Detective and AWS Security Hub are complementary services that support different phases of security operations. Amazon Detective helps security teams investigate incidents by analyzing AWS activity and resource relationships, while AWS Security Hub provides a centralized view of security findings and compliance across AWS accounts and services.

| Feature | Amazon Detective | AWS Security Hub |
|---------|------------------|------------------|
| Primary Purpose | Security Investigation | Security Posture Management |
| Focus | Incident Analysis | Security Findings Management |
| Generates Findings | No | Aggregates Findings |
| Root Cause Analysis | Yes | No |
| Compliance Dashboard | No | Yes |
| Investigation Graphs | Yes | No |
| Integrates With | GuardDuty, CloudTrail, VPC Flow Logs | GuardDuty, Inspector, Macie, Config, IAM Access Analyzer |
| Typical Users | Incident Responders, Security Analysts | SOC Teams, Compliance Teams |

## Key Differences

- Detective investigates **why** a security event occurred.
- Security Hub shows **what** security findings exist.
- Detective focuses on investigation and forensic analysis.
- Security Hub focuses on centralized visibility and compliance.
- Security Hub findings are often investigated using Detective.

## When to Choose Detective

Use Detective when you need to:

- Investigate security incidents.
- Perform root cause analysis.
- Analyze relationships between AWS resources.
- Understand attacker behavior.

## When to Choose Security Hub

Use Security Hub when you need to:

- Aggregate findings from multiple AWS services.
- Monitor security posture.
- Prioritize remediation.
- Track compliance.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Investigate an incident | **Amazon Detective** |
| Centralize security findings | **AWS Security Hub** |
| Perform root cause analysis | **Amazon Detective** |
| Monitor compliance | **AWS Security Hub** |
| Analyze attack behavior | **Amazon Detective** |
| View findings from multiple security tools | **AWS Security Hub** |
