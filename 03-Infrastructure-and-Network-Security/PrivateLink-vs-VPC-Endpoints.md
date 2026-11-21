# AWS PrivateLink vs VPC Endpoints

## Purpose

AWS PrivateLink and VPC Endpoints enable private connectivity to AWS services and applications without traversing the public internet. AWS PrivateLink securely exposes services across VPCs and AWS accounts using interface endpoints, while VPC Endpoints provide private access from a VPC to supported AWS services. Understanding their relationship is essential for designing secure and scalable AWS network architectures.

| Feature | AWS PrivateLink | VPC Endpoints |
|---------|-----------------|---------------|
| Primary Purpose | Private Service Connectivity | Private Access to AWS Services |
| Scope | AWS Services, Customer Services, SaaS | AWS Services |
| Uses Public Internet | No | No |
| Endpoint Type | Interface Endpoint | Gateway or Interface Endpoint |
| Cross-Account Support | Yes | Limited |
| Supports Customer Services | Yes | Interface Endpoints Only |
| Typical Use Case | Share private services | Access AWS services privately |
| Typical Users | SaaS Providers, Enterprise Architects | Cloud Engineers, Security Engineers |

## Key Differences

- AWS PrivateLink is the **technology** for privately exposing services.
- Interface VPC Endpoints are the **implementation** of AWS PrivateLink.
- VPC Endpoints include both **Gateway Endpoints** and **Interface Endpoints**.
- PrivateLink supports secure communication across AWS accounts and VPCs.
- Both eliminate the need for Internet Gateways, NAT Gateways, or VPNs for supported services.

## When to Choose AWS PrivateLink

Use AWS PrivateLink when you need to:

- Share private applications across AWS accounts.
- Connect securely to SaaS providers.
- Publish services privately.
- Enable cross-VPC private communication.

## When to Choose VPC Endpoints

Use VPC Endpoints when you need to:

- Access AWS services privately.
- Keep traffic within the AWS network.
- Improve security by avoiding the public internet.
- Simplify private connectivity to supported AWS services.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Publish a private service | **AWS PrivateLink** |
| Access AWS services privately | **VPC Endpoints** |
| Connect to a SaaS provider | **AWS PrivateLink** |
| Eliminate internet access to AWS services | **VPC Endpoints** |
| Share services across AWS accounts | **AWS PrivateLink** |
| Access S3 or DynamoDB privately | **VPC Endpoints** |
