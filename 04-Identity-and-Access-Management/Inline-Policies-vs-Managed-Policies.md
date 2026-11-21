# Inline Policies vs Managed Policies

## Purpose

Inline Policies and Managed Policies are two ways to assign permissions in AWS IAM. Inline Policies have a one-to-one relationship with a single IAM identity and are deleted when that identity is deleted. Managed Policies are standalone policy objects that can be attached to multiple users, groups, and roles, making them reusable and easier to manage.

| Feature | Inline Policies | Managed Policies |
|---------|-----------------|------------------|
| Primary Purpose | Identity-Specific Permissions | Reusable Permissions |
| Relationship | One-to-One | One-to-Many |
| Reusable | No | Yes |
| Attached To | Single User, Group, or Role | Multiple Users, Groups, and Roles |
| Central Management | No | Yes |
| Versioning | No | Yes (Customer Managed Policies) |
| Best For | Unique Exceptions | Standardized Permissions |
| Typical Users | IAM Administrators | Enterprise IAM Teams |

## Key Differences

- Inline Policies are **embedded directly** into an IAM identity.
- Managed Policies exist **independently** of IAM identities.
- Managed Policies can be reused across multiple identities.
- Inline Policies are deleted with the identity.
- AWS recommends Managed Policies for most environments because they simplify permission management.

## When to Choose Inline Policies

Use Inline Policies when you need to:

- Create one-off permissions.
- Apply unique exceptions.
- Prevent policy reuse.
- Assign identity-specific access.

## When to Choose Managed Policies

Use Managed Policies when you need to:

- Standardize permissions.
- Reuse policies across identities.
- Simplify permission management.
- Support enterprise-scale IAM.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Create unique permissions for one user | **Inline Policy** |
| Reuse a policy across many roles | **Managed Policy** |
| Standardize access control | **Managed Policy** |
| Assign a one-time exception | **Inline Policy** |
| Centrally manage permissions | **Managed Policy** |
| Follow AWS IAM best practices | **Managed Policy** |
