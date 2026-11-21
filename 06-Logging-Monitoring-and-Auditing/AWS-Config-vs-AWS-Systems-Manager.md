# AWS Config vs AWS Systems Manager

## Purpose

AWS Config and AWS Systems Manager are management services that help organizations maintain secure and compliant AWS environments, but they serve different purposes. AWS Config continuously records and evaluates the configuration of AWS resources to detect configuration drift and compliance violations. AWS Systems Manager provides operational management capabilities, allowing administrators to manage, patch, automate, inventory, and securely access AWS resources at scale.

| Feature | AWS Config | AWS Systems Manager |
|---------|------------|---------------------|
| Primary Purpose | Configuration Tracking and Compliance | Operations and Resource Management |
| Tracks Resource Configuration | Yes | Limited |
| Compliance Evaluation | Yes | No |
| Automation | Limited (Remediation) | Extensive |
| Patch Management | No | Yes |
| Inventory Management | No | Yes |
| Remote Administration | No | Yes (Session Manager) |
| Best For | Governance and Compliance | Operations and Administration |
| Typical Users | Security & Compliance Teams | Operations & Cloud Engineers |

## Key Differences

- AWS Config records **resource configurations and configuration changes**.
- AWS Systems Manager **manages and operates AWS resources**.
- AWS Config evaluates compliance against Config Rules.
- Systems Manager automates operational tasks such as patching, inventory collection, and remote access.
- The two services are often used together to detect non-compliance and automatically remediate it.

## When to Choose AWS Config

Use AWS Config when you need to:

- Track configuration changes.
- Evaluate compliance.
- Detect configuration drift.
- Maintain a historical configuration inventory.
- Audit AWS resources.

## When to Choose AWS Systems Manager

Use AWS Systems Manager when you need to:

- Patch EC2 instances.
- Run commands remotely.
- Access instances using Session Manager.
- Collect software inventory.
- Automate operational tasks.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Detect changes to a security group | **AWS Config** |
| Patch hundreds of EC2 instances | **AWS Systems Manager** |
| Evaluate compliance with security policies | **AWS Config** |
| Connect to an EC2 instance without SSH | **AWS Systems Manager** |
| Track historical resource configurations | **AWS Config** |
| Automate routine operational tasks | **AWS Systems Manager** |
