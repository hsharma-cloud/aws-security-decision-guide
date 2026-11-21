# Bastion Host vs Session Manager

## Purpose

Bastion Hosts and AWS Systems Manager Session Manager both provide administrative access to Amazon EC2 instances, but they use different approaches. A Bastion Host is a hardened EC2 instance that serves as a secure entry point into a private network, while Session Manager provides browser-based or CLI-based access to managed instances without requiring SSH keys, inbound ports, or bastion hosts.

| Feature | Bastion Host | Session Manager |
|---------|--------------|-----------------|
| Primary Purpose | Secure Administrative Access | Secure Administrative Access |
| Access Method | SSH / RDP | AWS Console, CLI, SDK |
| Inbound Ports Required | Yes | No |
| SSH Keys Required | Yes | No |
| Bastion Server Required | Yes | No |
| Session Logging | Manual Configuration | Built-in (CloudWatch/S3) |
| Multi-Factor Authentication | External | IAM + MFA |
| Management Overhead | High | Low |
| Typical Users | Traditional Infrastructure Teams | Cloud and Security Engineers |

## Key Differences

- Bastion Hosts require inbound SSH or RDP access.
- Session Manager eliminates the need for inbound ports.
- Bastion Hosts require server maintenance.
- Session Manager is a fully managed AWS capability.
- Session Manager provides built-in auditing and session logging.

## When to Choose Bastion Host

Use a Bastion Host when you need to:

- Support legacy environments.
- Access systems without the SSM Agent.
- Meet specific operational requirements.
- Provide controlled SSH or RDP access.

## When to Choose Session Manager

Use Session Manager when you need to:

- Eliminate SSH and RDP exposure.
- Reduce administrative overhead.
- Record administrative sessions.
- Improve security using IAM-based access controls.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Access legacy servers | **Bastion Host** |
| Eliminate inbound SSH/RDP | **Session Manager** |
| Reduce operational overhead | **Session Manager** |
| Record administrative sessions | **Session Manager** |
| Support traditional jump-server architectures | **Bastion Host** |
| Use IAM-based access | **Session Manager** |
