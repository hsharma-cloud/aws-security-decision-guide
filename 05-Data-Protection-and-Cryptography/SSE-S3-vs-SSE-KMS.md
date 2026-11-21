# SSE-S3 vs SSE-KMS

## Purpose

Server-Side Encryption with Amazon S3 Managed Keys (SSE-S3) and Server-Side Encryption with AWS Key Management Service (SSE-KMS) both encrypt data at rest in Amazon S3. The primary difference is who manages the encryption keys and the level of control, auditing, and access management available. SSE-S3 is fully managed by Amazon S3, while SSE-KMS uses AWS KMS to provide centralized key management, detailed audit logging, and fine-grained access control.

| Feature | SSE-S3 | SSE-KMS |
|---------|---------|----------|
| Primary Purpose | Simple Server-Side Encryption | Managed Encryption with KMS |
| Key Management | Amazon S3 | AWS KMS |
| Customer Control | No | Yes |
| CloudTrail Logging | No | Yes |
| Key Policies | No | Yes |
| Automatic Key Rotation | AWS Managed | Configurable (Customer Managed Keys) |
| Additional Cost | No | Yes (KMS Requests) |
| Best For | General Data Protection | Compliance and Fine-Grained Access Control |
| Typical Users | General AWS Customers | Security and Compliance Teams |

## Key Differences

- SSE-S3 uses encryption keys managed entirely by Amazon S3.
- SSE-KMS uses AWS KMS customer-managed or AWS-managed keys.
- SSE-KMS provides CloudTrail audit logs for key usage.
- SSE-KMS supports IAM policies and KMS key policies.
- SSE-KMS is recommended when compliance, auditing, or key management is required.

## When to Choose SSE-S3

Use SSE-S3 when you need to:

- Encrypt S3 objects with minimal configuration.
- Reduce operational complexity.
- Avoid additional KMS costs.
- Meet standard encryption requirements.

## When to Choose SSE-KMS

Use SSE-KMS when you need to:

- Control encryption keys.
- Audit key usage.
- Restrict who can decrypt data.
- Meet regulatory or compliance requirements.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Encrypt S3 objects by default | **SSE-S3** |
| Audit every key usage | **SSE-KMS** |
| Control encryption with IAM and Key Policies | **SSE-KMS** |
| Minimize cost and administration | **SSE-S3** |
| Meet compliance requirements | **SSE-KMS** |
| Use AWS-managed encryption with no configuration | **SSE-S3** |
