# Identity-Based Policies vs Resource-Based Policies

## Purpose

Identity-Based Policies and Resource-Based Policies are the two primary authorization models in AWS. Identity-Based Policies are attached to IAM users, groups, or roles and define what actions those identities can perform. Resource-Based Policies are attached directly to AWS resources and define which principals are allowed to access those resources. Understanding both models is fundamental to designing secure AWS environments.

| Feature | Identity-Based Policies | Resource-Based Policies |
|---------|-------------------------|-------------------------|
| Primary Purpose | Grant Permissions to Identities | Grant Access to Resources |
| Attached To | IAM Users, Groups, Roles | AWS Resources |
| Controls | What an Identity Can Do | Who Can Access a Resource |
| Cross-Account Access | Supported (with Roles) | Native Support |
| Uses Principal Element | No | Yes |
| Common Services | IAM | S3, SQS, SNS, KMS, Lambda |
| Best For | Identity Management | Resource Sharing |
| Typical Users | IAM Administrators | Resource Owners |

## Key Differences

- Identity-Based Policies are attached to **IAM identities**.
- Resource-Based Policies are attached to **AWS resources**.
- Identity-Based Policies define **what actions an identity can perform**.
- Resource-Based Policies define **who can access a resource**.
- Many AWS services support both policy types, which AWS evaluates together during authorization.

## When to Choose Identity-Based Policies

Use Identity-Based Policies when you need to:

- Grant permissions to users or roles.
- Implement least privilege.
- Control access from the identity perspective.
- Manage permissions centrally through IAM.

## When to Choose Resource-Based Policies

Use Resource-Based Policies when you need to:

- Share resources across AWS accounts.
- Grant direct access to a resource.
- Control access from the resource perspective.
- Allow AWS services or external principals to access a resource.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Give a developer access to Amazon EC2 | **Identity-Based Policy** |
| Share an S3 bucket with another account | **Resource-Based Policy** |
| Grant permissions to an IAM role | **Identity-Based Policy** |
| Allow another AWS account to use a KMS key | **Resource-Based Policy** |
| Manage permissions for users and roles | **Identity-Based Policy** |
| Control access directly from the resource | **Resource-Based Policy** |
