# Security Groups vs Network ACLs

## Purpose

Security Groups and Network ACLs (NACLs) are foundational network security controls within Amazon VPC. Security Groups act as virtual firewalls for individual AWS resources, while Network ACLs protect entire subnets by filtering inbound and outbound traffic. Together, they provide layered network security using a defense-in-depth approach.

| Feature | Security Groups | Network ACLs |
|---------|-----------------|--------------|
| Primary Purpose | Instance-Level Firewall | Subnet-Level Firewall |
| Scope | Elastic Network Interface (ENI) | Entire Subnet |
| Stateful | Yes | No |
| Rule Type | Allow Rules Only | Allow and Deny Rules |
| Rule Evaluation | All rules evaluated | Rules processed in numerical order |
| Default Behavior | Deny inbound, allow outbound | Default NACL allows all traffic |
| Supports Deny Rules | No | Yes |
| Typical Users | Cloud Engineers, Security Engineers | Network Engineers, Security Architects |

## Key Differences

- Security Groups protect **instances and ENIs**.
- Network ACLs protect **subnets**.
- Security Groups are **stateful**, automatically allowing return traffic.
- Network ACLs are **stateless**, requiring explicit inbound and outbound rules.
- Security Groups support **allow rules only**, while Network ACLs support both **allow** and **deny** rules.

## When to Choose Security Groups

Use Security Groups when you need to:

- Protect EC2 instances or other AWS resources.
- Control application-level access.
- Simplify firewall management.
- Allow only trusted traffic to resources.

## When to Choose Network ACLs

Use Network ACLs when you need to:

- Control traffic entering or leaving an entire subnet.
- Block specific IP addresses.
- Add an additional security layer.
- Enforce subnet-wide network policies.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Protect an EC2 instance | **Security Groups** |
| Protect an entire subnet | **Network ACLs** |
| Create deny rules | **Network ACLs** |
| Use a stateful firewall | **Security Groups** |
| Apply defense in depth | **Use Both** |
| Filter traffic before it reaches instances | **Network ACLs** |
