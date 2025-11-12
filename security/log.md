---
title: Log Retention Policy
satisfies:
  SOC 2:
    - CC7.2   # Logs and monitors system activity to detect security events
    - CC7.3   # Detects and analyzes deviations from expected operations
    - CC7.4   # Monitors for unauthorized or malicious use of systems
tags:
    - security
---

## Purpose and Scope

This policy defines the requirements for generating, storing, aggregating, and reviewing audit logs across {{company_name}}’s production environment to support security monitoring and threat detection. It applies to all production systems, as well as all employees, contractors, and partners responsible for administering or maintaining those systems.

## Background

Audit logs are essential for maintaining visibility into the confidentiality, integrity, and availability of critical systems. Logs from infrastructure, applications, and supporting services provide valuable information for monitoring, troubleshooting, incident response, and forensic investigations. This policy establishes expectations for consistent log management, aggregation, and review across {{company_name}}’s environment.

## Policy

### Logging Requirements

1. All production systems must record and retain audit logs that include:
   1. Activities performed on the system
   1. The user or entity performing the activity
   1. The file, application, or object affected
   1. The time of the activity
   1. The tool used to perform the activity
   1. The outcome (success or failure)

1. The following events must be logged where technically feasible:
   1. Creation, reading, updating, or deletion of information (including authentication data)
   1. Accepted or initiated network connections
   1. User authentication and authorization activity
   1. Granting, modification, or revocation of access rights
   1. System, network, or service configuration changes (including patches, updates, and software installations)
   1. Startup, shutdown, or restart of applications or services
   1. Application failures, abnormal terminations, or hardware/service faults
   1. Detection of suspicious or malicious activity (e.g., antivirus, antimalware, IDS/IPS)

### Centralized Logging

1. Unless technically impractical, all logs must be aggregated into a centralized log management system.
1. Centralized logging systems must support:
   1. Timely log ingestion
   1. Automated event or anomaly tagging and alerting
   1. Manual search and review capabilities

### Log Review

1. User, administrator, and operator activity logs must be reviewed at least **monthly**.
1. Logs related to Personally Identifiable Information (PII) must be reviewed at least **monthly** for anomalies.

### Cloud Environments

1. Logs must be retained for cloud environments, including:
   1. Access and usage events
   1. Resource allocation and utilization
   1. Changes to PII
   1. All administrator and operator activities

### Time Synchronization

1. All systems must synchronize clocks using NTP or an equivalent time service.
1. All systems must use the same primary trusted time source when possible.
