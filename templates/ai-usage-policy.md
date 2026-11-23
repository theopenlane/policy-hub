---
title: AI Usage Policy
satisfies:
  SOC 2:
    - CC2.2
    - CC3.2
    - CC5.2
    - CC6.1
    - CC6.7
    - CC8.1
    - CC9.2
tags:
    - security
    - ai
---

## Purpose

To define which artificial intelligence (AI) tools {{company_name}} personnel may use, which data may enter those tools, the review standard that applies to AI-generated work, and who owns the risk when an AI tool is wrong.

## Scope

All AI tools and AI systems used to perform work for {{company_name}}, and all {{company_name}} data, source code, and information systems that those tools can read or change. This policy applies to all employees, contractors, and other third parties who use AI tools on behalf of {{company_name}}, on company-managed or personal devices.

## Policy

{{company_name}} permits the use of AI tools that have been approved for the data and the task involved. Personnel shall use only approved tools at approved license tiers, shall keep company data inside the boundaries set by this policy, and remain accountable for all work produced with the assistance of AI.

AI-generated code and other AI output is untrusted input until reviewed, tested, and understood by a human accountable for it.

## AI Tool Categories <sup>2</sup>

{{company_name}} classifies AI tools by how they interact with company data and systems. The category determines which controls apply.

| Category | Description |
| :---- | :---- |
| Consumer AI tools | Personal or free/pro accounts where company data, source code, prompts, outputs, or telemetry may be retained, reviewed, or used for model improvement unless the user configures an opt-out |
| Enterprise AI tools | Centrally procured tools with contractual protections around data retention, training use, access controls, audit logging, and administrative visibility |
| Self-hosted or private AI systems | Models or gateways running under company-controlled infrastructure, with explicit retention, logging, and isolation rules |
| Agentic development tools | Systems that can read repositories, modify files, run commands, create pull requests, or interact with external systems |
| Production AI systems | AI embedded into customer-facing, internal, or automated business workflows, especially those affecting people, money, access, safety, employment, education, healthcare, credit, or legal rights |

## Approved Tools and License Tiers

The &lt;owner of the approved AI tool register, e.g., Security Team&gt;  shall maintain a register of approved AI tools. For each tool, the register records the approved license tier, the tool owner, the renewal date, the vendor’s data retention terms, and whether the vendor may train models on {{company_name}} data. The register is maintained in Appendix A <sup>3</sup> to this policy.

The AI tools listed on the register are approved for use on company systems and codebases only when provisioned through company-managed enterprise accounts.

Free, personal, trial, browser-extension, or consumer tiers are not approved for company code, customer data, confidential information, secrets, regulated data, or production system information unless an exception has been approved in writing by &lt;approvers of AI tool exceptions, e.g., Security and Legal&gt; .

## Data Boundaries <sup>4</sup>

Data classifications are defined in the {{company_name}} Data Management Policy <sup>5</sup>. Employees and contractors must not submit proprietary source code, credentials, API keys, customer data, personal data, PHI, payment data, unreleased product plans, security findings, incident details, contracts, or confidential vendor or customer information to an AI tool unless that tool is explicitly approved for the relevant data classification and use case.

The following table maps each data classification to the approved tool categories.

| Data Classification | Permitted AI Tools |
| :---- | :---- |
| Public | Approved tools, with normal review expectations |
| Restricted | Enterprise AI tools and self-hosted or private AI systems, when the tool is covered by company access controls and retention settings |
| Confidential, including proprietary source code, customer implementation details, architecture diagrams, internal incidents, unreleased product plans, and vendor security artifacts | Limited to approved enterprise AI tools or self-hosted or private AI systems with explicit no-training and retention commitments |

The following data shall not enter external AI tools unless {{company_name}} has a specific, reviewed, documented architecture for that use, approved by the &lt;approver of AI data handling designs, e.g., CISO&gt; :

* Secrets, credentials, and production tokens
* Regulated personal data, including protected health information (PHI) and payment data
* Legal strategy
* Customer data under strict contractual limits

## AI-Generated Code

AI-generated code shall meet the same review, testing, style, security, and architecture standards as code written by a person, in accordance with the {{company_name}} Secure Development Policy <sup>6</sup>.

The following requirements apply to all code that an AI tool suggests, generates, refactors, or tests:

* The person merging code is accountable for the code. A human developer remains accountable for every line merged under their name, regardless of whether AI suggested, generated, refactored, or tested it.
* AI-generated code must be reviewed, tested, and understood before it is merged. “The AI wrote it” is not an acceptable explanation in a post-incident review.
* Generated tests do not prove generated code is correct. Reviewers must evaluate whether tests cover the failure modes that matter, including negative cases.
* A change shall not be merged if the reviewer cannot explain what changed.

### Security-Critical Code

AI may assist with security-critical code only when a qualified human reviewer validates the design and implementation. When AI contributes to the implementation, review by &lt;qualified reviewer, e.g., a senior engineer&gt;  is required before merge. Security-critical code includes:

* Authentication, authorization, and access control
* Cryptography
* Tenant isolation
* Payment processing
* Audit logging
* Data deletion
* Infrastructure permissions
* Deployment workflows
* Incident response automation

## Agentic Development Tools

AI agents that can modify files, run commands, access repositories, create pull requests, interact with CI/CD, or call external systems require explicit approval before use. In addition to the requirements for AI-generated code, the following requirements apply:

* Agents must operate with least privilege
* Agents must not receive production secrets
* Agents must not receive production credentials, unrestricted repository write access, or deployment authority without a separate approval from the &lt;approver of elevated agent access, e.g., VP of Engineering&gt;  and a logging path
* Agents must produce reviewable artifacts describing commands run, files changed, and assumptions made
* Changes produced by an agent shall pass through the same change control procedures as any other change

## High-Impact AI Use Cases

Any AI system that makes or materially influences a decision about a person, customer, employee, vendor, security event, financial outcome, legal obligation, or access to essential services requires documented risk review, human oversight design, logging expectations, a monitoring plan, and a named business owner before launch.

Before launching a new AI use case, the owner of the use case shall answer the following questions:

1. Does the system make or materially influence a decision about a person?
1. Does it touch regulated data or customer confidential data?
1. Can it affect access to money, employment, healthcare, education, housing, essential services, or legal rights?
1. Can it take action automatically rather than merely recommend?
1. Can it access production systems, secrets, customer data, repositories, CI/CD, or administrative APIs?
1. Would a wrong answer create security, financial, legal, reputational, or safety harm?

If any answer is yes, the use case leaves the lightweight path and enters a reviewed path. A reviewed use case shall not launch until the &lt;approver of high-impact AI use cases, e.g., CISO and General Counsel&gt;  has approved it. The reviewed path requires:

* Documented purpose
* Data classification
* Risk assessment, performed in accordance with the {{company_name}} Risk Management Policy <sup>7</sup>
* Named business owner
* Human oversight design
* Logging and monitoring
* Rollback plan
* Vendor review
* Launch approval

A high-impact use case shall be reviewed again when its purpose, data, model, or vendor changes.

## Transparency

Where law, regulation, or contract requires it, {{company_name}} shall disclose to customers and other affected persons that they are interacting with an AI system or receiving AI-generated content.

## Logging & Monitoring

Audit logging shall be enabled for coding assistants, agents, and production AI systems where the tool provides it. Logs from agents and production AI systems shall record the actions taken and the identity under which they were taken, and shall be retained in accordance with the {{company_name}} Operations Security Policy <sup>8</sup>.

The &lt;team responsible for monitoring AI tool usage, e.g., Security Team&gt;  shall review AI tool usage for unapproved tools and unapproved license tiers at least &lt;frequency of usage review, e.g., quarterly&gt; .

## Tool Onboarding

Personnel may request approval of a new AI tool or license tier by submitting a request to the &lt;receiver of AI tool requests, e.g., Security Team&gt; . The request shall state the intended use, the data classifications involved, and the tool category. The onboarding process shall be one that developers can use without waiting weeks.

The &lt;receiver of AI tool requests, e.g., Security Team&gt;  shall respond to requests within &lt;response time for tool requests, e.g., ten (10) business days&gt; . New AI vendors shall be assessed in accordance with the {{company_name}} Third-Party Management Policy <sup>9</sup>.

## Changes to Vendor Terms

Tool approval depends on the vendor terms, license tier, data retention posture, model training posture, administrative controls, audit logging, and security architecture in effect at the time of approval.

&lt;teams responsible for vendor review, e.g., Procurement and Security&gt;  must re-verify these conditions at renewal and when the vendor materially changes terms or functionality. A tool that no longer meets the conditions of its approval shall be removed from the register until it is approved again.

## Training

All personnel who use AI tools shall complete training on this policy upon hire and at least annually. Training shall cover the approved tool register, the data boundaries, and the review requirements for AI-generated code. Training shall explain the reason for each requirement, not only what is forbidden.

## Incident Reporting

Personnel shall report the submission of data to an unapproved AI tool, or to a tool not approved for that data classification, in accordance with the {{company_name}} Incident Response Plan <sup>10</sup>.

## Policy Review

This policy and the approved AI tool register shall be reviewed at least &lt;frequency of policy review, e.g., annually&gt; , and after any of the following events:

* Vendor changes to the terms or functionality of an approved tool
* Incidents involving an AI tool
* Adoption of new tools
* Regulatory developments that apply to {{company_name}}’s use of AI

## Exceptions

Requests for an exception to this Policy must be submitted to the &lt;approver of exceptions to this policy, e.g., CISO&gt;  for approval. Each approved exception shall have an expiration date, compensating controls, and a named risk owner.

## Violations & Enforcement

Any known violations of this policy should be reported to the &lt;receiver of reported violations to this policy, e.g., CISO&gt; . Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

## APPENDIX A – Approved AI Tool Register <sup>11</sup>

| Tool | Category | Approved License Tier | Highest Data Classification Permitted | Tool Owner | Vendor Trains on Company Data | Vendor Retention Period | Renewal Date |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| &lt;tool name&gt; | Enterprise AI tool | &lt;tier&gt; | Confidential | &lt;owner&gt; | No | &lt;period&gt; | &lt;date&gt; |
| &lt;tool name&gt; | Agentic development tool | &lt;tier&gt; | Confidential | &lt;owner&gt; | No | &lt;period&gt; | &lt;date&gt; |
| &lt;tool name&gt; | Self-hosted or private AI system | Not applicable | Confidential | &lt;owner&gt; | Not applicable | &lt;period&gt; | Not applicable |

***Master Version:*** &lt;link&gt;

<hr />

<sup>1</sup> All fields in this document marked by angled brackets &lt; &gt;  and highlighted must be filled in.

<sup>2</sup> Update these categories to match the AI tools your company uses. Remove any category that does not apply.

<sup>3</sup> This is a reference to an appendix in this document. If your register is maintained elsewhere, include a reference or a link to it.

<sup>4</sup> Update the classification labels in this section to match your company’s data classification labels.

<sup>5</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s data classification labels here.

<sup>6</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s code review and testing requirements here.

<sup>7</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s risk assessment process here.

<sup>8</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s log retention requirements here.

<sup>9</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s vendor assessment process here.

<sup>10</sup> This is a reference to another Openlane policy. If you are not planning on using this policy, describe your company’s incident reporting process here.

<sup>11</sup> You can remove this table from the document as long as you include a link or a reference to your approved AI tool register. It is recommended that you structure your register like this table.
