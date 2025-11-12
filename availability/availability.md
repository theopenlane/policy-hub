---
title: System Availability Policy
satisfies:
  SOC 2:
    - A1.1 # system monitoring
    - A1.2 # incident response
    - A1.3 # disaster recovery
tags:
    - availability
---

## Purpose and Scope

1. Defines requirements for proper controls to protect the availability of the organization’s information systems.
1. Applies to all users of information systems (employees, contractors, and authorized external parties).
1. Must be readily available to all users.

## Background

1. Seeks to minimize unplanned downtime (outages) of information systems under the organization’s control.
1. Prescribes redundancy, failover, and monitoring measures to prevent outages or quickly remediate them.
1. Defines availability as the ability for information or systems to be accessed by authorized entities whenever needed.

## Policy

### General Availability
1. Information systems must be consistently available to conduct and support business operations.
1. Systems must have a defined availability classification, with appropriate controls enabled.
1. System and network failures must be reported promptly to IT leadership.
1. Scheduled outages must be communicated to users in advance with timing and expected duration.
1. Prior to production use, new or modified applications must complete a risk assessment that includes availability risks.

### Capacity and Load Management
1. Use capacity management and load balancing techniques to minimize system failure impact.

### Data Backups
1. Sensitive data must be restorable within a reasonable timeframe.
1. Perform full backups of critical resources weekly.
1. Perform incremental backups of critical resources daily.
1. Retain backups/media for at least 30 days and archive for one year (or longer per legal/regulatory needs).
1. Store backups off-site with redundancy and encryption.
1. Test backup data quarterly and configuration restores twice annually.

### Redundancy and Failover
1. Critical network infrastructure must have system-level redundancy (e.g., secondary power supply, backup arrays, spare routers/switches).
1. Critical servers must have redundant power supplies and NICs, with spare parts available.
1. High-availability servers must use disk mirroring.

### Business Continuity
1. Recovery time and data loss limits must follow the classification matrix in Appendix A.
1. Plans must identify critical resources, personnel, and corrective actions.
1. Responsibilities for responding to emergencies and resuming business operations must be defined.
1. Plans must satisfy all applicable legal and regulatory requirements.

# Appendix A: System Availability Classification Matrix

| Classification | Description                                                                 | RTO (Max Downtime) | RPO (Max Data Loss) | Examples                                |
|----------------|-----------------------------------------------------------------------------|--------------------|---------------------|-----------------------------------------|
| **High**       | Mission-critical systems. Outage severely impacts business operations, customers, or compliance obligations. Must be continuously available. | ≤ 1 hour           | ≤ 15 minutes        | Production database, payment systems, authentication services |
| **Medium**     | Important systems. Outage causes moderate disruption but operations can continue with workarounds for a limited time. | ≤ 4 hours          | ≤ 4 hours           | Internal file storage, HR systems, source code repositories |
| **Low**        | Non-critical systems. Outage causes minimal impact; restoration can be deferred. | Next business day  | ≤ 24 hours          | Internal wiki, test/dev environments, marketing website |