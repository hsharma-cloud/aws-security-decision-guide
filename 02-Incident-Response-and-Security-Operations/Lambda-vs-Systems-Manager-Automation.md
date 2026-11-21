# Lambda vs Systems Manager Automation

## Purpose

AWS Lambda and AWS Systems Manager Automation both automate operational and security tasks, but they are designed for different purposes. Lambda executes custom serverless code in response to events, while Systems Manager Automation executes predefined runbooks to automate operational, administrative, and remediation tasks across AWS resources.

| Feature | AWS Lambda | Systems Manager Automation |
|---------|------------|----------------------------|
| Primary Purpose | Execute Custom Code | Execute Automation Runbooks |
| Focus | Event-driven processing | Operational and security automation |
| Requires Coding | Yes | Usually No |
| Uses Runbooks | No | Yes |
| State Management | No | Yes |
| Built-in AWS Actions | Limited | Extensive |
| Best For | Custom business logic | Infrastructure remediation |
| Typical Users | Developers, Security Engineers | Cloud Administrators, Security Operations |

## Key Differences

- Lambda runs **custom code**.
- Systems Manager Automation runs **predefined runbooks**.
- Lambda is ideal for lightweight event-driven automation.
- Systems Manager Automation is ideal for operational and security remediation.
- Lambda can be invoked from Systems Manager Automation when custom logic is required.

## When to Choose Lambda

Use Lambda when you need to:

- Execute custom code.
- Respond to AWS events.
- Process security findings.
- Build serverless integrations.

## When to Choose Systems Manager Automation

Use Systems Manager Automation when you need to:

- Execute operational runbooks.
- Remediate security findings automatically.
- Patch or configure AWS resources.
- Standardize operational procedures.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Execute custom code | **AWS Lambda** |
| Run operational playbooks | **Systems Manager Automation** |
| Respond to events | **AWS Lambda** |
| Automate remediation | **Systems Manager Automation** |
| Build serverless integrations | **AWS Lambda** |
| Standardize operations | **Systems Manager Automation** |
