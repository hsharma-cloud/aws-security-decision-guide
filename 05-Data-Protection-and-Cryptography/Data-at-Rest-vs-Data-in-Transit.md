# Data at Rest vs Data in Transit

## Purpose

Data at Rest and Data in Transit represent two states of data that require different security controls. Data at Rest refers to data stored on persistent storage such as Amazon S3, Amazon EBS, Amazon RDS, or backups. Data in Transit refers to data actively moving between systems, applications, users, or AWS services across a network. AWS provides encryption mechanisms to protect both states of data using services such as AWS KMS, AWS Certificate Manager (ACM), and Transport Layer Security (TLS).

| Feature | Data at Rest | Data in Transit |
|---------|--------------|-----------------|
| Primary Purpose | Protect Stored Data | Protect Moving Data |
| Data State | Stored | Being Transmitted |
| Common Storage | S3, EBS, RDS, EFS | HTTPS, TLS, VPN, SSH |
| Encryption Method | AES-256, KMS | TLS/SSL |
| AWS Services | KMS, S3 Encryption, EBS Encryption | ACM, Elastic Load Balancer, API Gateway |
| Main Threat | Unauthorized Storage Access | Network Eavesdropping |
| Best For | Persistent Data Protection | Secure Communications |
| Typical Users | Storage Administrators | Network and Security Engineers |

## Key Differences

- Data at Rest is **stored** on disks or storage services.
- Data in Transit is **moving** across a network.
- Data at Rest is commonly protected using **AES encryption** and AWS KMS.
- Data in Transit is commonly protected using **TLS/SSL**.
- Both should be encrypted as part of a defense-in-depth security strategy.

## When to Protect Data at Rest

Protect Data at Rest when you need to:

- Encrypt Amazon S3 buckets.
- Encrypt Amazon EBS volumes.
- Protect database storage.
- Secure backups and snapshots.
- Meet compliance requirements.

## When to Protect Data in Transit

Protect Data in Transit when you need to:

- Secure HTTPS websites.
- Encrypt API communications.
- Protect VPN traffic.
- Secure SSH connections.
- Encrypt communication between AWS services.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Encrypt an Amazon S3 bucket | **Data at Rest** |
| Secure a web application with HTTPS | **Data in Transit** |
| Encrypt an EBS volume | **Data at Rest** |
| Protect API traffic | **Data in Transit** |
| Secure database storage | **Data at Rest** |
| Encrypt communication over the network | **Data in Transit** |
