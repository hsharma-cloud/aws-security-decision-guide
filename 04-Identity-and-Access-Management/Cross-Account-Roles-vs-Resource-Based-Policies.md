# Cross-Account Roles vs Resource-Based Policies

## Purpose

Cross-Account IAM Roles and Resource-Based Policies both enable access across AWS accounts, but they accomplish this differently. Cross-Account Roles allow trusted identities in another AWS account to assume a role and receive temporary credentials, while Resource-Based Policies grant another AWS account or principal direct access to a specific AWS resource without assuming a role.

| Feature | Cross-Account IAM Roles | Resource-Based Policies |
|---------|-------------------------|-------------------------|
| Primary Purpose | Cross-Account Identity Access | Cross-Account Resource Access |
| Access Method | AssumeRole (STS) | Resource Policy |
| Temporary Credentials | Yes | No |
| Uses AWS STS | Yes | No |
| Attached To | IAM Role | AWS Resource |
| Common Services | EC2, Lambda, Organizations | S3, SQS, SNS, KMS |
| Best For | Administrative Access | Resource Sharing |
| Typical Users | Security Administrators | Resource Owners |

## Key Differences

- Cross-Account Roles grant access **to an identity**.
- Resource-Based Policies grant access **to a resource**.
- Cross-Account Roles use **AWS STS** to issue temporary credentials.
- Resource-Based Policies directly trust another AWS principal.
- Many AWS services support Resource-Based Policies for secure cross-account sharing.

## When to Choose Cross-Account IAM Roles

Use Cross-Account Roles when you need to:

- Delegate administration.
- Provide temporary credentials.
- Support cross-account automation.
- Apply least-privilege access for users and applications.

## When to Choose Resource-Based Policies

Use Resource-Based Policies when you need to:

- Share an S3 bucket.
- Allow another account to access an SQS queue or SNS topic.
- Share a KMS key.
- Grant access directly from the resource.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Delegate administrator access to another account | **Cross-Account IAM Role** |
| Share an S3 bucket | **Resource-Based Policy** |
| Issue temporary credentials | **Cross-Account IAM Role** |
| Share a KMS key | **Resource-Based Policy** |
| Enable cross-account automation | **Cross-Account IAM Role** |
| Control access from the resource itself | **Resource-Based Policy** |
