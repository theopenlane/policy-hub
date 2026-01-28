---
title: Access Control Policy
satisfies:
  SOC 2:
    - CC5.2
    - CC6.1
    - CC6.2
    - CC6.3
    - CC6.4
    - CC7.2
tags:
    - security
---

## Purpose

To limit access to information and information processing systems, networks, and facilities to authorized parties in accordance with business objectives.

## Scope

All {{company_name}} information systems that process, store, or transmit confidential data as defined in the {{company_name}} Data Management Policy<sup>2</ sup>. This policy applies to all employees of {{company_name}} and to all external parties with access to {{company_name}} networks and system resources.

## Policy

Access to information computing resources is limited to personnel with a business requirement for such access. Access rights shall be granted or revoked in accordance with this Access Control Policy.

## Business Requirements of Access Control

### Access Control Policy

{{company_name}} shall determine the type and level of access granted to individual users based on the “principle of least privilege.” This principle states that users are only granted the level of access absolutely required to perform their job functions, and is dictated by {{company_name}}’s business and security requirements. Permissions and access rights not expressly granted shall be, by default, prohibited.

{{company_name}}’s primary method of assigning and maintaining consistent access controls and access rights shall be through the implementation of Role-Based Access Control (RBAC). Wherever feasible, rights and restrictions shall be allocated to groups. Individual user accounts may be granted additional permissions as needed with approval from the system owner or authorized party.

 All privileged access to production infrastructure shall use Multi-Factor Authentication (MFA)<sup>3</ sup>.

### Access to Networks and Network Services

The following security standards shall govern access to {{company_name}} networks and network services:

* Technical access to {{company_name}} networks must be formally documented including the standard role or approver, grantor, and date
* Only authorized {{company_name}} employees and third-parties working off a signed contract or statement of work, with a business need, shall be granted access to the {{company_name}} production networks and resources
* {{company_name}} guests may be granted access to guest networks after registering with office staff without a documented request
* Remote connections to production systems and networks must be encrypted

## Customer Access Management<sup>4</ sup>

When configuring cross-account access using AWS IAM roles, you must use a value you generate for the external ID, instead of one provided by the customer, to ensure the integrity of the cross account role configuration. A partner-generated external ID ensures that malicious parties cannot impersonate a customer's configuration and enforces uniqueness and format consistency across all customers.

The external IDs used must be unique across all customers. Re-using external IDs for different customers does not solve the confused deputy problem and runs the risk of customer A being able to view data of customer B by using the role ARN of customer B along with the external ID of customer B.

Customers must not be able to set or influence external IDs. When the external ID is editable, it is possible for one customer to impersonate the configuration of another.

## User Access Management

{{company_name}} requires that all personnel have a unique user identifier for system access, and that user credentials and passwords are not shared between multiple personnel. Users with multiple levels of access (e.g. administrators) should be given separate accounts for normal system use and for administrative functions wherever feasible. Root, service, and administrator accounts may use a password management system to share passwords for business continuity purposes only. Administrators shall only use shared administrative accounts as needed. If a password is compromised or suspected of compromise the incident should be escalated to &lt;IR Team&gt;  immediately and the password must be changed.

### User Registration and Deregistration

Only authorized administrators shall be permitted to create new user IDs, and may only do so upon receipt of a documented request from authorized parties. User provisioning requests must include approval from data owners or {{company_name}} management authorized to grant system access. Prior to account creation, administrators should verify that the account does not violate any {{company_name}} security or system access control policies such as segregation of duties, fraud prevention measures, or access rights restrictions.

User IDs shall be promptly disabled or removed when users leave the organization or contract work ends in accordance with SLAs. User IDs shall not be re-used.

### User Access Provisioning

* New employees and/or contractors are not to be granted access to any {{company_name}} production systems until after they have completed all HR on-boarding tasks, which may include but is not limited to signed employment agreement, intellectual property agreement, and acknowledgement of {{company_name}}’s information security policy
* Access should be restricted to only what is necessary to perform job duties
* No access may be granted earlier than official employee start date
* Access requests and rights modifications shall be documented in an access request ticket or email. No permissions shall be granted without approval from the system or data owner or management
* Records of all permission and privilege changes shall be maintained for no less than one year

### Management of Privileged Access



{{company_name}} shall ensure that the allocation and use of privileged access rights are restricted and managed judiciously. The objective is to ensure that only authorized users, software components, and services are granted privileged access rights. {{company_name}} will ensure that access and privileges conform to the following standard:

* Identify and Validate Users: Identify users who require privileged access for each system and process.
* Allocate Privileged Rights: Provision access rights basing allocations on specific needs and competencies, and adhering strictly to the access control policy.
* Maintain Authorization Protocols: maintain records of all privileged access allocations.
* Enforce Strong Authentication: Require MFA for all privileged access.
* Prevent Generic Admin ID Usage: prevent the usage of generic administrative user IDs
* [Optional depending on Context] Adopt Time-Bound Access Protocols: Grant privileged access only for the necessary duration required to accomplish specific tasks and revoke once the task is completed.
* Ensure Logging and Auditing: Log all privileged logins and activity
* [Optional depending on Context] Uphold Distinct and Separate Identities: Preserve distinct identities for privileged access rights and ensure such identities are neither shared among multiple users nor used for routine, non-administrative tasks.

### User Access Reviews

Administrators shall perform access rights reviews of user, administrator, and service accounts on a {{frequency}} basis to verify that user access is limited to systems that are required for their job function. Access reviews shall be documented.

Access reviews may include group membership as well as evaluations of any specific or exception-based permission. Access rights shall also be reviewed as part of any job role change, including promotion, demotion, or transfer within the company.

### Removal & Adjustment of Access Rights

The access rights of all users shall be promptly removed upon termination of their employment or contract, or when rights are no longer needed due to a change in job function or role. The maximum allowable time period for access termination is {{time}} business hours.

### Access Provisioning, Deprovisioning, and Change Procedure

The Access Management Procedure for {{company_name}} systems can be found in Appendix A to this policy.

### Segregation of Duties

Conflicting duties and areas of responsibility shall be segregated to reduce opportunities for unauthorized or unintentional modification or misuse of {{company_name}} assets. When provisioning access, care should be taken that no single person can access, modify or use assets without authorization or detection. The initiation of an event should be separated from its authorization. The possibility of collusion should be considered when determining access levels for individuals and groups.

## User Responsibility for the Management of Secret Authentication Information

Control and management of individual user passwords is the responsibility of all {{company_name}} personnel and third-party users. Users shall protect secret authentication information in accordance with the Information Security Policy.

## Password Policy<sup>5</ sup>

Where feasible, passwords for confidential systems shall be configured for at least &lt;minimum password requirements&gt; :

* &lt;e.g., eight (8) or more characters, one upper case, one number
* &lt;Systems shall be configured to remember and prohibit reuse of passwords for last &lt;16&gt; passwords used&gt;
* &lt;Passwords shall be set to lock out after &lt;6&gt;  failed attempts&gt;
* &lt;Passwords shall expire after &lt;90 days&gt; &gt;
* &lt;Initial passwords must be set to a unique value and changed after first log in&gt;
* &lt;For manual password resets, a user’s identity must be verified prior to changing passwords&gt;
* &lt;Do not limit the permitted characters that can be used&gt;
* &lt;Do not limit the length of the password to anything below 64 characters&gt;
* &lt;Do not use secret questions (place of birth, etc) as a sole password reset requirement&gt;
* &lt;Require email verification of a password change request&gt;
* &lt;Require the current password in addition to the new password during password change&gt;
* &lt;Verify newly created passwords against common passwords lists or leaked passwords databases&gt;
* &lt;Check existing user passwords for compromise regularly&gt;
* &lt;Store passwords in a hashed and salted format using a memory-hard or CPU-hard one-way hash function&gt;
* &lt;Enforce appropriate account lockout and brute-force protection on account access&gt;

## System and Application Access

### Information Access Restriction

Applications must restrict access to program functions and information to authorized users and support personnel in accordance with the defined access control policy. The level and type of restrictions applied by each application should be based on the individual application requirements, as identified by the data owner. The application-specific access control policy must also conform to {{company_name}} policies regarding access controls and data management.

Prior to implementation, evaluation criteria are to be applied to application software to determine the necessary access controls and data policies. Assessment criteria include, but are not limited to:

* Sensitivity and classification of data.
* Risk to the organization of unauthorized access or disclosure of data
* The ability to, and granularity of, control(s) on user access rights to the application and data stored within the application
* Restrictions on data outputs, including filtering sensitive information, controlling output, and restricting information access to authorized personnel
* Controls over access rights between the evaluated application and other applications and systems
* Programmatic restrictions on user access to application functions and privileged instructions
* Logging and auditing functionality for system functions and information access
* Data retention and aging features

All unnecessary default accounts must be removed or disabled before making a system available on the network. Specifically, vendor default passwords and credentials must be changed on all {{company_name}} systems, devices, and infrastructure prior to deployment. This applies to ALL default passwords, including but not limited to those used by operating systems, software that provides security services, application and system accounts, and Simple Network Management Protocol (SNMP) community strings where feasible.

### Secure Log-on Procedures

Secure log-on controls shall be designed and selected in accordance with the sensitivity of data and the risk of unauthorized access based on the totality of the security and access control architecture.

### Password Management System

Systems for managing passwords should be interactive and assist {{company_name}} personnel in maintaining password standards by enforcing password strength criteria including minimum length, and password complexity where feasible.

All storage and transmission of passwords is to be protected using appropriate cryptographic protections, either through hashing or encryption.

### Use of Privileged Utility Programs

Use of utility programs, system files, or other software that might be capable of overriding system and application controls or altering system configurations must be restricted to the minimum personnel required. Systems are to maintain logs of all use of system utilities or alteration of system configurations. Extraneous system utilities or other privileged programs are to be removed or disabled as part of the system build and configuration process.

Management approval is required prior to the installation or use of any ad hoc or third-party system utilities.

### Access to Program Source Code

Access to program source code and associated items, including designs, specifications, verification plans, and validation plans shall be strictly controlled in order to prevent the introduction of unauthorized functionality into software, avoid unintentional changes, and protect {{company_name}} intellectual property.

All access to source code shall be based on business need and must be logged for review and audit.

## Exceptions

Requests for an exception to this Policy must be submitted to the IT Manager for approval.

## Violations & Enforcement

Any known violations of this policy should be reported to the IT Manager. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

## APPENDIX A – Access Management Procedure<sup>6</ sup>

At the completion of the onboarding process, HR will send an email that will generate a series of service tickets for access.

IT will provision access for all company-wide systems as well as engineering systems for the Members of Technical Staff (MTS) group.

Additional access, beyond standard pre-approved access, must be requested and approved by a manager or system owner.

## APPENDIX B – Access Matrix<sup>7</ sup>

| Role | Email | Google Workspace | Expense Tool | CRM | App | Infrastructure | Version Control | Build System | Vuln Scanner |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Employee | x | x | x |  | x |  |  |  |  |
| Engineer 1 | x | x | x |  | x | x | x | x |  |
| Engineer Sprvs | x | x | x |  | x | x | x | x | x |
| Sales | x | x | x | x | x |  |  |  |  |
| Sales Mgr | x | x | x | x |  |  |  |  |  |

---

<sup>1</ sup>All fields in this document marked by angled brackets &lt; &gt;  and highlighted must be filled in.

<sup>2</ sup>Reference to another Openlane template policy.

<sup>3</ sup>Remove or change this if not accurate

<sup>4</ sup>Delete if not relevant or not using AWS.

<sup>5</ sup>Tailor for your environment. Consider some security standards have prescriptive requirements.

<sup>6</ sup>If your company has a defined access management procedure, describe it here. If your company does not have such a procedure, you can delete this appendix in its entirety. The procedure described is provided as an example.

<sup>7</ sup>Example Access matrix v2.0. Predefined access based on role would not require tickets and approvals.
