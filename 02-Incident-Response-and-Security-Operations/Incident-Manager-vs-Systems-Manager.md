# Incident Manager vs Systems Manager

## Purpose

AWS Incident Manager and AWS Systems Manager support different aspects of security operations. Incident Manager helps organizations prepare for, respond to, and coordinate security incidents, while AWS Systems Manager provides operational capabilities for managing, automating, patching, and maintaining AWS resources throughout their lifecycle.

| Feature | AWS Incident Manager | AWS Systems Manager |
|---------|----------------------|---------------------|
| Primary Purpose | Incident Coordination | Infrastructure Management |
| Focus | Incident Response | Operations Management |
| Incident Timeline | Yes | No |
| Response Plans | Yes | No |
| Escalation Management | Yes | No |
| Runbooks | References Automation Runbooks | Executes Automation Runbooks |
| Operational Management | Limited | Comprehensive |
| Typical Users | SOC Teams, Incident Responders | Cloud Administrators, Operations Teams |

## Key Differences

- Incident Manager coordinates **people and processes** during an incident.
- Systems Manager automates **operational and remediation tasks**.
- Incident Manager manages response plans, contacts, and timelines.
- Systems Manager manages AWS resources through automation, patching, inventory, and compliance.
- Incident Manager often invokes Systems Manager Automation during incident response.

## When to Choose Incident Manager

Use Incident Manager when you need to:

- Coordinate security incidents.
- Notify and escalate responders.
- Execute incident response plans.
- Track incident timelines and communications.

## When to Choose Systems Manager

Use Systems Manager when you need to:

- Automate operational tasks.
- Patch managed instances.
- Execute remediation runbooks.
- Maintain AWS infrastructure.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Coordinate incident response | **AWS Incident Manager** |
| Automate infrastructure operations | **AWS Systems Manager** |
| Escalate responders | **AWS Incident Manager** |
| Execute remediation runbooks | **AWS Systems Manager** |
| Track incident timelines | **AWS Incident Manager** |
| Manage AWS resources | **AWS Systems Manager** |
