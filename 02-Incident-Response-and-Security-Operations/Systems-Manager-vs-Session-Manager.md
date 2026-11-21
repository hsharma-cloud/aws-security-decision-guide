# Systems Manager vs Session Manager

## Purpose

AWS Systems Manager and AWS Systems Manager Session Manager are closely related services that simplify the management of AWS resources. Systems Manager is a comprehensive operations management service that provides capabilities such as automation, patching, inventory, parameter management, and compliance, while Session Manager is a feature of Systems Manager that provides secure, browser-based and CLI-based access to managed instances without requiring SSH, RDP, or bastion hosts.

| Feature | AWS Systems Manager | Session Manager |
|---------|---------------------|-----------------|
| Primary Purpose | Manage AWS Resources | Secure Remote Access |
| Focus | Operations Management | Instance Access |
| SSH/RDP Required | N/A | No |
| Bastion Host Required | N/A | No |
| Supports Automation | Yes | No |
| Patch Management | Yes | No |
| Inventory Management | Yes | No |
| Session Logging | Limited | Yes |
| Typical Users | Cloud Administrators, Security Engineers | Administrators, Incident Responders |

## Key Differences

- Systems Manager is a complete operations management platform.
- Session Manager is one capability within Systems Manager.
- Systems Manager automates operational tasks.
- Session Manager provides secure remote access to managed instances.
- Session Manager eliminates the need for inbound SSH or RDP ports.

## When to Choose Systems Manager

Use Systems Manager when you need to:

- Automate operational tasks.
- Patch and maintain infrastructure.
- Collect inventory and compliance data.
- Manage parameters and secrets.

## When to Choose Session Manager

Use Session Manager when you need to:

- Securely access EC2 instances.
- Eliminate bastion hosts.
- Remove inbound SSH and RDP access.
- Record administrator sessions for auditing.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Automate infrastructure management | **AWS Systems Manager** |
| Securely connect to EC2 instances | **Session Manager** |
| Patch managed instances | **AWS Systems Manager** |
| Eliminate SSH or RDP access | **Session Manager** |
| Manage operational tasks | **AWS Systems Manager** |
| Record administrative sessions | **Session Manager** |
