# What is a Security Operations Center?

A Security Operations Center (SOC) is a centralized security function responsible for monitoring, detecting, investigating, and responding to cybersecurity threats affecting an organization.

A SOC brings together people, processes, and technology to provide continuous visibility into an organization's security environment.

The primary purpose of a SOC is to help an organization identify suspicious activity, determine whether security events represent genuine threats, respond to incidents, and reduce the likelihood and impact of future attacks.

---

# Purpose of a SOC

A SOC provides an organized capability for security monitoring and incident response.

Its objectives commonly include:

* Monitoring security activity across the organization.
* Detecting suspicious or malicious behaviour.
* Investigating security alerts and potential incidents.
* Supporting containment and remediation.
* Protecting organizational systems, users, applications, and data.
* Improving security controls and detection capabilities.
* Maintaining security visibility through continuous monitoring.

Threat detection is only the beginning—**investigation and response are equally important**.

A SOC therefore operates as an ongoing defensive capability rather than simply an alert-monitoring function.

---

# People, Processes, and Technology

An effective SOC depends on three interconnected components:

### People

People perform the analysis, investigation, decision-making, coordination, and response activities required during security operations.

Examples include:

* SOC Analysts
* Incident Responders
* Threat Hunters
* Detection Engineers
* Security Engineers
* SOC Managers

Different SOC roles may have different responsibilities, which will be explored in later chapters.

### Processes

Processes provide structure for how security events and incidents are handled.

Examples include:

* Alert triage
* Incident investigation
* Escalation procedures
* Incident response
* Evidence collection
* Documentation
* Threat hunting
* Detection improvement
* Post-incident review

Well-defined processes help ensure that security events are handled consistently.

### Technology

Technology provides the telemetry, detection, investigation, and response capabilities used by security teams.

Examples include:

* Security Information and Event Management (SIEM)
* Extended Detection and Response (XDR)
* Endpoint Detection and Response (EDR)
* Network monitoring
* Identity and access security
* Threat intelligence platforms
* Security automation and orchestration

People, processes, and technology must work together for effective Security Operations.

---

# Core SOC Functions

Although SOC structures differ between organizations, common SOC functions include:

### Security Monitoring

Analysts monitor security events and alerts from systems throughout the environment.

### Alert Triage

Alerts are reviewed to determine their relevance, severity, and potential impact.

### Investigation

Analysts examine available evidence to determine what happened, when it happened, which systems or users were affected, and whether malicious activity occurred.

### Incident Response

When an event is confirmed as an incident, the SOC supports appropriate response activities such as containment, eradication, recovery, and documentation.

### Threat Hunting

Threat Hunters proactively search security telemetry for suspicious activity that may not have generated a conventional alert.

### Detection Engineering

Detection Engineers develop and improve detection rules, queries, and other mechanisms used to identify malicious activity.

### Continuous Improvement

Security teams use lessons learned from investigations and incidents to improve detections, procedures, controls, and monitoring capabilities.

---

# Common SOC Technologies

SOC teams may use multiple technologies to collect telemetry, detect threats, investigate activity, and support response.

### SIEM

A Security Information and Event Management platform collects and analyses security-related data from multiple sources.

A SIEM can help analysts:

* Search security logs.
* Correlate events.
* Create detection rules.
* Investigate incidents.
* Monitor security activity.

### EDR and XDR

Endpoint Detection and Response (EDR) provides visibility into endpoint activity and supports investigation and response.

Extended Detection and Response (XDR) can correlate security information across multiple security domains, such as endpoints, identities, email, applications, and networks.

### SOAR and Automation

Security Orchestration, Automation and Response (SOAR) technologies can automate repetitive security tasks and coordinate response workflows.

Automation may help with activities such as:

* Enriching alerts.
* Gathering information.
* Notifying analysts.
* Isolating systems.
* Updating security controls.

### Threat Intelligence

Threat intelligence provides information about threats, adversaries, indicators, and attacker behaviour that can support detection and investigation.

---

# Continuous Security Monitoring

Cybersecurity threats can occur at any time. Continuous monitoring allows organizations to identify suspicious activity as it occurs or shortly afterwards.

SOC monitoring may include:

* Authentication activity.
* Endpoint activity.
* Network traffic.
* Email activity.
* Cloud activity.
* Application activity.
* Security configuration changes.

Continuous monitoring improves visibility and gives security teams more opportunities to identify and respond to threats.

---

# The SOC Analyst Perspective

For a SOC Analyst, a SOC is an operational environment in which security information is continuously evaluated.

An analyst may receive an alert indicating:

> Multiple failed login attempts followed by a successful login.

The analyst should not automatically assume that the event represents a confirmed compromise.

Instead, the analyst may investigate:

* The source IP address.
* The affected user account.
* Authentication timestamps.
* The device involved.
* Geographic information.
* Related authentication events.
* Other activity performed by the account.
* Whether similar activity affected other accounts.

The analyst then determines whether the activity is benign, suspicious, or indicative of a security incident, based on the available evidence and organizational procedures.

---

# Real-World Example

Consider an organization where an employee's account generates an unusual authentication alert.

The SOC may follow a process such as:

1. The security platform generates an alert.
2. A SOC Analyst performs initial triage.
3. Authentication logs are reviewed.
4. The user's device and recent activity are examined.
5. Related alerts and indicators are searched for.
6. The analyst determines whether the activity is legitimate or suspicious.
7. If necessary, the incident is escalated.
8. Appropriate containment or remediation actions are supported.
9. The investigation is documented.
10. Detection rules or security controls may be improved based on the findings.

This demonstrates how **monitoring, detection, investigation, response, and continuous improvement** operate together.

---

# SOC vs IT Help Desk

A SOC and an IT Help Desk both support an organization, but they have different primary responsibilities.

| SOC                                    | IT Help Desk                       |
| -------------------------------------- | ---------------------------------- |
| Focuses on cybersecurity               | Focuses on IT user support         |
| Monitors security events               | Handles user support requests      |
| Investigates suspicious activity       | Troubleshoots technical problems   |
| Responds to security incidents         | Resolves service and access issues |
| Analyses security telemetry            | Supports applications and devices  |
| Supports threat detection and response | Supports normal IT operations      |

There can be collaboration between the two functions.

For example, an IT Help Desk may report a suspected phishing email or compromised account to the SOC for security investigation.

---

# Benefits of a SOC

A SOC can provide organizations with:

* Continuous security monitoring.
* Centralized security visibility.
* Structured alert investigation.
* Faster identification of threats.
* Coordinated incident response.
* Improved detection capabilities.
* Better understanding of attacker behaviour.
* Security knowledge gained from previous incidents.

The effectiveness of a SOC depends on appropriate people, processes, technology, and organizational support.

---

# Summary

A Security Operations Center provides a structured capability for monitoring, detecting, investigating, and responding to cybersecurity threats.

A SOC combines **people, processes, and technology** to maintain security visibility and support incident response.

Threat detection is only the beginning—investigation, response, documentation, and continuous improvement are equally important.

SOC Analysts work within this environment to evaluate security events, investigate suspicious activity, support incident response, and contribute to improving organizational security.

---

# Key Takeaways

* A SOC provides centralized security monitoring and response capabilities.
* SOC operations depend on people, processes, and technology.
* Core SOC functions include monitoring, alert triage, investigation, incident response, threat hunting, and detection engineering.
* SIEM, EDR, XDR, SOAR, and threat intelligence technologies can support SOC operations.
* Continuous monitoring improves security visibility.
* SOC Analysts investigate evidence rather than automatically treating every alert as a confirmed incident.
* A SOC and IT Help Desk have different primary responsibilities but may work together.
* Security Operations includes continuous improvement based on lessons learned.

---

# Review Questions

1. What is the purpose of a Security Operations Center?
2. Name five responsibilities of a SOC.
3. What technologies are commonly used in a SOC?
4. Why is continuous monitoring important?
5. How does a SOC differ from an IT Help Desk?

---

# Further Reading

* NIST SP 800-61
* MITRE ATT&CK Framework
* Microsoft Sentinel Documentation

---

> **Interview Tip**
>
> A common SOC interview question is:
>
> **"What is a SOC?"**
>
> A strong answer should explain that a SOC is a security function that combines people, processes, and technology to continuously monitor an organization's environment, detect and investigate threats, support incident response, and improve defensive capabilities.

---

> **SC-200 Exam Note**
>
> For the SC-200, understand the role of the SOC and how security analysts use Microsoft security technologies to monitor, investigate, hunt for threats, and respond to incidents.
>
> Pay particular attention to the relationship between Microsoft Sentinel, Microsoft Defender XDR, security telemetry, detection, investigation, and incident response.

---

# Key Terms

* Security Operations Center (SOC)
* SOC Analyst
* Security Monitoring
* Alert Triage
* Security Event
* Security Incident
* SIEM
* EDR
* XDR
* SOAR
* Threat Intelligence
* Security Telemetry
* Threat Hunting
* Detection Engineering
* Incident Response
* Containment
* Remediation

