---
title: Access Control Policy
satisfies:
  SOC 2:
    - CC6.1  # Logical access controls
    - CC6.3  # Authentication and monitoring of access
    - CC6.6  # Restriction of privileged access
    - CC6.8  # Controls over end-user devices
tags:
    - security
---

## Purpose and Scope

This policy governs access to {{company_name}}’s internal systems, including the production network, production services, corporate systems, and SaaS applications. It applies to all employees, contractors, and vendors throughout the full access lifecycle—from initial onboarding to modification and removal of access.

## Background

Access must be granted in a way that supports authorized business use while protecting sensitive systems and data. Strong access and device security controls reduce the risk of unauthorized disclosure, misuse, or compromise of organizational information.

## Policy

### Access to Internal Systems

1. Access controls must be enforced through technical measures such as IAM, MFA, and conditional access where applicable.
1. Logon attempts, successful authentications, failures, and session activity must be recorded and retained in accordance with the Logging and Monitoring Policy.
1. Administrative activities must be logged where technically feasible.
1. At least two individuals must hold full administrative access for any critical production system or service that stores or processes customer data.

### Granular Access Controls

1. Systems must support role-based, least-privilege access, granting only the minimum permissions required to perform authorized job duties.
1. Entitlements must reflect business requirements without exposing unnecessary systems or data.

### End-User Devices

1. Employees, contractors, and vendors are responsible for the secure handling of company-issued devices.
1. Devices must use full-disk encryption, automatic screen locking, and company-approved endpoint protection.
1. Lost or stolen devices must be reported immediately and treated as a security incident; remote wipe must be initiated when appropriate.

### Changing Roles or Responsibilities

1. Accounts belonging to terminated users must be disabled within one business day.
1. Access for users who transfer roles must be reviewed and updated promptly to align with current responsibilities.
1. The Security or IT team must conduct periodic access reviews and remediate unnecessary access.