# Data Protection and Cryptography

## Overview

Data Protection and Cryptography are fundamental to securing information throughout its lifecycle in AWS. Organizations must protect sensitive data both at rest and in transit while ensuring proper encryption key management, certificate handling, tokenization, and secure storage practices.

AWS provides multiple services and features to help secure data, including AWS Key Management Service (KMS), AWS CloudHSM, AWS Certificate Manager (ACM), AWS Secrets Manager, Systems Manager Parameter Store, Amazon Macie, Amazon S3 encryption options, AWS Private CA, and client-side encryption libraries.

Security engineers should understand when to use each service, how they integrate, and which solution best fits a given security or compliance requirement.

## Decision Guides

1. Server-Side Encryption vs Client-Side Encryption
2. SSE-S3 vs SSE-KMS
3. SSE-KMS vs DSSE-KMS
4. SSE-C vs SSE-KMS
5. Envelope Encryption vs Direct Encryption
6. AWS Certificate Manager vs AWS Private CA
7. AWS Private CA vs Self-Managed CA
8. Secrets Manager vs KMS
9. KMS Key Policies vs IAM Policies
10. Data at Rest vs Data in Transit
11. Symmetric Keys vs Asymmetric Keys
12. Digital Signature vs Encryption
13. Hashing vs Encryption
14. Tokenization vs Encryption
15. Amazon Macie vs Amazon Inspector
