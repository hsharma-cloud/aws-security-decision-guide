# Hashing vs Encryption

## Purpose

Hashing and Encryption are both cryptographic techniques, but they serve fundamentally different purposes. Hashing creates a fixed-length digest that cannot be reversed and is primarily used to verify data integrity. Encryption transforms readable data into ciphertext that can later be decrypted with the appropriate key, providing confidentiality for sensitive information.

| Feature | Hashing | Encryption |
|---------|---------|------------|
| Primary Purpose | Verify Integrity | Protect Confidentiality |
| Reversible | No | Yes |
| Uses Keys | No | Yes |
| Output | Fixed-Length Hash | Variable-Length Ciphertext |
| Data Recovery | Impossible | Possible with Correct Key |
| Common Algorithms | SHA-256, SHA-384, SHA-512 | AES, RSA, ECC |
| Typical Uses | Password Verification, Integrity Checks | Data Protection, Secure Communication |
| Typical Users | Security Engineers | Security and Application Engineers |

## Key Differences

- Hashing is **one-way** and cannot be reversed.
- Encryption is **two-way** and allows data to be decrypted.
- Hashing verifies whether data has changed.
- Encryption prevents unauthorized users from reading data.
- Passwords should be stored as secure password hashes, not encrypted values.

## When to Choose Hashing

Use Hashing when you need to:

- Verify file integrity.
- Store passwords securely.
- Detect unauthorized modifications.
- Validate downloaded software.
- Generate checksums.

## When to Choose Encryption

Use Encryption when you need to:

- Protect confidential information.
- Encrypt files and databases.
- Secure network communications.
- Protect customer data.
- Meet data confidentiality requirements.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Verify file integrity | **Hashing** |
| Encrypt sensitive documents | **Encryption** |
| Store user passwords securely | **Hashing** |
| Protect Amazon S3 objects | **Encryption** |
| Detect tampering | **Hashing** |
| Secure confidential communications | **Encryption** |
