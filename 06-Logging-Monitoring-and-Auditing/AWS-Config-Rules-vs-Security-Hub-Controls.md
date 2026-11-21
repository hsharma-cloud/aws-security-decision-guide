# AWS Config Rules vs AWS Security Hub Controls

## Purpose

AWS Config Rules and AWS Security Hub Controls both help organizations assess compliance and improve security posture, but they operate at different levels. AWS Config Rules evaluate whether AWS resource configurations comply with defined policies, while AWS Security Hub Controls assess AWS resources against security best practices and compliance frameworks such as CIS AWS Foundations Benchmark, PCI DSS, AWS Foundational Security Best Practices (FSBP), and NIST.

| Feature | AWS Config Rules | AWS Security Hub Controls |
|---------|------------------|---------------------------|
| Primary Purpose | Evaluate Resource Configuration | Assess Security Posture |
| Evaluation Scope | Individual Resource Configurations | AWS Security Best Practices |
| Uses AWS Config | Yes | Yes (Many Controls) |
| Compliance Frameworks | Custom or Managed Rules | Built-in Standards |
| Custom Rules | Yes | No |
| Security Findings | Limited | Yes |
| Centralized Dashboard | No | Yes |
| Best For | Configuration Compliance | Security Posture Management |
| Typical Users | Compliance Engineers | Security Operations Teams |

## Key Differences

- AWS Config Rules evaluate **resource configurations**.
- Security Hub Controls evaluate **overall security posture**.
- Config Rules can be **AWS-managed or custom**.
- Security Hub aggregates findings from multiple AWS security services.
- Many Security Hub controls rely on AWS Config to perform compliance evaluations.

## When to Choose AWS Config Rules

Use AWS Config Rules when you need to:

- Validate resource configurations.
- Enforce organization-specific policies.
- Detect configuration drift.
- Build custom compliance checks.
- Continuously evaluate AWS resources.

## When to Choose AWS Security Hub Controls

Use AWS Security Hub Controls when you need to:

- Measure security posture.
- Evaluate compliance with industry standards.
- Aggregate security findings.
- Prioritize remediation efforts.
- View security findings in a centralized dashboard.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Verify that S3 buckets are not publicly accessible | **AWS Config Rules** |
| Assess compliance with CIS AWS Foundations Benchmark | **AWS Security Hub Controls** |
| Create a custom compliance rule | **AWS Config Rules** |
| View findings from GuardDuty, Inspector, and Macie in one place | **AWS Security Hub Controls** |
| Detect resource configuration drift | **AWS Config Rules** |
| Monitor overall AWS security posture | **AWS Security Hub Controls** |
