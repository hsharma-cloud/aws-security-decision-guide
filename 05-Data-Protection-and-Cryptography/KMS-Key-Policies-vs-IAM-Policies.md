# KMS Key Policies vs IAM Policies

## Purpose

KMS Key Policies and IAM Policies both control access to AWS KMS keys, but they operate at different levels. KMS Key Policies are resource-based policies attached directly to a KMS key and define who can use or manage that key. IAM Policies are identity-based policies attached to IAM users, groups, or roles and specify what KMS actions an identity can perform. In most cases, access to a KMS key requires both the Key Policy and the IAM Policy to allow the requested action.

| Feature | KMS Key Policies | IAM Policies |
|---------|------------------|--------------|
| Primary Purpose | Control Access to a Specific KMS Key | Grant Permissions to IAM Identities |
| Policy Type | Resource-Based | Identity-Based |
| Attached To | KMS Key | IAM User, Group, or Role |
| Required for KMS Access | Yes | Usually Yes |
| Scope | Single KMS Key | Multiple AWS Resources |
| Cross-Account Support | Yes | Limited (Requires Key Policy) |
| Best For | Key Administration | User and Role Permissions |
| Typical Users | Security Administrators | IAM Administrators |

## Key Differences

- KMS Key Policies are attached **directly to a KMS key**.
- IAM Policies are attached **to IAM identities**.
- KMS Key Policies determine **who can use or manage the key**.
- IAM Policies determine **what actions an identity is allowed to perform**.
- For most KMS operations, both the Key Policy and the IAM Policy must allow access.

## When to Choose KMS Key Policies

Use KMS Key Policies when you need to:

- Control access to a specific KMS key.
- Enable cross-account key usage.
- Define key administrators.
- Secure cryptographic operations.

## When to Choose IAM Policies

Use IAM Policies when you need to:

- Grant KMS permissions to users or roles.
- Apply least-privilege access.
- Manage permissions across AWS services.
- Centralize identity permissions.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Control who can use a specific KMS key | **KMS Key Policy** |
| Grant a role permission to encrypt data | **IAM Policy** |
| Configure cross-account KMS access | **KMS Key Policy** |
| Manage permissions for IAM users | **IAM Policy** |
| Define key administrators | **KMS Key Policy** |
| Apply least privilege to identities | **IAM Policy** |
