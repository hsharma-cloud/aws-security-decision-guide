# Security Lake vs Security Hub

## Purpose

AWS Security Lake and AWS Security Hub are complementary services that address different aspects of security operations. Security Lake centralizes security logs from AWS, on-premises, and third-party sources into a unified data lake for analytics, while Security Hub centralizes and prioritizes security findings to improve an organization's security posture.

| Feature | AWS Security Lake | AWS Security Hub |
|---------|-------------------|------------------|
| Primary Purpose | Centralized Security Data Lake | Centralized Security Findings |
| Focus | Log collection and analytics | Security posture management |
| Stores Data | Yes | No |
| Aggregates Findings | No | Yes |
| Compliance Dashboard | No | Yes |
| Investigation Support | Yes | Limited |
| Data Format | OCSF (Open Cybersecurity Schema Framework) | AWS Security Findings Format (ASFF) |
| Typical Users | Security Analysts, Threat Hunters | Security Operations, Compliance Teams |

## Key Differences

- Security Lake centralizes **security logs**.
- Security Hub centralizes **security findings**.
- Security Lake supports advanced analytics and threat hunting.
- Security Hub provides dashboards, compliance checks, and finding management.
- Security Hub findings can be enriched using data stored in Security Lake.

## When to Choose Security Lake

Use Security Lake when you need to:

- Centralize security logs.
- Perform threat hunting.
- Retain security telemetry.
- Support forensic investigations.

## When to Choose Security Hub

Use Security Hub when you need to:

- View security findings in one place.
- Monitor compliance.
- Prioritize remediation.
- Manage organizational security posture.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Centralize security logs | **AWS Security Lake** |
| Centralize security findings | **AWS Security Hub** |
| Perform threat hunting | **AWS Security Lake** |
| Monitor compliance posture | **AWS Security Hub** |
| Store long-term security telemetry | **AWS Security Lake** |
| Prioritize security findings | **AWS Security Hub** |
