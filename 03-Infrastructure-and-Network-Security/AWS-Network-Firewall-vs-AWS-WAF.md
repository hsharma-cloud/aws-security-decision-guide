# AWS Network Firewall vs AWS WAF

## Purpose

AWS Network Firewall and AWS WAF protect AWS workloads at different layers of the network stack. AWS Network Firewall secures Amazon VPCs by inspecting and filtering network traffic at Layers 3 through 7, while AWS WAF protects web applications and APIs from common web exploits such as SQL injection, cross-site scripting (XSS), bots, and other HTTP/S-based attacks.

| Feature | AWS Network Firewall | AWS WAF |
|---------|----------------------|----------|
| Primary Purpose | Network Protection | Web Application Protection |
| OSI Layer | Layers 3–7 | Layer 7 (HTTP/HTTPS) |
| Protects | VPC Network Traffic | Web Applications and APIs |
| Deployment | VPC Subnets | CloudFront, ALB, API Gateway, AppSync |
| Filters | IP, Port, Protocol, Domain, Stateful Traffic | HTTP/S Requests |
| Threats | Unauthorized network access, malware, lateral movement | SQL Injection, XSS, Bots, OWASP Top 10 |
| Rule Types | Stateful and Stateless | Web ACL Rules |
| Typical Users | Network Engineers, Security Architects | Application Security Engineers, Web Developers |

## Key Differences

- AWS Network Firewall protects the **network**.
- AWS WAF protects **web applications**.
- Network Firewall filters traffic entering and leaving a VPC.
- AWS WAF inspects HTTP and HTTPS requests.
- Both services are commonly deployed together for layered security.

## When to Choose AWS Network Firewall

Use AWS Network Firewall when you need to:

- Inspect VPC network traffic.
- Control inbound and outbound connections.
- Prevent unauthorized network access.
- Enforce network security policies.

## When to Choose AWS WAF

Use AWS WAF when you need to:

- Protect web applications.
- Block SQL injection and XSS attacks.
- Defend APIs from malicious requests.
- Filter HTTP/S traffic.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Protect a VPC network | **AWS Network Firewall** |
| Protect a web application | **AWS WAF** |
| Filter IP, port, and protocol traffic | **AWS Network Firewall** |
| Block SQL injection or XSS | **AWS WAF** |
| Inspect network traffic | **AWS Network Firewall** |
| Protect HTTP/S requests | **AWS WAF** |
