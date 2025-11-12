---
title: Disaster Recovery Requirements
satisfies:
  SOC 2:
    - A1.1 # system availability
    - A1.2 # backup and restoration
    - A1.3 # system recovery plan
    - CC7.2 # monitoring of anomalies
tags:
    - security
---

## Purpose and Scope

This policy defines {{company_name}}’s disaster recovery requirements for restoring IT infrastructure, systems, and services within acceptable timeframes following a disruption. It establishes key recovery objectives, including the **Recovery Time Objective (RTO)**—the maximum allowable downtime—and the **Recovery Point Objective (RPO)**—the maximum allowable data loss, measured in time. This policy applies to all personnel and suppliers involved in disaster recovery planning and execution.

## Background

Disasters or major outages can threaten system availability and business operations. This policy outlines {{company_name}}’s disaster recovery strategy, including roles, procedures, and recovery objectives, and defines the conditions required for successful execution, such as backup availability, failover capability, and regular testing. This policy does not apply to incidents isolated to a single customer or outages solely within core cloud provider infrastructure.

## Policy

### Relocation

1. If the primary site becomes unavailable, an alternate environment must be used to restore critical systems.
1. Designated personnel are responsible for initiating relocation procedures and executing restoration activities.

### Critical Services, Key Tasks, and SLAs

1. Critical systems must be restored in priority order based on business impact.
1. Recovery activities must align with all SLAs, regulatory requirements, RTOs, and RPOs.
1. Restoration must be completed within the defined RTO, and data recovered within the defined RPO thresholds.

### Backups

1. Backups must be maintained and regularly tested to ensure they can support full recovery.
1. Security and IT teams must:
   1. Verify backups exist for all critical systems and data.
   1. Test backup and restoration procedures at least annually.
   1. Review architecture and redundancy plans for resiliency.
   1. Monitor backup jobs and storage systems for failures or risks.

### Outage Detection

1. Outages may be detected through automated monitoring, employee reports, or third-party notifications.
1. Confirmed outages must follow the incident response process and, when appropriate, trigger activation of the Disaster Recovery Plan (DRP).

### Notification of Plan Initiation

1. Specific personnel must be notified when the DRP is activated.
1. Responsibility for issuing notifications must be assigned to a designated role.

### Plan Deactivation

1. Only authorized personnel may deactivate the DRP.
1. Deactivation may occur only after relocation and restoration activities are complete and services are stable.
1. Personnel must be notified when the DRP is deactivated.

### Execution

1. Normal operations must be restored as quickly as possible.
1. Internal and external contact lists must be maintained and kept current in Appendix A.
1. Pre-approved recovery tasks (e.g., purchases, communications, or vendor interactions) may be executed as needed to support restoration.

### Testing and Review

1. The DRP must be reviewed and tested at least twice per year, including relocation and recovery rehearsals.
1. A walkthrough review of recovery procedures and backup processes must be conducted annually.
1. Production data restore tests must be performed at least annually to validate recoverability.
