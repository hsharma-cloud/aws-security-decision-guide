# Detective vs GuardDuty

## Purpose

Amazon GuardDuty and Amazon Detective work together but serve different purposes in the security lifecycle. GuardDuty continuously detects suspicious or malicious activity across AWS environments, while Amazon Detective helps security teams investigate and understand those findings by analyzing relationships, timelines, and resource behavior.

| Feature | Amazon Detective | Amazon GuardDuty |
|---------|------------------|------------------|
| Primary Purpose | Security Investigation | Threat Detection |
| Focus | Analyze incidents | Detect threats |
| Data Sources | CloudTrail, VPC Flow Logs, GuardDuty Findings | CloudTrail, VPC Flow Logs, DNS Logs, EKS Audit Logs |
| Detects Threats | No | Yes |
| Root Cause Analysis | Yes | No |
| Behavioral Analysis | Yes | Limited |
| Automated Findings | No | Yes |
| Typical Users | Incident Responders, Security Analysts | SOC Analysts, Security Operations |

## Key Differences

- GuardDuty identifies **that a threat exists**.
- Detective explains **how and why the threat occurred**.
- GuardDuty generates findings automatically.
- Detective provides visual investigation tools and behavioral analysis.
- GuardDuty is typically the first service used, followed by Detective during investigations.

## When to Choose Detective

Use Detective when you need to:

- Investigate GuardDuty findings.
- Perform root cause analysis.
- Understand attack timelines.
- Analyze relationships between AWS resources.

## When to Choose GuardDuty

Use GuardDuty when you need to:

- Continuously detect threats.
- Monitor suspicious AWS activity.
- Detect compromised credentials.
- Identify malware and reconnaissance activity.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Detect active threats | **Amazon GuardDuty** |
| Investigate security incidents | **Amazon Detective** |
| Perform root cause analysis | **Amazon Detective** |
| Monitor AWS continuously | **Amazon GuardDuty** |
| Detect compromised credentials | **Amazon GuardDuty** |
| Analyze attack timelines | **Amazon Detective** |
