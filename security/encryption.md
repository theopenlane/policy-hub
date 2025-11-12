---
title: Data Encryption
satisfies:
  SOC 2:
    - CC6.6
    - CC6.7
    - CC6.8
tags:
    - security
---

## Purpose and Scope

This policy defines the requirements for using cryptographic controls and key management practices to protect the confidentiality, integrity, authenticity, and non-repudiation of information. It applies to all systems, equipment, facilities, and data within scope of {{company_name}}’s information security program, as well as all employees, contractors, service providers, and others who work with or manage cryptographic systems, algorithms, or key material.

## Background

To ensure consistent and secure protection of information, {{company_name}} adopts a standardized approach to the use of cryptographic controls across all environments. This policy establishes expectations for approved algorithms, key management practices, and the use of cryptography in cloud and production systems to provide end-to-end protection and interoperability.

## Policy

### Approved Cryptographic Controls

{{company_name}} uses industry-standard cryptographic algorithms and key strengths to protect data in transit and at rest. The following controls are approved for production systems:

| **System / Type**                  | **Tool**             | **Algorithm** | **Key Size**  |
|------------------------------------|----------------------|---------------|---------------|
| Public Key Infrastructure (PKI)    | OpenSSL (3.x)        | AES-256       | 256-bit key   |
| Data Encryption Keys               | OpenSSL (3.x)        | AES-256       | 256-bit key   |
| Virtual Private Network (VPN)      | OpenSSL / OpenVPN    | AES-256       | 256-bit key   |
| Transport Layer Security (TLS)     | OpenSSL, Cert Mgmt   | AES-256 (TLS) | 256-bit key   |

⚠️ Note: TLS 1.2 or higher is required; TLS 1.3 is strongly recommended. SSL protocols are prohibited.

### Encryption In Transit

1. All data transmitted over public or untrusted networks must be encrypted using TLS 1.2 or higher.
1. Encryption must be enforced for all externally facing services, APIs, administrative interfaces, and connections between production services.

### Encryption At Rest

1. All customer data, secrets, and sensitive internal information stored within production systems must be encrypted at rest using strong, industry-standard algorithms such as AES-256.
1. Disk-level encryption, database encryption, or application-level encryption must be used to protect data in the event of unauthorized system or media access.

### Key Management

1. Encryption keys must be protected against loss, modification, or destruction through strict access controls and secure storage.
1. Keys must be generated, stored, backed up, rotated, and retired using an approved Key Management Service (KMS).
1. Keys must never be exported or shared outside the approved KMS, and access must be limited to authorized users and administrators.
1. Key rotation must occur at least annually, or immediately if compromise or personnel changes introduce risk.

### Cloud Environments

1. Encryption in cloud environments must comply with all applicable laws and regional restrictions.
1. Customers may request information about the cryptographic tools used to protect their data and any available customer-managed encryption options.