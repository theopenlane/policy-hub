---
title: Data Management Policy
satisfies:
  SOC 2:
    - CC1.1
    - CC1.2
    - CC1.4
    - CC2.2
    - CC6.1
    - CC6.2
    - CC6.6
tags:
    - security
---

## Purpose

To ensure that information is classified, protected, retained and securely disposed of in accordance with its importance to the organization.

## Scope

All {{company_name}} data, information and information systems.

## Policy

{{company_name}} classifies data and information systems in accordance with legal requirements, sensitivity, and business criticality in order to ensure that information is given the appropriate level of protection. Data owners are responsible for identifying any additional requirements for specific data or exceptions to standard handling requirements.

Information systems and applications shall be classified according to the highest classification of data that they store or process.

## Data Classification<sup>2</ sup>

To help {{company_name}} and its employees easily understand requirements associated with different kinds of information, the company has created three classes of data.

### Confidential

Highly sensitive data requiring the highest levels of protection; access is restricted to specific employees or departments, and these records can only be passed to others with approval from the data owner, or a company executive. Example include<sup>3</ sup>:

* Customer Data
* Personally identifiable information (PII)
* Company financial and banking data
* Salary, compensation and payroll information
* Strategic plans
* Incident reports
* Risk assessment reports
* Technical vulnerability reports
* Authentication credentials
* Secrets and private keys
* Source code
* Litigation data

### Restricted

{{company_name}} proprietary information requiring thorough protection; access is restricted to employees with a “need-to-know” based on business requirements. This data can only be distributed outside the company with approval. This is default for all company information unless stated otherwise. Examples include<sup>4</ sup>:

* Internal policies
* Legal documents
* Meeting minutes and internal presentations
* Contracts
* Internal reports
* Slack messages
* Email

### Public

Documents intended for public consumption which can be freely distributed outside {{company_name}}. Examples include<sup>5</ sup>:

* Marketing materials
* Product descriptions
* Release notes
* External facing policies

## Labeling

Confidential data should be labeled “confidential” whenever paper copies are produced for distribution.

## Data Handling<sup>6</ sup>

### Confidential Data Handling

Confidential data is subject to the following protection and handling requirements<sup>7</ sup>:

* Access for non pre-approved roles requires documented approval from the data owner
* Access is restricted to specific employees, roles and/or departments
* Confidential systems shall not allow unauthenticated or anonymous access
* Confidential Customer Data shall not be used or stored in non-production systems/environments
* Confidential data shall be encrypted at rest and in transit over public networks in accordance with the Cryptography Policy
* Mobile device hard drives containing confidential data, including laptops, shall be encrypted
* Mobile devices storing or accessing confidential data shall be protected by a log-on password (or equivalent, such as biometric) or passcode and shall be configured to lock the screen after five (5) minutes of non-use
* Backups shall be encrypted
* Confidential data shall not be stored on personal phones or devices or removable media including USB drives, CD’s, or DVD’s
* Paper records shall be labeled “confidential” and securely stored and disposed of in a secure, approved manner in accordance with data handling and destruction policies and procedures
* Hard copy paper records shall only be created based on a business need and shall be avoided whenever possible<sup>8</ sup>
* Hard drives and mobile devices used to store confidential information must be securely wiped prior to disposal or physically destroyed
* Transfer of confidential data to people or entities outside the company shall only be done in accordance with a legal contract or arrangement, and the explicit written permission of management or the data owner

### Restricted Data Handling

Restricted data is subject to the following protection and handling requirements<sup>9</ sup>:

* Access is restricted to users with a need-to-know based on business requirements
* Restricted systems shall not allow unauthenticated or anonymous access
* Transfer of restricted data to people or entities outside the company or authorized users shall require management approval and shall only be done in accordance with a legal contract or arrangement, or the permission of the data owner
* Paper records shall be securely stored and disposed of in a secure, approved manner in accordance with data handling and destruction policies and procedures<sup>10</ sup>
* Hard drives and mobile devices used to store restricted information must be securely wiped prior to disposal or physically destroyed

### Public Data Handling

No special protection or handling controls are required for public data. Public data may be freely distributed.

## Data Retention

{{company_name}} shall retain data as long as the company has a need for its use, or to meet regulatory or contractual requirements. Once data is no longer needed, it shall be securely disposed of or archived. Data owners, in consultation with legal counsel, may determine retention periods for their data.

Personally identifiable information (PII) shall be deleted or de-identified as soon as it no longer has a business use<sup>11</ sup>.

Retention periods shall be documented in the Data Retention Matrix in Appendix B <sup>12</sup> to this policy.

## Data & Device Disposal

Data classified as restricted or confidential shall be securely deleted when no longer needed. {{company_name}} shall assess the data and disposal practices of third-party vendors in accordance with the Third-Party Management Policy. Only third-parties who meet {{company_name}} requirements for secure data disposal shall be used for storage and processing of restricted or confidential data<sup>13</ sup>.

{{company_name}} shall ensure that all restricted and confidential data is securely deleted from company devices prior to, or at the time of, disposal.

Confidential and Restricted hard copy materials shall be shredded or otherwise disposed of using a secure method<sup>14</ sup><sup>15</ sup>.

Personally identifiable information (PII)<sup>16</ sup> shall be collected, used and retained only for as long as the company has a legitimate business purpose. PII shall be securely deleted and disposed of following contract termination in accordance with company policy, contractual commitments and all relevant laws and regulations. PII shall also be deleted in response to a verified request from a consumer or data subject, where the company does not have a legitimate business interest or other legal obligation to retain the data.

## Annual Data Review

Management shall review data retention requirements during the annual review of this policy. Data shall be disposed of in accordance with this policy.

## Legal Requirements

Under certain circumstances, {{company_name}} may become subject to legal proceedings requiring retention of data associated with legal holds, lawsuits, or other matters as stipulated by {{company_name}} legal counsel. Such records and information are exempt from any other requirements specified within this Data Management Policy and are to be retained in accordance with requirements identified by the Legal department. All such holds and special retention requirements are subject to annual review with {{company_name}}’s legal counsel to evaluate continuing requirements and scope.

## Policy Compliance

{{company_name}} will measure and verify compliance to this policy through various methods, including but not limited to, business tool reports, and both internal and external audits.

## Exceptions

Requests for an exception to this policy must be submitted to the &lt;approver of requests for an exception to this policy, e.g., CFO&gt;  for approval.

## Violations & Enforcement

Any known violations of this policy should be reported to the &lt;who should receive reports of violations to this policy, e.g., CFO&gt; . Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

## APPENDIX A – Internal Retention and Disposal Procedure<sup>17</ sup>

{{company_name}}’s &lt;responsible party, e.g., Engineering Team&gt;  is responsible for setting and enforcing the data retention and disposal procedures for {{company_name}} managed accounts and devices.

**Customer Accounts:**

1. Customer accounts and data shall be deleted within &lt;sixty (60)&gt;  days of contract termination through manual data deletion processes.

**Devices:**

1. Employee devices will be collected promptly upon an employee’s termination. Remote employees will be sent a shipping label and the return of their device shall be monitored.
2. Collected devices will be cleared to be re-provisioned—or removed from inventory;, {{company_name}} will securely erase the device when reprovisioning.
3. Device images may be retained at the discretion of management for business purposes

**Destroying devices or electronic media**

In cases where a device is damaged in a way that {{company_name}} cannot access the Recovery Partition to erase the drive, {{company_name}} may optionally decide to use an E-Waste service that includes data destruction with a certificate. {{company_name}} will keep certificates of destruction on record for one year. Physical destruction can be optional if it is verified that the device is encrypted with Full Disk Encryption, which would negate the risk of data recovery.

Management will review this procedure at least &lt;frequency of procedure review, e.g., annually&gt; .

## APPENDIX B – Data Retention Matrix<sup>18</ sup>

| System or Application | Data Description | Retention Period |
| :---- | :---- | :---- |
| {{company_name}} SaaS Products (AWS) | Customer Data | Up to 60 days after contract termination |
| {{company_name}} AutoSupport | Customer instance and metadata, debugging data | Indefinite |
| {{company_name}} Customer Support Tickets (Salesforce) | Support Tickets and Cases | Indefinite |
| {{company_name}} Customer Support Phone Conversations (TalkDesk) | Support Phone Conversations | Indefinite |
| {{company_name}} Security Event Data (Splunk) | Security and system event and log data, network data flow logs | On-Premise - Indefinite AWS Instance - 1 year |
| {{company_name}} Vulnerability Scan Data (Qualys) | Vulnerability scan results and detection data | 6 months host (asset) data is retained until removed and purged from Qualys |
| {{company_name}} Customer Sales (Salesforce) | Opportunity and Sales Data | Indefinite |
| {{company_name}} QA and Testing Data (TestRail) | QA, testing scenarios and results data | Indefinite |
| Security Policies | Security Policies | 1 year after archive |
| Temporary Files<sup>19</ sup> | AWS /tmp ephemeral storage | automatically when process finishes |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

***Master Version:*** &lt;link&gt;

__________

<sup>1</ sup> All fields in this document marked by angled brackets &lt; &gt;  and highlighted must be filled in.

<sup>2</ sup> Describe your company’s data classification labels here. Customize the labels to meet your company’s needs.

<sup>3</ sup> Update this list of examples to fit your organization

<sup>4</ sup> Update this list of examples to fit your organization

<sup>5</ sup> Update this list of examples to fit your organization

<sup>6</ sup> Update the data classification labels in this section to describe the systems that your company uses

<sup>7</ sup> Update this list of confidential data handling requirements to fit your organization

<sup>9</ sup> Update this list of restricted data handling requirements to fit your organization

<sup>12</ sup> This is a reference to an appendix in this document. If this is documented elsewhere, include a reference or a link to the document.

<sup>13</ sup> If your company does not use third-parties to process sensitive data, you can delete these sentences.

<sup>14</ sup> This is a reference to another Openlane policy. If you are not planning on using the Third-Party Management Policy, describe your data disposal practices of third-party vendors here.

<sup>17</ sup> In this appendix, describe your company’s internal data retention and disposal procedures. The content here is provided as an example.

<sup>18</ sup> You can remove this table from the document as long as you include a link or a reference to your data retention matrix. It is recommended that you structure your matrix like this table.
