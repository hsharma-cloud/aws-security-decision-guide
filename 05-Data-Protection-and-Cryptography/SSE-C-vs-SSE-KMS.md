# SSE-C vs SSE-KMS

## Purpose

Server-Side Encryption with Customer-Provided Keys (SSE-C) and Server-Side Encryption with AWS Key Management Service (SSE-KMS) both encrypt Amazon S3 objects on the server side, but they differ in who manages the encryption keys. With SSE-C, customers provide and manage their own encryption keys for every request. With SSE-KMS, AWS KMS securely stores and manages encryption keys while providing centralized access control, auditing, and key lifecycle management.

| Feature | SSE-C | SSE-KMS |
|---------|--------|----------|
| Primary Purpose | Customer-Supplied Encryption Keys | AWS KMS Managed Encryption |
| Key Management | Customer | AWS KMS |
| Key Storage | Customer | AWS KMS |
| Key Sent with Every Request | Yes | No |
| CloudTrail Logging | No | Yes |
| IAM & Key Policies | No | Yes |
| Automatic Key Rotation | Customer Responsibility | Supported |
| Operational Complexity | High | Low |
| Best For | Customer-Controlled Key Management | Enterprise AWS Workloads |
| Typical Users | Specialized Compliance Environments | Most AWS Customers |

## Key Differences

- SSE-C requires customers to **provide the encryption key with every request**.
- SSE-KMS securely stores keys in **AWS KMS**.
- SSE-C places full responsibility for key management on the customer.
- SSE-KMS supports IAM policies, KMS key policies, and CloudTrail auditing.
- AWS generally recommends SSE-KMS over SSE-C for most workloads.

## When to Choose SSE-C

Use SSE-C when you need to:

- Maintain complete control over encryption keys.
- Keep encryption keys outside AWS.
- Meet regulatory requirements that prohibit AWS-managed key storage.
- Integrate with an external key management process.

## When to Choose SSE-KMS

Use SSE-KMS when you need to:

- Centrally manage encryption keys.
- Audit key usage.
- Control decryption permissions with IAM.
- Simplify encryption management.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Keep encryption keys outside AWS | **SSE-C** |
| Use AWS KMS for centralized key management | **SSE-KMS** |
| Audit key usage with CloudTrail | **SSE-KMS** |
| Provide your own encryption key for every upload | **SSE-C** |
| Simplify operational management | **SSE-KMS** |
| Meet strict customer-managed key requirements | **SSE-C** |
