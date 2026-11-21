# Gateway Load Balancer vs Network Load Balancer

## Purpose

Gateway Load Balancer (GWLB) and Network Load Balancer (NLB) both operate at the network layer but serve different purposes. Gateway Load Balancer transparently deploys, scales, and manages third-party virtual network appliances such as firewalls, intrusion detection systems (IDS), and intrusion prevention systems (IPS). Network Load Balancer distributes TCP, UDP, and TLS traffic across application targets while delivering high performance and low latency.

| Feature | Gateway Load Balancer | Network Load Balancer |
|---------|-----------------------|-----------------------|
| Primary Purpose | Deploy Security Appliances | Load Balance Network Traffic |
| Focus | Traffic Inspection | Traffic Distribution |
| OSI Layer | Layer 3/4 | Layer 4 |
| Typical Targets | Firewalls, IDS, IPS | EC2, Containers, IP Addresses |
| Uses GENEVE | Yes | No |
| Preserves Client IP | Yes | Yes |
| High Performance | Yes | Yes |
| Typical Users | Security Architects | Application and Network Engineers |

## Key Differences

- Gateway Load Balancer is designed for **security inspection**.
- Network Load Balancer is designed for **traffic distribution**.
- Gateway Load Balancer integrates with third-party security appliances.
- Network Load Balancer forwards traffic directly to application targets.
- Gateway Load Balancer enables centralized network security architectures.

## When to Choose Gateway Load Balancer

Use Gateway Load Balancer when you need to:

- Deploy virtual firewalls.
- Inspect network traffic.
- Scale security appliances.
- Centralize traffic inspection.

## When to Choose Network Load Balancer

Use Network Load Balancer when you need to:

- Distribute TCP or UDP traffic.
- Support high-performance applications.
- Preserve client IP addresses.
- Balance traffic across multiple targets.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Deploy virtual firewalls | **Gateway Load Balancer** |
| Load balance TCP/UDP traffic | **Network Load Balancer** |
| Inspect network traffic | **Gateway Load Balancer** |
| Support low-latency applications | **Network Load Balancer** |
| Scale security appliances | **Gateway Load Balancer** |
| Route traffic to application servers | **Network Load Balancer** |
