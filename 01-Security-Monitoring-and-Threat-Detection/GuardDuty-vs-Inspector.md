# GuardDuty vs Inspector

## Purpose

Amazon GuardDuty and Amazon Inspector are complementary AWS security services that address different aspects of cloud security. GuardDuty continuously detects threats by analyzing AWS activity and behavior, while Amazon Inspector continuously assesses workloads for software vulnerabilities and unintended network exposure.

| Feature | Amazon GuardDuty | Amazon Inspector |
|---------|------------------|------------------|
| Primary Purpose | Threat Detection | Vulnerability Management |
| Focus | Active threats and suspicious activity | Software vulnerabilities and exposure |
| Monitors | AWS accounts, identities, workloads, network activity | EC2 instances, ECR container images, Lambda functions |
| Data Sources | CloudTrail, VPC Flow Logs, DNS Logs, EKS Audit Logs | Software inventory, CVE database, package analysis |
| Detects | Compromised credentials, malware, reconnaissance, suspicious behavior | Missing patches, CVEs, vulnerable packages, unintended network exposure |
| Continuous Monitoring | Yes | Yes |
| Automatic Findings | Yes | Yes |
| Typical Users | Security Operations (SOC), Incident Response Teams | Security Engineers, Vulnerability Management Teams |

## Key Differences

- GuardDuty detects **active threats** occurring in your AWS environment.
- Inspector identifies **security weaknesses** before they can be exploited.
- GuardDuty analyzes AWS logs and network activity.
- Inspector scans workloads for known vulnerabilities (CVEs).
- Both services integrate with AWS Security Hub for centralized visibility.

## When to Choose GuardDuty

Use GuardDuty when you need to:

- Detect compromised AWS credentials.
- Identify suspicious or malicious activity.
- Monitor AWS accounts continuously for threats.
- Detect reconnaissance, malware, or unauthorized access.

## When to Choose Inspector

Use Inspector when you need to:

- Identify vulnerable software packages.
- Detect missing security patches.
- Scan EC2 instances, ECR images, and Lambda functions.
- Prioritize remediation based on vulnerability severity.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Detect active threats | **Amazon GuardDuty** |
| Find software vulnerabilities | **Amazon Inspector** |
| Detect compromised credentials | **Amazon GuardDuty** |
| Scan workloads for CVEs | **Amazon Inspector** |
| Monitor suspicious AWS activity | **Amazon GuardDuty** |
| Identify missing patches | **Amazon Inspector** |
