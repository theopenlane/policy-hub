---
title: Testing Policy
satisfies:
  SOC 2:
    - CC7.2   # Change management procedures include testing prior to implementation
    - CC7.3   # Changes are authorized and tested before release
tags:
    - security
---

## Purpose and Scope

This policy establishes requirements for testing software, infrastructure, and system changes to ensure they function as intended and do not introduce security vulnerabilities. It applies to code developed for {{company_name}} products and services, infrastructure managed in production environments, and client software releases provided to customers.

## Background

Testing reduces the risk of introducing defects or vulnerabilities that could lead to security incidents or service disruption. Automated testing, CI/CD validation, and review processes help ensure consistent quality across environments. Testing is especially critical prior to production deployment; exceptions are permitted only under urgent circumstances such as incident response.

## Policy

### Code Changes

1. All production code changes that modify product functionality must be tested through the organization’s continuous integration (CI) system prior to merge.
1. Testing must not be conducted solely in local development environments or in live production systems.
1. Exception: urgent changes needed to resolve an incident may be merged without prior testing, provided they are documented in accordance with the Change Management Policy and tested or reviewed within two business days.
1. Non-functional changes (such as documentation updates, comments, or static text) may be exempt from mandatory testing.

### Client Releases

1. New client releases must undergo testing before general availability.
1. Testing must verify major product features on supported platforms.
1. New features should be released first through an unstable or beta channel before inclusion in stable releases.
1. Exception: urgent security fixes may be released directly to stable channels.

### Infrastructure Changes

1. Infrastructure changes should be tested when feasible before deployment to production.
1. Infrastructure should be managed “as code” to allow review, approval, and testing similar to application code.
1. Testing should validate security controls, failover behavior, and monitoring or alerting coverage.
