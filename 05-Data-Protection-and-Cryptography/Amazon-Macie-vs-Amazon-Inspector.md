# Amazon Macie vs Amazon Inspector

## Purpose

Amazon Macie and Amazon Inspector are AWS security services that help identify security risks, but they focus on different assets. Amazon Macie discovers, classifies, and protects sensitive data stored in Amazon S3 using machine learning and pattern matching. Amazon Inspector continuously assesses Amazon EC2 instances, Amazon ECR container images, and AWS Lambda functions for software vulnerabilities and unintended network exposure.

| Feature | Amazon Macie | Amazon Inspector |
|---------|--------------|------------------|
| Primary Purpose | Sensitive Data Discovery | Vulnerability Management |
| Focus | Data Security | Workload Security |
| Scans | Amazon S3 Buckets | EC2, ECR, Lambda |
| Detects Sensitive Data | Yes | No |
| Detects Software Vulnerabilities | No | Yes |
| Detects CVEs | No | Yes |
| Uses Machine Learning | Yes | Yes (Service Intelligence) |
| Best For | Data Classification and Compliance | Vulnerability Assessment |
| Typical Users | Data Security Teams | Security Operations and Infrastructure Teams |

## Key Differences

- Amazon Macie protects **data**.
- Amazon Inspector protects **compute workloads**.
- Macie discovers sensitive information such as PII and financial data.
- Inspector identifies software vulnerabilities and network exposure.
- The two services complement each other and are commonly deployed together.

## When to Choose Amazon Macie

Use Amazon Macie when you need to:

- Discover personally identifiable information (PII).
- Identify sensitive data stored in Amazon S3.
- Meet data privacy and compliance requirements.
- Classify sensitive business information.
- Monitor S3 buckets for sensitive content.

## When to Choose Amazon Inspector

Use Amazon Inspector when you need to:

- Scan EC2 instances for vulnerabilities.
- Scan container images in Amazon ECR.
- Assess AWS Lambda functions.
- Detect Common Vulnerabilities and Exposures (CVEs).
- Prioritize remediation of security findings.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Find PII in Amazon S3 | **Amazon Macie** |
| Scan EC2 instances for CVEs | **Amazon Inspector** |
| Classify sensitive data | **Amazon Macie** |
| Assess container image vulnerabilities | **Amazon Inspector** |
| Meet data privacy compliance requirements | **Amazon Macie** |
| Identify software vulnerabilities | **Amazon Inspector** |
