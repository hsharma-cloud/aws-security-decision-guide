# Security Hub vs Incident Manager

## Purpose

AWS Security Hub and AWS Incident Manager support different phases of security operations. Security Hub continuously aggregates, prioritizes, and manages security findings across AWS services, while Incident Manager helps security teams coordinate, communicate, and manage the response to security incidents.

| Feature | AWS Security Hub | AWS Incident Manager |
|---------|------------------|----------------------|
| Primary Purpose | Security Posture Management | Incident Coordination |
| Focus | Security findings | Incident response |
| Aggregates Findings | Yes | No |
| Compliance Dashboard | Yes | No |
| Response Plans | No | Yes |
| Escalation Management | No | Yes |
| Incident Timeline | No | Yes |
| Typical Users | Security Operations, Compliance Teams | Incident Responders, SOC Teams |

## Key Differences

- Security Hub identifies and prioritizes **security issues**.
- Incident Manager coordinates **people and processes** during an incident.
- Security Hub provides centralized visibility into security findings.
- Incident Manager manages response plans, communications, and timelines.
- Security Hub findings can trigger Incident Manager response plans.

## When to Choose Security Hub

Use Security Hub when you need to:

- Aggregate security findings.
- Monitor organizational security posture.
- Track compliance.
- Prioritize remediation efforts.

## When to Choose Incident Manager

Use Incident Manager when you need to:

- Coordinate incident response.
- Notify responders.
- Manage incident timelines.
- Execute response plans.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Centralize security findings | **AWS Security Hub** |
| Coordinate incident response | **AWS Incident Manager** |
| Monitor compliance | **AWS Security Hub** |
| Escalate responders | **AWS Incident Manager** |
| Prioritize security issues | **AWS Security Hub** |
| Manage incident communications | **AWS Incident Manager** |
