# AWS Config vs Security Hub

## Purpose

AWS Config and AWS Security Hub help organizations improve security posture, but they serve different purposes. AWS Config continuously records resource configurations and evaluates them against compliance rules, while AWS Security Hub aggregates security findings from AWS services and partner products to provide a centralized view of an organization's security posture.

| Feature | AWS Config | AWS Security Hub |
|---------|------------|------------------|
| Primary Purpose | Configuration Management | Security Posture Management |
| Focus | Resource configuration and compliance | Centralized security findings |
| Records Configuration Changes | Yes | No |
| Compliance Evaluation | Yes | Yes (Aggregated) |
| Aggregates Findings | No | Yes |
| Supports Security Standards | Through Config Rules | Yes (CIS, PCI DSS, AWS Foundational Security Best Practices) |
| Typical Users | Governance, Compliance Teams | Security Operations, Compliance Teams |

## Key Differences

- AWS Config monitors **resource configurations**.
- Security Hub monitors **security findings**.
- Config evaluates compliance using Config Rules.
- Security Hub aggregates findings from GuardDuty, Inspector, Macie, Config, and partner products.
- Both services complement each other to strengthen governance and security visibility.

## When to Choose AWS Config

Use AWS Config when you need to:

- Track resource configuration changes.
- Detect configuration drift.
- Evaluate compliance continuously.
- Audit AWS resource configurations.

## When to Choose Security Hub

Use Security Hub when you need to:

- View security findings in one place.
- Prioritize security issues.
- Monitor security posture.
- Track compliance across multiple AWS services.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Track configuration changes | **AWS Config** |
| Centralize security findings | **AWS Security Hub** |
| Evaluate compliance rules | **AWS Config** |
| Monitor overall security posture | **AWS Security Hub** |
| Detect configuration drift | **AWS Config** |
| Aggregate findings from multiple security services | **AWS Security Hub** |
