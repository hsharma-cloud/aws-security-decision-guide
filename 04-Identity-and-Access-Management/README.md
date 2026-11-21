# Identity and Access Management

## Overview

Identity and Access Management (IAM) is the foundation of AWS security. It ensures that the right identities have the appropriate level of access to AWS resources while enforcing the principle of least privilege. Effective IAM reduces the risk of unauthorized access, protects sensitive resources, and simplifies security administration across AWS environments.

AWS provides a comprehensive set of identity and access management services, including AWS Identity and Access Management (IAM), IAM Identity Center, AWS Organizations, AWS Resource Access Manager (RAM), AWS Secrets Manager, AWS Key Management Service (KMS), IAM Access Analyzer, AWS Security Token Service (STS), and Amazon Cognito.

Rather than viewing these services independently, security engineers should understand how they work together to authenticate users, authorize access, manage permissions, protect credentials, and securely share AWS resources across accounts.

## Decision Guides

1. IAM Users vs IAM Roles
2. IAM Roles vs Resource-Based Policies
3. IAM Policies vs SCPs
4. IAM Identity Center vs IAM Users
5. IAM Identity Center vs Amazon Cognito
6. IAM Roles vs STS
7. IAM Access Analyzer vs IAM Policy Simulator
8. Secrets Manager vs Systems Manager Parameter Store
9. KMS vs CloudHSM
10. Customer Managed Keys vs AWS Managed Keys
11. Inline Policies vs Managed Policies
12. Permission Boundaries vs SCPs
13. Cross-Account Roles vs Resource-Based Policies
14. Authentication vs Authorization
15. Identity-Based Policies vs Resource-Based Policies
