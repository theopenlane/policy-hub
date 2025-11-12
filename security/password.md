---
title: Password Policy
satisfies:
  SOC 2:
    - CC6.1   # Restricts logical access to authorized users via secure authentication
    - CC6.2   # Access based on roles and responsibilities, requiring unique credentials
    - CC6.3   # Access removed or modified when no longer required
    - CC6.6   # Encryption and protection of authentication data
tags:
    - security
---

## Purpose and Scope

This policy defines the requirements for selecting, securing, and managing passwords used to access {{company_name}} systems and services. It applies to all employees, contractors, and third parties who access {{company_name}} systems, networks, applications, or infrastructure.

## Policy

### Password Strength

1. Passwords must be unique for each system or service.
1. Passwords must be randomly generated.
1. Default passwords must be changed immediately after system installation.
1. Initial passwords issued to users must be changed upon first login.
1. Passwords do not require scheduled rotation; however, they must be changed immediately if compromise is known or suspected.

### Single Sign-On (SSO)

1. Where a third-party application supports SSO, it must be used.

### Multi-Factor Authentication (MFA)

1. Where a third-party application supports MFA, it must be used, and enforcement must be enabled when possible.
1. Acceptable MFA methods include WebAuthn hardware tokens, embedded hardware tokens (e.g., Touch ID), or authentication apps.
1. WebAuthn hardware or embedded hardware tokens are preferred over authentication apps.

### Password Manager

1. Where SSO is not supported, passwords must be stored in a company-approved password manager.

### Password Storage and Logging

1. Passwords must be encrypted at rest.
1. Passwords must not be logged under any circumstances.

### Requirements for Specific Use Cases

#### Servers
1. Access to production, development, and testing servers must use MFA with a password or must rely on per-user public key authentication (e.g., SSH keys).

#### Automated Processes
1. Automated processes such as CI/CD jobs or deployment tools must use passwords or API keys to authenticate.
1. Passwords or secrets used in scripts must be encrypted at rest.

#### End-User Devices
1. End-user devices must use passwords to encrypt disks and unlock the device.
1. Device passwords must be unique per individual, though they may be reused across that individual’s personal devices.
1. These passwords do not need to be randomly generated.

#### SaaS Applications and Other Software
1. Access to SaaS applications must use SSO where possible and MFA where supported.
1. Passwords used for password-vault access must be unique, but do not need to be randomly generated.
