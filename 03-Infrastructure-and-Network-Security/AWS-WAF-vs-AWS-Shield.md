# AWS WAF vs AWS Shield

## Purpose

AWS WAF and AWS Shield both protect internet-facing applications, but they defend against different types of threats. AWS WAF filters and blocks malicious HTTP and HTTPS requests targeting web applications, while AWS Shield protects against Distributed Denial of Service (DDoS) attacks that attempt to overwhelm applications and infrastructure.

| Feature | AWS WAF | AWS Shield |
|---------|---------|------------|
| Primary Purpose | Web Application Protection | DDoS Protection |
| Focus | HTTP/HTTPS Traffic Filtering | Network and Transport Layer Attack Mitigation |
| Protects | Web Applications and APIs | AWS Infrastructure and Internet-Facing Resources |
| Attack Types | SQL Injection, XSS, Bots, OWASP Top 10 | Layer 3, Layer 4, and Layer 7 DDoS Attacks |
| Deployment | CloudFront, ALB, API Gateway, AppSync | Automatic for supported AWS services |
| Custom Rules | Yes | No |
| Protection Type | Rule-Based | Automatic Detection and Mitigation |
| Typical Users | Application Security Engineers | Network and Security Engineers |

## Key Differences

- AWS WAF protects against **application-layer attacks**.
- AWS Shield protects against **DDoS attacks**.
- WAF allows custom rules to filter web requests.
- Shield automatically detects and mitigates DDoS attacks.
- AWS Shield Advanced provides enhanced protection, visibility, and response capabilities.

## When to Choose AWS WAF

Use AWS WAF when you need to:

- Block SQL injection and XSS attacks.
- Protect APIs and web applications.
- Filter malicious HTTP/S requests.
- Enforce custom web security rules.

## When to Choose AWS Shield

Use AWS Shield when you need to:

- Protect against DDoS attacks.
- Defend internet-facing applications.
- Minimize service disruption during attacks.
- Automatically mitigate volumetric attacks.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Protect a web application | **AWS WAF** |
| Defend against DDoS attacks | **AWS Shield** |
| Filter HTTP/S requests | **AWS WAF** |
| Automatically mitigate network attacks | **AWS Shield** |
| Block SQL injection or XSS | **AWS WAF** |
| Protect internet-facing AWS resources | **AWS Shield** |
