# Customer Managed Keys vs AWS Managed Keys

## Purpose

Customer Managed Keys (CMKs) and AWS Managed Keys are both encryption keys stored and protected by AWS Key Management Service (KMS), but they differ in ownership, control, and management capabilities. Customer Managed Keys give customers full control over key policies, rotation, and lifecycle management, while AWS Managed Keys are automatically created and managed by AWS for use with specific AWS services.

| Feature | Customer Managed Keys | AWS Managed Keys |
|---------|-----------------------|------------------|
| Primary Purpose | Customer-Controlled Encryption | AWS Service Encryption |
| Key Ownership | Customer | AWS |
| Key Policy Management | Yes | No |
| Automatic Rotation | Optional (Customer Controlled) | AWS Managed |
| Key Deletion | Yes | No |
| Cross-Account Sharing | Yes | No |
| Audit Control | Full | Limited |
| Cost | Additional Charges Apply | No Additional Key Charge |
| Typical Users | Security Engineers | General AWS Users |

## Key Differences

- Customer Managed Keys provide **full administrative control**.
- AWS Managed Keys are **automatically managed by AWS**.
- CMKs allow custom key policies and cross-account access.
- AWS Managed Keys cannot be modified by customers.
- AWS recommends Customer Managed Keys when fine-grained access control or compliance is required.

## When to Choose Customer Managed Keys

Use Customer Managed Keys when you need to:

- Define custom key policies.
- Share keys across AWS accounts.
- Control key rotation.
- Meet regulatory or compliance requirements.
- Manage the full key lifecycle.

## When to Choose AWS Managed Keys

Use AWS Managed Keys when you need to:

- Encrypt AWS resources with minimal administration.
- Use default encryption.
- Reduce operational overhead.
- Quickly secure AWS services.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Control key policies | **Customer Managed Key** |
| Use default AWS encryption | **AWS Managed Key** |
| Share keys across accounts | **Customer Managed Key** |
| Minimize administration | **AWS Managed Key** |
| Manage key rotation yourself | **Customer Managed Key** |
| Encrypt resources with default settings | **AWS Managed Key** |
