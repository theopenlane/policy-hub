---
title: Secure Development Policy
satisfies:
  SOC 2:
    - CC6.1
    - CC6.2
    - CC6.3
    - CC7.2
    - CC7.3
    - CC8.1
tags:
    - security
---

## Purpose

To ensure that information security is designed and implemented within the development lifecycle for applications and information systems.

## Scope

All {{company_name}} applications and information systems that are business critical and/or process, store, or transmit Confidential data. This policy applies to all internal and external engineers and developers of {{company_name}} software and infrastructure.

## Policy

This policy describes the rules for the acquisition and development of software and systems that shall be applied to developments within the {{company_name}} organization.

## System Change Control Procedures <sup>2</sup>

Changes to systems within the development lifecycle shall be controlled by the use of formal change control procedures. Change control procedures and requirements are described in the {{company_name}} Operations Security Policy.

Significant code changes must be reviewed and approved by &lt;who can approve code changes, e.g., a developer or manager within the Review Board&gt;  before being merged into any production branch in accordance with the &lt;name of process, e.g., Check In Process&gt;  found here: &lt;link to process outline in company wiki&gt;

Change control procedures shall ensure that development, testing and deployment of changes shall not be performed by a single individual without approval and oversight.

## Software Version Control <sup>3</sup>

All {{company_name}} software is version controlled and synced between contributors (developers). Access to the central repository is restricted based on an employee’s role. All code is written, tested, and saved in a local repository before being synced to the origin repository.

## Technical Review of Applications after Operating Platform Changes

When operating platforms are changed, business critical applications shall be reviewed and tested to ensure that there is no adverse impact on organizational operations or security.

## Restrictions on Changes to Software Packages

Modifications to third-party business application packages shall be discouraged, limited to necessary changes and all changes shall be strictly controlled.

## Secure System Engineering Principles

Principles for engineering secure systems shall be established, documented, maintained and applied to any information system implementation efforts.

At a minimum, the following secure-by-design and privacy-by-design principles shall be applied:

Secure-by-design principles:

1. Minimize attack surface area
1. Establish secure defaults
1. The principle of Least privilege
1. The principle of defense in depth
1. Fail securely
1. Don’t trust services
1. Separation of duties
1. Avoid security by obscurity
1. Keep security simple
1. Fix security issues correctly

Privacy-by-design principles:

1. Proactive not Reactive; Preventative not Remedial
1. Privacy as the Default Setting
1. Privacy Embedded into Design
1. Full Functionality – Positive-Sum, not Zero-Sum
1. End-to-End Security – Full Lifecycle Protection
1. Visibility and Transparency – Keep it Open
1. Respect for User Privacy – Keep it User-Centric

Engineering documentation and technical references can be found in the &lt;name of page with documents, e.g., Development Process Confluence Page&gt;  here: &lt;link&gt;

Software developers are expected to adhere to {{company_name}}’s coding standards throughout the development cycle, including standards for quality, commenting, and security.

## Secure Development Environment <sup>4</sup>

{{company_name}} shall establish and appropriately protect environments for system development and integration efforts that cover the entire system development life cycle. The following environments shall be logically or physically segregated:

* Production
* Test / Staging
* Development

## Outsourced Development <sup>5</sup>

{{company_name}} shall supervise and monitor the activity of outsourced system development. Outsourced development shall adhere to all {{company_name}} standards and policies.

## System Security Testing

Testing of security functionality shall be performed at defined periods during the development life cycle. No code shall be deployed to {{company_name}} production systems without documented, successful test results and evidence of security remediation activities.

## Application Vulnerability Management

Application code should be scanned prior to deployment. Patches to address application vulnerabilities that materially impact security should be deployed within 90 days of discovery.

## System Acceptance Testing <sup>6</sup>

Acceptance testing programs and related criteria shall be established for new information systems, upgrades and new versions.

Prior to deploying code, a Release Checklist MUST be completed which includes a checklist of all Test Plans which show the completion of all associated tests and remediation of identified issues.

## Protection of Test Data

Test data shall be selected carefully, protected and controlled. Confidential customer data shall be protected in accordance with all contracts and commitments. Customer data shall not be used for testing purposes without the explicit permission of the data owner and the &lt;approver of use of customer data as test data, e.g., VP of Engineering&gt; .

## Acquisition of Third-Party Systems and Software

The acquisition of third-party systems and software shall be done in accordance with the requirements of the {{company_name}} Third-Party Management Policy <sup>7</sup>.

## Developer Training

Software developers shall be provided with secure development training appropriate to their role at least annually. Training content shall be determined by management but shall address the prevention of common web application attacks and vulnerabilities. The following threats and vulnerabilities should be addressed as appropriate:

* prevention of authorization bypass attacks
* prevention of the use of insecure session IDs
* prevention of Injection attacks
* prevention of cross-site scripting attacks
* prevention of cross-site request forgery attacks
* prevention of the use of vulnerable libraries

## Exceptions

Requests for an exception to this Policy must be submitted to the &lt;approver of exceptions to this policy, e.g., VP of Engineering&gt;  for approval.

## Violations & Enforcement

Any known violations of this policy should be reported to the &lt;receiver of reported violations to this policy, e.g., VP of Engineering&gt; . Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

<hr />

<sup>1</sup> All fields in this document marked by angled brackets &lt; &gt;  and highlighted must be filled in.

<sup>2</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s change control procedures and requirements here.

<sup>3</sup> Describe your company’s version control use here

<sup>4</sup> Tailor this section to describe your company’s development environment and SDLC

<sup>5</sup> This section references outsourced development. If you company does not use outsourced development, remove this section.

<sup>6</sup> Describe your company’s acceptance testing process here

<sup>7</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s third-party systems and software acquisition processes
