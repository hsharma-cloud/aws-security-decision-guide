# Authentication vs Authorization

## Purpose

Authentication and Authorization are the two core components of access control in AWS. Authentication verifies **who** a user or service is, while Authorization determines **what** that authenticated identity is allowed to do. Every AWS request first goes through authentication before AWS evaluates authorization policies.

| Feature | Authentication | Authorization |
|---------|----------------|---------------|
| Primary Purpose | Verify Identity | Grant or Deny Permissions |
| Answers | Who are you? | What can you do? |
| Occurs First | Yes | No |
| Uses | Passwords, MFA, Access Keys, Federation | IAM Policies, SCPs, Resource Policies |
| Failure Result | Identity Not Verified | Access Denied |
| AWS Services | IAM, IAM Identity Center, Cognito, STS | IAM, SCPs, Permission Boundaries, Resource Policies |
| Typical Users | All AWS Identities | All AWS Identities |

## Key Differences

- Authentication verifies **identity**.
- Authorization verifies **permissions**.
- Authentication always occurs before authorization.
- A successfully authenticated identity can still be denied access if it lacks the required permissions.
- AWS evaluates IAM policies, resource-based policies, SCPs, permission boundaries, and session policies during authorization.

## When Authentication Applies

Authentication is required when you need to:

- Sign in to the AWS Management Console.
- Assume an IAM role.
- Authenticate using MFA.
- Obtain temporary credentials through AWS STS.
- Verify the identity of a user or application.

## When Authorization Applies

Authorization is required when AWS needs to:

- Determine whether an action is allowed.
- Evaluate IAM policies.
- Check resource-based policies.
- Apply SCPs and permission boundaries.
- Enforce least-privilege access.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Verify a user's identity | **Authentication** |
| Determine if an EC2 instance can access S3 | **Authorization** |
| Validate MFA credentials | **Authentication** |
| Evaluate IAM policies | **Authorization** |
| Confirm who is making a request | **Authentication** |
| Decide whether to allow an AWS API call | **Authorization** |
