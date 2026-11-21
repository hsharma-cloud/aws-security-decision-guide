# AWS Transit Gateway vs AWS Cloud WAN

## Purpose

AWS Transit Gateway and AWS Cloud WAN both simplify network connectivity, but they are designed for different scopes. AWS Transit Gateway serves as a regional hub that connects VPCs, VPNs, and Direct Connect gateways, while AWS Cloud WAN provides centralized management of global enterprise networks spanning multiple AWS Regions, on-premises environments, and branch offices.

| Feature | AWS Transit Gateway | AWS Cloud WAN |
|---------|---------------------|---------------|
| Primary Purpose | Regional Network Hub | Global Network Management |
| Scope | Single AWS Region | Multi-Region Global Network |
| Architecture | Hub-and-Spoke | Global WAN |
| Connects | VPCs, VPNs, Direct Connect | Transit Gateways, Branches, Data Centers |
| Multi-Region Support | Via Peering | Native |
| Centralized Policy | Limited | Yes |
| Best For | Regional Connectivity | Enterprise Global Networks |
| Typical Users | Cloud Architects | Enterprise Network Architects |

## Key Differences

- Transit Gateway centralizes **regional AWS connectivity**.
- Cloud WAN centralizes **global enterprise networking**.
- Transit Gateway connects VPCs within and across Regions.
- Cloud WAN manages multiple Transit Gateways and branch locations through a single network policy.
- Cloud WAN is designed for organizations with global networking requirements.

## When to Choose AWS Transit Gateway

Use AWS Transit Gateway when you need to:

- Connect multiple VPCs within a Region.
- Integrate VPN and Direct Connect.
- Simplify regional routing.
- Build a hub-and-spoke network.

## When to Choose AWS Cloud WAN

Use AWS Cloud WAN when you need to:

- Manage a global network.
- Connect multiple AWS Regions.
- Integrate branch offices and data centers.
- Apply centralized networking policies.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Connect VPCs in one Region | **AWS Transit Gateway** |
| Manage a global enterprise network | **AWS Cloud WAN** |
| Simplify regional routing | **AWS Transit Gateway** |
| Apply centralized global policies | **AWS Cloud WAN** |
| Connect VPNs and Direct Connect | **AWS Transit Gateway** |
| Connect Regions, branches, and AWS together | **AWS Cloud WAN** |
