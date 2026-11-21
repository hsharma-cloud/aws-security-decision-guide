# Macie vs Inspector

## Purpose

Amazon Macie and Amazon Inspector both help improve AWS security but focus on different areas. Amazon Macie discovers and protects sensitive data stored in Amazon S3, while Amazon Inspector identifies software vulnerabilities and unintended network exposure in compute workloads.

| Feature | Amazon Macie | Amazon Inspector |
|---------|--------------|------------------|
| Primary Purpose | Sensitive Data Discovery | Vulnerability Management |
| Focus | Data Security | Workload Security |
| Protects | Amazon S3 | EC2, ECR, Lambda |
| Identifies | Sensitive data (PII, financial data, credentials) | CVEs, missing patches, vulnerable packages |
| Uses ML | Yes | No |
| Compliance Support | Yes | Yes |
| Typical Users | Data Security, Compliance Teams | Security Engineers, Vulnerability Management Teams |

## Key Differences

- Macie protects **data**.
- Inspector protects **workloads**.
- Macie discovers sensitive information stored in Amazon S3.
- Inspector scans workloads for known software vulnerabilities.
- Together they provide both data protection and workload security.

## When to Choose Macie

Use Macie when you need to:

- Discover sensitive data in S3.
- Identify Personally Identifiable Information (PII).
- Monitor data privacy risks.
- Support compliance initiatives.

## When to Choose Inspector

Use Inspector when you need to:

- Scan workloads for vulnerabilities.
- Detect missing security patches.
- Prioritize CVEs.
- Continuously assess compute resources.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Discover sensitive data | **Amazon Macie** |
| Scan workloads for vulnerabilities | **Amazon Inspector** |
| Protect data stored in S3 | **Amazon Macie** |
| Identify missing patches | **Amazon Inspector** |
| Detect PII | **Amazon Macie** |
| Find CVEs | **Amazon Inspector** |
