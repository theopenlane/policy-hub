---
title: Business Continuity Policy
satisfies:
  SOC 2:
    - A1.3
tags:
    - availability
---

## Purpose and Scope

1. Ensure the organization establishes objectives, plans, and procedures such that a major disruption to key business activities is minimized.
1. Applies to all infrastructure and data within the information security program.
1. Applies to all management, employees, and suppliers involved in business continuity decisions and processes.

## Background

1. Preserves critical business operations and essential functions used to deliver products and services.
1. Defines the structure, authority, and requirements for maintaining business resilience.
1. Establishes criteria for managing through disruptive events and resuming normal operations.

1. *Definitions:**
1. *Business Impact Analysis (BIA):* Determines the impact of losing key resources, escalation over time, minimum recovery resources, and process prioritization.
1. *Disaster Recovery Plan (DRP):* Procedures, people, and resources needed to return to normal operations within defined time and cost.
1. *Recovery Time Objective (RTO):* Maximum allowed downtime before recovery.
1. *Recovery Point Objective (RPO):* Maximum acceptable data loss (in time) in case of disruption.

## Policy

### Business Risk Assessment and Business Impact Analysis
1. Each manager must perform a business risk assessment and BIA for all key systems under their responsibility.
1. The assessment must identify critical systems, data repositories, applicable risks, and recovery priorities.
1. Each area must document a Disaster Recovery Plan (DRP) that includes:
  1. Key business processes
  1. Applicable risks to availability
  1. Prioritization of recovery activities
  1. Defined RTOs and RPOs

### Disaster Recovery Plan
1. Every critical system must have a documented DRP addressing both short-term and long-term outages.
1. Each DRP must explain the impact of system unavailability and the processes to continue operations during outages.
1. Plans should consider offsite computing alternatives (cold, warm, or hot sites).
1. DRPs must be reviewed against organizational strategy, policies, and legal/regulatory requirements.
1. Each DRP must include:
  1. Emergency mode operations plan
  1. Recovery plan for restoring on-site operations
  1. Periodic testing, review, and revision schedule

### Data Backup and Restoration
1. Each system owner must implement a data backup and restoration plan.
1. Plans must identify:
  1. Data custodian(s)
  1. Backup schedule and storage location
  1. Security controls for access to backup media
  1. Authorized personnel for removing/transferring media
  1. Restoration procedures to recover from backup media
  1. Testing plan and frequency to confirm effectiveness
  1. Methods for restoring encrypted backup media

# Appendix A: RTO and RPO Matrix

This table defines the **Recovery Time Objective (RTO)** and **Recovery Point Objective (RPO)** for key business systems.
- **RTO:** Maximum time allowed to restore system after a disruption.
- **RPO:** Maximum data loss measured in time.

| System / Service             | Owner              | Criticality | RTO (Max Downtime) | RPO (Max Data Loss) | Notes / Dependencies                  |
|-------------------------------|-------------------|-------------|--------------------|---------------------|---------------------------------------|
| Production Database           | Engineering       | High        | 4 hours            | 15 minutes          | Requires real-time replication         |
| Customer Portal / SaaS Frontend | Product & Eng   | High        | 8 hours            | 1 hour              | Hosted on cloud provider, multi-zone   |
| Email & Communication (Gmail/Slack) | IT / Ops   | Medium      | 24 hours           | 4 hours             | Vendor-managed SaaS, fallback via mobile|
| Source Code Repositories (GitHub/GitLab) | Engineering | Medium | 12 hours           | 4 hours             | Access via cloud; export backups weekly |
| Internal File Storage / Docs  | IT                | Low         | 48 hours           | 24 hours            | Google Drive/Confluence backups        |
| HR / Payroll System           | HR + Finance      | Medium      | 72 hours           | 24 hours            | Vendor SaaS with built-in backups      |

---

# Appendix B: DRP Testing and Review Schedule

| Test Type           | Frequency       | Responsible Team | Notes |
|---------------------|-----------------|------------------|-------|
| Backup restoration  | Quarterly       | IT               | Validate recovery from encrypted backups |
| DRP tabletop exercise | Semi-annually | IT + Management  | Simulated outage walk-through |
| Full failover drill | Annually        | Engineering/IT   | Include alternate site activation |
| Risk/BIA update     | Annually        | All Departments  | Update RTO/RPO and dependencies |