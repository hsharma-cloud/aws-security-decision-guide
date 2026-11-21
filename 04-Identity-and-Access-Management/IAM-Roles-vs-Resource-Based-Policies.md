# IAM Roles vs Resource-Based Policies

## Purpose

IAM Roles and Resource-Based Policies both grant access to AWS resources, but they do so in different ways. IAM Roles provide temporary permissions to trusted identities, while Resource-Based Policies are attached directly to AWS resources and specify which principals are allowed to access them. Understanding when to use each is essential for designing secure and scalable AWS environments.

| Feature | IAM Roles | Resource-Based Policies |
|---------|-----------|-------------------------|
| Primary Purpose | Grant Temporary Permissions | Grant Access to a Resource |
| Attached To | Identity | AWS Resource |
| Uses STS | Yes | No |
| Temporary Credentials | Yes | No |
| Supports Cross-Account Access | Yes | Yes |
| Common Resources | EC2, Lambda, ECS | S3, SQS, SNS, KMS |
| Policy Location | IAM | Resource |
| Typical Users | Security Engineers | Resource Owners |

## Key Differences

- IAM Roles grant permissions **to identities**.
- Resource-Based Policies grant permissions **to resources**.
- IAM Roles issue temporary credentials through AWS STS.
- Resource-Based Policies specify which principals can access a resource.
- Cross-account access can be implemented using either approach, depending on the service.

## When to Choose IAM Roles

Use IAM Roles when you need to:

- Grant permissions to AWS services.
- Provide temporary credentials.
- Enable cross-account access.
- Eliminate long-term access keys.

## When to Choose Resource-Based Policies

Use Resource-Based Policies when you need to:

- Share AWS resources.
- Allow another AWS account to access a resource.
- Control access directly from the resource.
- Grant service-specific permissions.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Grant permissions to EC2 or Lambda | **IAM Role** |
| Share an S3 bucket | **Resource-Based Policy** |
| Provide temporary credentials | **IAM Role** |
| Control who can access a resource | **Resource-Based Policy** |
| Enable service-to-service access | **IAM Role** |
| Allow another account to access an S3 bucket | **Resource-Based Policy** |
