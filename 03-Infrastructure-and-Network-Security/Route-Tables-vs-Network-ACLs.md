# Route Tables vs Network ACLs

## Purpose

Route Tables and Network ACLs (NACLs) are essential components of Amazon VPC networking, but they serve different purposes. Route Tables determine where network traffic is directed, while Network ACLs control whether traffic is allowed or denied as it enters or leaves a subnet. Together, they enable secure and efficient network communication.

| Feature | Route Tables | Network ACLs |
|---------|--------------|--------------|
| Primary Purpose | Traffic Routing | Traffic Filtering |
| Scope | Subnet | Subnet |
| Controls | Packet Destination | Packet Permission |
| Stateful | N/A | No |
| Supports Deny Rules | No | Yes |
| Rule Processing | Longest Prefix Match | Numerical Rule Order |
| Default Behavior | Local Route Included | Default NACL Allows All Traffic |
| Typical Users | Network Engineers | Security Engineers |

## Key Differences

- Route Tables determine **where traffic goes**.
- Network ACLs determine **whether traffic is allowed**.
- Route Tables forward packets to destinations.
- Network ACLs filter inbound and outbound traffic.
- Both work together to enable secure communication within a VPC.

## When to Choose Route Tables

Use Route Tables when you need to:

- Route traffic between networks.
- Configure Internet Gateway access.
- Configure NAT Gateway routing.
- Connect VPCs using Transit Gateway or VPC Peering.

## When to Choose Network ACLs

Use Network ACLs when you need to:

- Filter subnet traffic.
- Block specific IP addresses.
- Apply subnet-wide security policies.
- Add a layer of network protection.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Route packets | **Route Tables** |
| Filter traffic | **Network ACLs** |
| Configure Internet Gateway routing | **Route Tables** |
| Deny unwanted traffic | **Network ACLs** |
| Connect networks | **Route Tables** |
| Protect an entire subnet | **Network ACLs** |
