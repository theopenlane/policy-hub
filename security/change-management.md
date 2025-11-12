---
title: Change Management
satisfies:
  SOC 2:
    - CC8.1 # change management
    - CC7.2   # Change management procedures include testing prior to implementation
    - CC7.3   # Changes are authorized and tested before release
tags:
    - security
---

## Purpose and Scope

This policy establishes change management requirements to ensure only authorized, reviewed, and approved changes are made to {{company_name}}’s systems and processes. It applies to all changes affecting production systems, infrastructure, applications, and security policies.

## Background

Unmanaged changes can introduce vulnerabilities, outages, or compliance failures. Proper change management ensures changes are reviewed, approved, tested, documented, and communicated to minimize risk. Emergency changes may be permitted under this policy, but must be subject to retrospective review to maintain accountability.

## Policy

### Code Changes

1. All code changes must be made through a pull request.
1. Each pull request must be reviewed and approved by at least one peer before merging.
1. Branch protection rules must enforce required approvals and prevent unauthorized changes.
1. Emergency fixes may be pushed without prior review and testing to resolve an incident, but must be reviewed within two business days.
1. Documentation-only changes, marketing website updates, and other non-substantive code changes are exempt from peer review and mandatory testing.
1. Dependency updates may be merged without an additional reviewer, provided release notes are reviewed prior to merging.
1. All production code changes that modify product functionality must be tested through the organization’s continuous integration (CI) system prior to merge.
1. Testing must not be conducted solely in local development environments or in live production systems.

### Client Releases

1. New client releases must undergo testing before general availability.
1. Testing must verify major product features on supported platforms.
1. New features should be released first through an unstable or beta channel before inclusion in stable releases.
1. Exception: urgent security fixes may be released directly to stable channels.


### Infrastructure Changes

1. Infrastructure changes must be communicated in advance to relevant teams.
1. Infrastructure should be managed “as code” to allow review, approval, and testing similar to application code.
1. Where infrastructure is managed through infrastructure-as-code, changes must undergo peer review and testing before deployment to production.
1. Manual infrastructure changes must have documented approvals retained for audit purposes.
1. Critical infrastructure must have at least two designated administrators with full rights to prevent single points of failure.
1. Testing should validate security controls, failover behavior, and monitoring or alerting coverage.

### Customer Account Changes

1. Changes to customer accounts may only be performed in response to validated support requests.
1. Security or compliance issues may require immediate changes without prior customer action; such changes must be documented and customers notified as appropriate.

### Security Policy Changes

1. All security policies must include a changelog capturing what changed, when, and by whom.
1. Policies must be reviewed at least annually for accuracy, alignment with business needs, and coverage of emerging risks.
1. Reviews must confirm that implemented controls remain sufficient and effective.

### Review and Oversight

1. Security and engineering leadership must review high-risk or high-impact changes before implementation.
1. Post-change reviews must be conducted to identify lessons learned and necessary follow-up actions.
1. Logs of changes, approvals, and reviews must be retained to support audit and compliance requirements.
