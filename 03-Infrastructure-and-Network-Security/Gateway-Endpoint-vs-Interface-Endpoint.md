# Gateway Endpoint vs Interface Endpoint

## Purpose

Gateway Endpoints and Interface Endpoints are two types of Amazon VPC Endpoints that enable private communication with AWS services without traversing the public internet. Gateway Endpoints provide private access to Amazon S3 and Amazon DynamoDB through route tables, while Interface Endpoints use AWS PrivateLink to privately connect to supported AWS services, customer services, and SaaS applications.

| Feature | Gateway Endpoint | Interface Endpoint |
|---------|------------------|--------------------|
| Primary Purpose | Private Access to S3 and DynamoDB | Private Access to Supported AWS and SaaS Services |
| Uses AWS PrivateLink | No | Yes |
| Supported Services | Amazon S3, Amazon DynamoDB | Most AWS Services, Customer Services, SaaS |
| Network Interface | No | Yes (Elastic Network Interface) |
| Route Tables Required | Yes | No |
| Security Groups | No | Yes |
| Hourly Charge | No | Yes |
| Data Processing Charge | No | Yes |
| Typical Users | Cloud Engineers | Cloud Architects, Security Engineers |

## Key Differences

- Gateway Endpoints support **only Amazon S3 and Amazon DynamoDB**.
- Interface Endpoints support **most AWS services and third-party services**.
- Gateway Endpoints use **route tables**.
- Interface Endpoints create **Elastic Network Interfaces (ENIs)** inside the VPC.
- Interface Endpoints are powered by **AWS PrivateLink**.

## When to Choose Gateway Endpoint

Use Gateway Endpoints when you need to:

- Access Amazon S3 privately.
- Access Amazon DynamoDB privately.
- Eliminate NAT Gateway costs for S3 or DynamoDB access.
- Keep traffic within the AWS network.

## When to Choose Interface Endpoint

Use Interface Endpoints when you need to:

- Access supported AWS services privately.
- Connect to private SaaS offerings.
- Publish private services using AWS PrivateLink.
- Secure traffic to AWS APIs without using the public internet.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Access Amazon S3 privately | **Gateway Endpoint** |
| Access Amazon DynamoDB privately | **Gateway Endpoint** |
| Access AWS Secrets Manager privately | **Interface Endpoint** |
| Connect to a SaaS provider | **Interface Endpoint** |
| Avoid NAT Gateway for S3 | **Gateway Endpoint** |
| Access most AWS services privately | **Interface Endpoint** |
