---
title: Third-Party Management Policy
satisfies:
  SOC 2:
    - CC1.2
    - CC2.2
    - CC3.2
    - CC3.3
    - CC3.4
    - CC5.2
    - CC7.2
    - CC9.2
tags:
    - security
---

## Third-Party Management Policy

**Policy Owner:** {{policy_owner}}

**Effective Date:** {{effective_date}}

## Purpose

To ensure protection of the organization's data and assets that are shared with, accessible to, or managed by suppliers, including external parties or third-party organizations such as service providers, vendors, and customers, and to maintain an agreed level of information security and service delivery in line with supplier agreements.

This document outlines a baseline of security controls that {{company_name}} expects partners and other third-party companies to meet when interacting with {{company_name}} Confidential data.

## Scope

All data and information systems owned or used by {{company_name}} that are business critical and/or process, store, or transmit Confidential data. This policy applies to all employees of {{company_name}} and to all external parties, including but not limited to {{company_name}} consultants, contractors, business partners, vendors, suppliers, partners, outsourced service providers, and other third-party entities with access to {{company_name}} data, systems, networks, or system resources.

## Policy

Information security requirements for mitigating the risks associated with supplier's access to the organization's assets shall be agreed with the supplier and documented.

For all service providers who may access {{company_name}} Confidential data, systems, or networks, proper due diligence shall be performed prior to provisioning access or engaging in processing activities. Information shall be maintained regarding which regulatory or certification requirements are managed by or impacted by each service provider, and which are managed by {{company_name}} as required. Applicable regulatory or certification requirements may include ISO 27001, SOC 2, PCI DSS, CCPA, GDPR or other frameworks, compliance standards, or regulations.

## Information Security in Third-Party Relationships

### Addressing Security in Agreements

Relevant information security requirements shall be established and agreed upon with each supplier that may access, process, store, transmit, or impact the security of Confidential data and systems, or provide physical or virtual IT infrastructure components for {{company_name}}.

For all service providers who may access {{company_name}} production systems, or who may impact the security of the {{company_name}} production environment, written agreements shall be maintained that include the service provider's acknowledgment of their responsibilities for the confidentiality of company and customer data, and any commitments regarding the integrity, availability, and/or privacy controls that they manage in order to meet the standards and requirements that {{company_name}} has established in accordance with {{company_name}}’s information security program or any relevant framework.

### Technology Supply Chain

{{company_name}} will consider and assess risk associated with suppliers and the technology supply chain. Where warranted, agreements with suppliers shall include requirements to address the relevant information security risks associated with information and communications technology services and the product supply chain.

## Third-Party Service Delivery Management

### Monitoring & Review of Third-Party Services

{{company_name}} shall regularly monitor, review, and audit supplier service delivery. Supplier security and service delivery performance shall be reviewed at least annually.

### Management of Changes to Third-Party Services

Changes to the provision of services by suppliers, including changes to agreements, services, technology, policies, procedures, or controls, shall be managed, taking account of the criticality of the business information, systems, and processes involved. {{company_name}} shall assess the risk of any material changes made by suppliers and make appropriate modifications to agreements and services accordingly.

## Third-Party Risk Management

{{company_name}} will ensure that potential risks posed by sharing Confidential data or providing access to company systems are identified, documented and addressed according to this policy. Risk management plays an integral part in the governance and management of the organization at a strategic and operational level. The purpose of a partner and third-party security policy is to ensure that partnerships and services achieve their business plan aims and objectives, and are consistent with {{company_name}}’s requirements for information security.

{{company_name}} shall not share or transmit Confidential data to a third-party without first performing a third-party risk assessment and fully executing a written contract, statement of work or service agreement which describes expected service levels and any specific information security requirements.

## Information security for use of cloud services

This section outlines the fundamental parameters for managing and mitigating risks related to cloud service usage.

Responsibilities and Risk Management:

* Roles and responsibilities related to the use and management of cloud services can be found in the *Roles and Responsibilities Policy*.
* Information security risks associated with cloud services use shall be managed in accordance with this policy and the *Risk Management Policy*.

Security Requirements and Control:

* The company shall be responsible for all customer controls as defined in cloud service providers’ responsibility matrices.

Service Selection and Usage Scope:

* Reviews of cloud service agreements for inherently high risk providers shall be performed annually to ensure they align with company requirements.

Incident Management:

* Information security incidents related to cloud services managed in accordance with the Incident Response Plan.

Service Review and Exit Strategy:

* Risks related to exit and vendor lock-in should be evaluated prior to the acquisition as part of the vendor security assessment.

Provider and Customer Agreement:

* Agreements with cloud service providers will specify protections for {{company_name}}’s data and service availability, even though they might be predefined and non-negotiable.
* Where possible, {{company_name}} will seek advance notification from providers concerning substantive changes in service delivery, including changes in technical infrastructure, data storage location, or usage of sub-contractors.

Ongoing Management and Assurance:

* Information regarding how to obtain and utilize information security capabilities provided by the cloud service provider should be assessed as part of the vendor review at time of acquisition.

## Third-Party Security Standards

All third-parties must maintain reasonable organizational and technical controls as assessed by {{company_name}}.

Assessment of third-parties which receive, process, or store Confidential data or access {{company_name}}’s resources shall consider the following controls as applicable based on the service provided and the sensitivity of data stored, processed or exchanged.

### Information Security Policy

Third-parties maintain information security policies supported by their executive management, which are regularly reviewed.

### Risk Assessment & Treatment

Third-parties maintain programs that assess, evaluate, and manage information and technology risks.

### Operations Security

Third-parties implement commercially reasonable practices and procedures designed, as appropriate, to maintain operations security. Protections may include:

* Technical testing
* Protection against malicious software
* Network protection and management
* Technical vulnerability management
* Logging and monitoring
* Incident response
* Business continuity planning

### Access Control

Third-parties maintain a technical access control program.

### Secure System Development

Third-parties maintain a secure development program consistent with industry software and systems development best practices including risk assessment, formal change management, code standards, code review and testing.

### Physical & Environmental Security

If third-parties are storing or processing confidential data, their physical and environmental security controls should meet the requirements of the {{company_name}} Physical Security Policy[^2].

### Human Resources

Third-parties maintain human resource policies and processes which include criminal background checks for any employees or contractors who access {{company_name}} confidential information.

### Compliance & Legal

{{company_name}} shall consider all applicable regulations and laws when evaluating suppliers and third parties who will access, store, process or transmit {{company_name}} confidential data.  Third-party assessments should consider the following criteria:

* Protection of customer data, organizational records, and records retention and disposition
* Privacy of Personally Identifiable Information (PII)

## Exceptions

Requests for an exception to this Policy must be submitted to the &lt;approver of requests for exceptions to this policy, e.g., CFO&gt;  for approval.

## Violations & Enforcement

Any known violations of this policy should be reported to the &lt;person responsible for receiving policy violation reports, e.g., CFO&gt; . Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

[^1]:  All fields in this document marked by angled brackets &lt; &gt;  and highlighted must be filled in.

[^2]:  This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s physical and environmental security controls here.
