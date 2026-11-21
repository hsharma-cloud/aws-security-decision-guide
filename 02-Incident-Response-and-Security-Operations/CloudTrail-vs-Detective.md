# CloudTrail vs Detective

## Purpose

AWS CloudTrail and Amazon Detective are complementary services that support different stages of incident response. CloudTrail records AWS API activity for auditing and accountability, while Amazon Detective analyzes security data to help investigators understand the root cause and scope of security incidents.

| Feature | AWS CloudTrail | Amazon Detective |
|---------|----------------|------------------|
| Primary Purpose | API Auditing | Security Investigation |
| Focus | Record AWS activity | Analyze security incidents |
| Records API Calls | Yes | Uses CloudTrail data |
| Root Cause Analysis | No | Yes |
| Timeline Analysis | Limited | Yes |
| Behavioral Analysis | No | Yes |
| Primary Use | Auditing and compliance | Incident investigation |
| Typical Users | Auditors, Security Teams | Incident Responders, Security Analysts |

## Key Differences

- CloudTrail records **what actions occurred** in AWS.
- Detective analyzes **how and why an incident occurred**.
- CloudTrail provides the audit trail.
- Detective builds investigations using CloudTrail, GuardDuty, and VPC Flow Logs.
- CloudTrail data is commonly used as an input to Detective.

## When to Choose CloudTrail

Use CloudTrail when you need to:

- Audit AWS API activity.
- Track user and service actions.
- Meet compliance requirements.
- Support forensic investigations.

## When to Choose Detective

Use Detective when you need to:

- Investigate security findings.
- Perform root cause analysis.
- Analyze attack timelines.
- Understand relationships between AWS resources.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Audit AWS API activity | **AWS CloudTrail** |
| Investigate incidents | **Amazon Detective** |
| Track user actions | **AWS CloudTrail** |
| Perform root cause analysis | **Amazon Detective** |
| Meet compliance requirements | **AWS CloudTrail** |
| Analyze attack behavior | **Amazon Detective** |
