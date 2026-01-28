---
title: Business Continuity and Disaster Recovery (BC/DR)
satisfies:
  SOC 2:
    - A1.1
    - A1.2
    - A1.3
tags:
    - availability
---

## Purpose

The purpose of this business continuity plan is to prepare {{company_name}} in the event of service outages caused by factors beyond our control (e.g., natural disasters, man-made events), and to restore services to the widest extent possible in a minimum time frame.

## Scope

All {{company_name}} IT systems that are business critical. This policy applies to all employees of {{company_name}} and to all relevant external parties, including but not limited to {{company_name}} consultants and contractors.

The following scenarios are excluded from the BC/DR plan scope[\^3]:

* Loss of availability for a production hosting service provider (i.e., &lt;production hosting service provider, e.g., AWS&gt; )
* Loss of availability of {{company_name}} satellite offices (these will be considered incidents)

In the event of a loss of availability of a hosting service provider, the &lt;driver of the response, e.g., VP of Global Support&gt;  will confer with the &lt;assistants for the response, e.g., IT Manager and executive staff&gt;  to determine an appropriate response strategy[\^4].

## Policy

In the event of a major disruption to production services and a disaster affecting the availability and/or security of the {{company_name}} office, senior managers and executive staff shall determine mitigation actions.

A disaster recovery test, including a test of backup restoration processes, shall be performed on an annual basis.

Continuity of information security shall be considered along with operational continuity.

In the case of an information security event or incident, refer to the Incident Response Plan[\^5].

## Alternate Work Facilities

If the {{company_name}} office becomes unavailable due to a disaster, all staff shall work remotely from their homes or any safe location.

## Communications and Escalation

Executive staff and senior managers should be notified of any disaster affecting {{company_name}} facilities or operations.

Communications shall take place over any available regular channels including &lt;list your company’s regular communication channels, e.g., Slack, email, phone and online meeting tools&gt; .

Key contacts shall be maintained on the on-call schedule and key contacts: &lt;link to wiki page that lists out key contacts&gt; [\^6]

## Roles and Responsibilities[\^7]

| Role | Responsibility |
| :---- | :---- |
| &lt;IT Manager&gt;  | The IT Manager shall lead BC/DR efforts to mitigate losses and recover the corporate network and information systems. |
| &lt;Departmental Heads&gt;  | Each department head shall be responsible for communications with their departmental staff and any actions needed to maintain continuity of their business functions. Departmental heads shall communicate regularly with executive staff and the IT Manager. |
| &lt;Managers&gt;   | Managers shall be responsible for communicating with their direct reports and providing any needed assistance for staff to continue working from alternative locations. |
| &lt;VP of Global Support&gt;   | The VP of Global Support, in conjunction with the CEO and CFO shall be responsible for any external and client communications regarding any disaster or business continuity actions that are relevant to customers and third parties. |
| &lt;VP of Engineering&gt;  | The VP of Engineering, in conjunction with the VP of Global Support, shall be responsible for leading efforts to maintain continuity of {{company_name}} services to customers during a disaster. |
| &lt;Chief HR Officer&gt;  | The CHRO shall be responsible for internal communications to employees as well as any action needed to maintain physical health and safety of the workforce. The CHRO shall work with the IT Manager to ensure continuity of physical security at the {{company_name}} office. |

## Continuity of Critical Services

Procedures for maintaining continuity of critical services in a disaster can be found in Appendix A[\^8].

Recovery Time Objectives (RTO) and Recovery Point Objects (RPO) can be found in Appendix B.

Strategy for maintaining continuity of services can be seen in the following table[\^9]:

| KEY BUSINESS PROCESS | CONTINUITY STRATEGY |
| :---- | :---- |
| Customer (Production) Service Delivery | Rely on AWS availability commitments and SLAs |
| IT Operations | Not dependent on HQ. VPN is redundant between HQ and Colo. Critical data is backed up to alternate locations. |
| Email | Utilize Gmail and its distributed nature, rely on Google’s standard service level agreements. |
| Finance, Legal and HR | All systems are vendor-hosted SaaS applications. |
| Sales and Marketing | All systems are vendor-hosted SaaS applications. |

#### Plan Activation

This BC/DR shall be automatically activated in the event of the loss or unavailability of the {{company_name}} office, or a natural disaster (i.e., severe weather, regional power outage, earthquake) affecting the larger &lt;describe the location of your company’s headquarters, e.g., San Francisco, CA&gt; region.

## Appendix A – Business Continuity Procedures by Scenario[\^10]

### Business Continuity Scenarios

#### HQ Offline (power and/or network)

* CRM, Telephony, Video Conferencing/Screen Share & Corp Email unaffected
* SUPPORT unaffected
* HQ Staff offline (30-60 minutes)
* Remote Staff unaffected (US)

##### Procedure:

1. HQ Staff relocate to home offices (30-60 minutes)
2. Verify Telephony, CRM, & Email Connectivity at home offices (10 minutes)
3. Remotely resume normal operations 

#### Colo Offline (power and/or network)

* CRM, Telephony, Video Conferencing/Screen Share & Corp Email unaffected
* SUPPORT Offline
* Production Database offline (redundant)
* HQ Staff unaffected
* Remote Staff unaffected (US)

##### Procedure:

1. Notify Customer Base that proactive monitoring is offline
2. Normal operations continue

#### Disaster Event at HQ (&lt;Location 1&gt;  & &lt;Location 2&gt; )

* CRM, Telephony, Video Conferencing/Screen Share & Corp Email unaffected
* SUPPORT offline
* HQ Staff offline (variable impact)
* Remote Staff unaffected (US)

##### Procedure:

3. Activate Remote Staff (US)
4. Notify Customer Base of impaired functions & potential delays
5. Commandeer Field Resources for Critical Response (SE Teams)

#### SaaS Tools Down

* CRM, Telephony, Video Conferencing/Screen Share, or Corp Email Affected
* SUPPORT partially affected (no new cases, manual triage required)
* HQ Staff unaffected
* Remote Staff unaffected (US)

##### Procedures:

###### Telephone Down

1. Notify Customer Base to use Support Portal or Email
1. Support Staff use Mobile Phones and/or Land Lines as needed

###### Email Down (Gmail/Corp Email)

1. Support Staff manually manage ‘case’ related communications
1. Support Staff use alternate email accounts as needed (Hotmail)

###### CRM Down

1. Notify Customer Base that CRM is down
1. Activate ‘Spreadsheet’ Case Tracking (Google Sheets)
1. Leverage ‘Production’ Database for Entitlements, Case History, Configuration data.

###### *Video Conferencing/ScreenShare Down (Zoom)*

4. Support Staff utilize alternate service as needed

## Appendix B – RTOs/RPOs[\^11]

| Rank | Asset | Affected Assets | Business Impact | Users | Owners | Recovery Time Objective (RTO) | Recovery Point Objective (RPO) | Comments / Gaps |
| :---: | ----- | ----- | ----- | ----- | ----- | :---: | :---: | ----- |
| 1 | Google Datacenters | Site | Core services | All | Engineering |  |  |  |
| 2 | Corporate Office | Site | Inability to access data? Any other impacts? | All | IT Ops |  |  |  |
| 3 | Corporate Network | Network | Inability to use network resources from corporate office | All | IT Ops |  |  |  |
| 4 | Google Cloud | Network | Core services | All | Engineering |  |  |  |
| 5 | Home Office ISP Networks | Network |  | IT Ops, Development | N/A |  |  |  |
| 6 | Subcontractor Networks | Network |  | Development | N/A |  |  |  |
| 7 | Third Party Networks | Network |  | Sales | N/A |  |  |  |
| 8 | Company Laptops | Hardware |  | All | IT Ops |  |  |  |
| 9 | Digital Projector | Hardware |  | All | IT Ops |  |  |  |
| 10 | Office Printers | Hardware | Inability to print in corporate office | All | IT Ops |  |  |  |
| 11 | Personal Mobile Device | Hardware |  |  |  |  |  |  |
| 12 | Wireless Access Points (WAP) | Hardware |  | All | IT Ops |  |  |  |

[\^1]:  All fields in this document marked by angled brackets &lt; &gt;  and highlighted must be filled in.

[\^2]:  BC/DR Policies and Plans differ significantly between different organizations. If you have an existing plan that works you should consider keeping it. You can also find other examples and templates. Pick what works best for your organization.

[\^3]:  Exclusions to this policy should be customized to your organization. Your company may not have any exclusions in which case you can remove this language. These scenarios are provided as an example.

[\^4]:  Change or remove this language based on your organization’s needs.

[\^5]:  This is a reference to another Openlane document. If you are not planning on using this document, describe how your company will respond to an information security event or incident here. It is, however, highly recommended that your organization has an Incident Response Plan because a managed approach to incident response is a requirement for all information security management standards.

[\^6]:  If your company does not use a wiki or some form of an internal knowledge base that can be linked here, you can list out the key contacts in this document. If you list out the contacts here, however, you will need to continually update this document and your employees may have to re-accept this policy if there are major changes.

[\^7]:  Adjust this table of roles and responsibilities to describe the roles and responsibilities for members of the BC/DR team

[\^8]:  This references an appendix in this document. If you describe these procedures elsewhere, update this reference.

[\^9]:  Adjust the table below the describe your company’s continuity strategies

[\^10]:  In this appendix, describe your company’s business continuity procedures. The scenarios listed in this table are examples of what you might consider including.

[\^11]:  Customize for your business
