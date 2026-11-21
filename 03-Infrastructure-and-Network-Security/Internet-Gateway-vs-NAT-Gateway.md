# Internet Gateway vs NAT Gateway

## Purpose

An Internet Gateway (IGW) and a NAT Gateway both enable internet connectivity for resources within an Amazon VPC, but they serve different purposes. An Internet Gateway allows resources in a public subnet to communicate directly with the internet, while a NAT Gateway enables resources in private subnets to initiate outbound internet connections without allowing inbound connections.

| Feature | Internet Gateway | NAT Gateway |
|---------|------------------|-------------|
| Primary Purpose | Public Internet Access | Outbound Internet Access for Private Subnets |
| Attached To | VPC | Public Subnet |
| Supports Inbound Traffic | Yes | No |
| Supports Outbound Traffic | Yes | Yes |
| Public IP Required | Yes (for EC2) | Yes (Elastic IP) |
| Used By | Public Subnets | Private Subnets |
| Managed Service | Yes | Yes |
| Typical Users | Cloud Engineers | Cloud Architects, Security Engineers |

## Key Differences

- Internet Gateway provides **direct internet connectivity**.
- NAT Gateway provides **outbound-only internet access**.
- Internet Gateway supports inbound and outbound communication.
- NAT Gateway blocks unsolicited inbound traffic.
- NAT Gateway must reside in a public subnet and uses an Internet Gateway to reach the internet.

## When to Choose Internet Gateway

Use an Internet Gateway when you need to:

- Host public web servers.
- Allow users to access EC2 instances from the internet.
- Provide direct internet connectivity.
- Support internet-facing applications.

## When to Choose NAT Gateway

Use a NAT Gateway when you need to:

- Allow private instances to download updates.
- Keep workloads isolated from inbound internet traffic.
- Provide secure outbound internet access.
- Support private application architectures.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Host a public website | **Internet Gateway** |
| Give private instances internet access | **NAT Gateway** |
| Allow inbound internet traffic | **Internet Gateway** |
| Block inbound internet traffic | **NAT Gateway** |
| Place resources in a public subnet | **Internet Gateway** |
| Keep workloads in a private subnet | **NAT Gateway** |
