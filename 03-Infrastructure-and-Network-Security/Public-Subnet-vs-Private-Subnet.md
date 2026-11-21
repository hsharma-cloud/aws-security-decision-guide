# Public Subnet vs Private Subnet

## Purpose

Public and Private Subnets are the foundation of secure Amazon VPC architectures. A Public Subnet hosts resources that require direct internet connectivity, while a Private Subnet hosts internal resources that should not be directly accessible from the internet. Proper subnet design helps reduce the attack surface and supports a defense-in-depth security strategy.

| Feature | Public Subnet | Private Subnet |
|---------|---------------|----------------|
| Primary Purpose | Internet-Facing Resources | Internal Resources |
| Internet Gateway Route | Yes | No |
| Public IP Support | Yes | Optional |
| Direct Internet Access | Yes | No |
| Outbound Internet Access | Yes | Via NAT Gateway |
| Typical Resources | ALB, Bastion Host, NAT Gateway | EC2, RDS, ECS, Lambda |
| Security | Internet Accessible | Isolated from Internet |
| Typical Users | Web Applications | Databases and Backend Services |

## Key Differences

- Public Subnets have a route to an Internet Gateway.
- Private Subnets do not have direct internet access.
- Public resources can communicate directly with the internet.
- Private resources use a NAT Gateway for outbound internet access.
- Most production workloads are deployed in Private Subnets.

## When to Choose a Public Subnet

Use a Public Subnet when you need to:

- Host internet-facing applications.
- Deploy Application Load Balancers.
- Deploy Bastion Hosts.
- Provide public access to services.

## When to Choose a Private Subnet

Use a Private Subnet when you need to:

- Protect application servers.
- Host databases.
- Isolate sensitive workloads.
- Reduce the attack surface.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Host a public web application | **Public Subnet** |
| Host a database | **Private Subnet** |
| Deploy an internet-facing load balancer | **Public Subnet** |
| Protect backend services | **Private Subnet** |
| Reduce internet exposure | **Private Subnet** |
| Provide direct internet access | **Public Subnet** |
