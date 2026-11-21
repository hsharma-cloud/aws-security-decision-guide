# SSE-KMS vs DSSE-KMS

## Purpose

Server-Side Encryption with AWS KMS (SSE-KMS) and Dual-Layer Server-Side Encryption with AWS KMS (DSSE-KMS) both protect Amazon S3 objects using AWS Key Management Service (KMS). SSE-KMS encrypts data with a single layer of KMS-based encryption, while DSSE-KMS applies two independent layers of server-side encryption using AWS KMS to meet stringent regulatory and compliance requirements.

| Feature | SSE-KMS | DSSE-KMS |
|---------|----------|-----------|
| Primary Purpose | Single-Layer Encryption | Dual-Layer Encryption |
| Encryption Layers | One | Two Independent Layers |
| Uses AWS KMS | Yes | Yes |
| AWS Managed | Yes | Yes |
| CloudTrail Logging | Yes | Yes |
| KMS Key Policies | Yes | Yes |
| Compliance Support | Standard | Enhanced Regulatory Requirements |
| Performance | Lower Overhead | Slightly Higher Overhead |
| Typical Users | Most AWS Workloads | Highly Regulated Industries |

## Key Differences

- SSE-KMS encrypts data using **one KMS-based encryption layer**.
- DSSE-KMS encrypts data using **two independent encryption layers**.
- Both provide centralized key management through AWS KMS.
- Both support CloudTrail logging and KMS key policies.
- DSSE-KMS is intended for workloads requiring additional protection or compliance with strict regulatory standards.

## When to Choose SSE-KMS

Use SSE-KMS when you need to:

- Encrypt sensitive S3 data.
- Audit key usage.
- Control access with KMS key policies.
- Meet standard compliance requirements.

## When to Choose DSSE-KMS

Use DSSE-KMS when you need to:

- Meet enhanced regulatory requirements.
- Apply dual-layer encryption.
- Increase protection for highly sensitive data.
- Strengthen defense-in-depth for stored objects.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Encrypt S3 objects with KMS | **SSE-KMS** |
| Apply two independent encryption layers | **DSSE-KMS** |
| Audit encryption key usage | **SSE-KMS** |
| Meet stricter compliance requirements | **DSSE-KMS** |
| Use standard KMS encryption | **SSE-KMS** |
| Provide enhanced protection for sensitive data | **DSSE-KMS** |
