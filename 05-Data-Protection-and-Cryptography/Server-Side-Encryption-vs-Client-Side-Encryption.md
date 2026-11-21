# Server-Side Encryption vs Client-Side Encryption

## Purpose

Server-Side Encryption (SSE) and Client-Side Encryption (CSE) both protect data at rest, but they differ in where encryption occurs and who manages the encryption process. With Server-Side Encryption, AWS encrypts data after it is received and decrypts it before returning it to authorized users. With Client-Side Encryption, data is encrypted before it leaves the client and remains encrypted until it is decrypted by the client.

| Feature | Server-Side Encryption (SSE) | Client-Side Encryption (CSE) |
|---------|-------------------------------|------------------------------|
| Primary Purpose | Encrypt Data in AWS | Encrypt Data Before Upload |
| Encryption Location | AWS | Client Application |
| Decryption Location | AWS | Client Application |
| Key Management | AWS or Customer (KMS/SSE-C) | Customer |
| AWS Can See Plaintext | Yes (during processing) | No |
| Operational Complexity | Low | High |
| Performance Impact | Low | Client Dependent |
| Best For | Most AWS Workloads | Highly Sensitive Data |
| Typical Users | Cloud Engineers | Security Architects |

## Key Differences

- Server-Side Encryption encrypts data **after it reaches AWS**.
- Client-Side Encryption encrypts data **before it leaves the client**.
- SSE simplifies encryption management.
- CSE gives customers complete control over encryption.
- CSE is commonly used when organizations require AWS to never access plaintext data.

## When to Choose Server-Side Encryption

Use Server-Side Encryption when you need to:

- Protect data stored in AWS.
- Simplify encryption management.
- Integrate with AWS services.
- Meet standard compliance requirements.

## When to Choose Client-Side Encryption

Use Client-Side Encryption when you need to:

- Encrypt data before transmission.
- Maintain full control of encryption keys.
- Prevent cloud providers from viewing plaintext.
- Meet strict security or regulatory requirements.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Encrypt Amazon S3 objects easily | **Server-Side Encryption** |
| Ensure AWS never sees plaintext | **Client-Side Encryption** |
| Minimize operational overhead | **Server-Side Encryption** |
| Maintain complete control over encryption | **Client-Side Encryption** |
| Integrate with AWS managed encryption | **Server-Side Encryption** |
| Encrypt data before upload | **Client-Side Encryption** |
