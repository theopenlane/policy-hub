---
title: Risk Assessment
satisfies:
  SOC 2:
    - CC3.1   # Specifies suitable objectives for risk management
    - CC3.2   # Identifies and analyzes risks to objectives, including information security risks
    - CC3.3   # Assesses fraud risk as part of the risk assessment process
    - CC3.4   # Identifies and assesses significant changes that could impact internal control
tags:
    - security
---

## Purpose and Scope

This policy defines {{company_name}}’s requirements for identifying, evaluating, and mitigating risks that may affect the confidentiality, integrity, or availability of critical systems and information assets. It applies to all information systems, including applications, servers, and supporting administrative or maintenance processes.

## Background

Risk management is a foundational element of {{company_name}}’s information security program and requires a systematic approach to identifying risks, evaluating their likelihood and impact, and determining appropriate treatments. This policy establishes the process for assessing threats and vulnerabilities, scoring risks, identifying and implementing treatment plans, and reviewing residual risk after mitigation.

## Policy

### Risk Assessment

The risk assessment process identifies threats and vulnerabilities associated with company assets that could impact the confidentiality, integrity, or availability of information. All in-scope assets—such as documents, applications, systems, infrastructure, and third-party services—must be inventoried and assigned an owner. Threats and vulnerabilities must be recorded in the Risk Assessment Table, and each risk must be assigned a risk owner responsible for evaluating likelihood and impact using defined scoring criteria. Overall risk levels must be calculated based on the combined consequence and likelihood scores.

**Table 3: Description of Consequence Levels and Criteria**

| Consequence Level | Score | Description |
|-------------------|-------|-------------|
| Low               | 0     | Loss of confidentiality, integrity, or availability will not affect the organization's cash flow, legal or contractual obligations, or reputation. |
| Moderate          | 1     | Loss of confidentiality, integrity, or availability may incur financial cost and has low or moderate impact on legal or contractual obligations and/or reputation. |
| High              | 2     | Loss of confidentiality, integrity, or availability will have immediate and/or considerable impact on cash flow, operations, legal obligations, and/or reputation. |

**Table 4: Description of Likelihood Levels and Criteria**

| Likelihood Level | Score | Description |
|------------------|-------|-------------|
| Low              | 0     | Existing controls are strong, incidents are unlikely, and no new incidents are expected. |
| Moderate         | 1     | Controls are moderately effective, minor incidents may have occurred, and new incidents are possible. |
| High             | 2     | Controls are ineffective or absent; incidents are highly likely to occur. |

### Risk Acceptance Criteria

1. Risk values of **0 through 2** are considered acceptable.
1. Risk values of **3 and 4** are considered unacceptable and must be treated.

### Risk Treatment

1. Risk treatment must be documented in the Risk Treatment Table, including treatment options and residual risk.
1. The CEO or designated managers must determine appropriate mitigation objectives.
1. Treatment options include:
   1. Implementing or enhancing security controls
   1. Transferring risk to a third party (e.g., insurance or supplier agreements)
   1. Avoiding the risk by discontinuing the activity
   1. Accepting the risk if treatment costs outweigh the potential impact
1. After selecting a treatment option, the risk owner must estimate new consequence and likelihood values to determine residual risk.

### Regular Reviews of Risk Assessment and Treatment

1. The Risk Assessment Table and Risk Treatment Table must be updated when new risks are identified.
1. The risk assessment and treatment plan must be reviewed at least annually.
1. Updates are also required after significant organizational, technological, or environmental changes.

### Reporting

1. Results of risk assessments, treatments, and reviews must be documented in a Risk Assessment Report.