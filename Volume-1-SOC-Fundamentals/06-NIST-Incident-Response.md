# SOC Analyst Knowledge Base

A structured cybersecurity handbook designed to document the knowledge, concepts, tools, and methodologies used by Security Operations Center (SOC) Analysts.

This repository combines theory, practical examples, industry frameworks, and Microsoft security technologies to support continuous learning, interview preparation, and real-world SOC operations.

## Who is this for?

- Aspiring SOC Analysts
- Blue Team professionals
- Cybersecurity students
- Microsoft SC-200 learners
- Threat Hunters
- Detection Engineers

---

# NIST Incident Response

NIST Incident Response provides a structured approach for preparing for, detecting, responding to, and learning from cybersecurity incidents.

For a SOC Analyst, an incident response framework helps provide a consistent process for handling suspicious activity and security incidents.

The framework connects technical investigation with organized response actions and post-incident improvement.

---

# The NIST Incident Response Lifecycle

Incident response can be viewed as a continuous operational lifecycle:

1. Preparation
2. Detection and Analysis
3. Containment
4. Eradication
5. Recovery
6. Post-Incident Activity

Each stage has a specific purpose, but incident response is not always strictly linear. New evidence discovered during an investigation may require analysts and response teams to revisit earlier activities.

---

# Phase 1 — Preparation

Preparation establishes the people, processes, technologies, and procedures required to respond to security incidents.

Examples include:

- Understanding security policies and procedures
- Preparing incident response plans
- Configuring security monitoring
- Maintaining appropriate logging
- Understanding available security tools
- Establishing communication and escalation procedures
- Preparing investigation and response resources

### SOC Analyst Perspective

A SOC Analyst needs to understand the organization's security tools and procedures before an incident occurs.

Good preparation allows analysts to respond consistently instead of determining the response process for the first time during an active incident.

---

# Phase 2 — Detection and Analysis

Detection and analysis begins when suspicious activity is identified.

A SOC may receive information from:

- SIEM alerts
- Endpoint security tools
- Authentication logs
- Network monitoring
- Email security systems
- User reports
- Threat intelligence
- Security detections

The analyst then investigates the available evidence to determine whether the activity represents a potential security incident.

### SOC Analyst Perspective

The analyst may:

- Review authentication logs
- Examine endpoint activity
- Investigate related alerts
- Identify affected accounts or systems
- Establish a timeline
- Determine whether activity is suspicious or legitimate
- Escalate confirmed incidents

The objective is to move from an alert or observation toward an evidence-based understanding of what happened.

---

# Phase 3 — Containment

Containment focuses on limiting the impact of a security incident.

Depending on the situation, response actions may include:

- Disabling a compromised account
- Isolating an affected endpoint
- Blocking malicious network activity
- Restricting access
- Revoking sessions
- Blocking malicious indicators

Containment should be performed carefully because response actions can affect legitimate users and systems.

### SOC Analyst Perspective

A SOC Analyst may support containment by providing evidence and recommending or initiating approved response actions according to organizational procedures.

The analyst should document:

- What was contained
- Why containment was necessary
- When the action occurred
- Who performed or approved the action
- What evidence supported the action

---

# Phase 4 — Eradication

Eradication focuses on removing the cause or components of the security incident.

Examples include:

- Removing malicious software
- Resetting compromised credentials
- Removing unauthorized access
- Deleting malicious persistence mechanisms
- Addressing exploited vulnerabilities
- Removing malicious accounts or configurations

### SOC Analyst Perspective

The analyst uses investigation findings to help determine what needs to be removed or corrected.

Eradication should address the underlying cause rather than simply removing the visible symptom.

---

# Phase 5 — Recovery

Recovery focuses on safely returning affected systems, accounts, and services to normal operation.

Recovery activities may include:

- Restoring affected systems
- Re-enabling user access
- Validating security controls
- Monitoring restored systems
- Confirming that malicious activity has stopped
- Continuing heightened monitoring where appropriate

### SOC Analyst Perspective

The SOC Analyst can help verify that systems remain clean and that suspicious activity does not return.

Monitoring after recovery is important because an incident should not be considered fully resolved simply because a system has been restored.

---

# Phase 6 — Post-Incident Activity

Post-incident activity focuses on learning from the incident and improving future security operations.

Activities may include:

- Documenting findings
- Reviewing the incident timeline
- Identifying lessons learned
- Improving detection rules
- Updating procedures
- Identifying control weaknesses
- Recording indicators of compromise
- Improving future response capability

### SOC Analyst Perspective

The SOC Analyst contributes valuable technical information from the investigation.

For example, an investigation may reveal that an existing detection rule failed to identify a particular technique.

The SOC team can use that information to improve detection coverage and reduce the likelihood of similar activity going unnoticed.

---

# SOC Analyst Role During Incident Response

A SOC Analyst contributes throughout the incident response lifecycle.

| Stage | SOC Analyst Contribution |
|---|---|
| Preparation | Understand tools, procedures, logging, and escalation paths |
| Detection | Identify and triage security alerts |
| Analysis | Investigate logs, alerts, endpoints, accounts, and timelines |
| Containment | Support approved response actions |
| Eradication | Help identify malicious activity and affected resources |
| Recovery | Validate systems and monitor for recurring activity |
| Post-Incident | Document findings and improve detections |

The SOC Analyst therefore does not work only at the moment an alert appears.

Effective incident response requires continuous preparation, investigation, communication, documentation, and improvement.

---

# Real-World Example

A user account shows suspicious login activity.

### Detection

A SIEM generates an alert indicating unusual authentication activity.

### Analysis

The analyst reviews:

- Authentication logs
- Login locations
- Login times
- Related alerts
- User activity
- Device information

The analyst determines that the activity requires further investigation.

### Containment

The account is temporarily disabled or access is restricted according to the organization's response procedure.

### Eradication

The compromised credentials are reset and malicious access is removed.

### Recovery

The user's access is restored after appropriate validation.

### Post-Incident Activity

The SOC reviews the incident and improves detection rules based on what was learned.

This example demonstrates how a SOC Analyst can move from an initial alert through investigation and response while maintaining an evidence-based process.

---

# NIST vs SOC Operations

NIST provides the structured incident response process.

SOC teams provide the people, tools, procedures, and actions needed to execute that process.

For example:

- NIST provides the response framework.
- The SOC monitors security events.
- SOC Analysts investigate alerts.
- Security tools provide telemetry and detection.
- Response teams perform approved containment and remediation actions.
- Post-incident reviews improve future security operations.

Together, the framework and operational capabilities support an organized incident response capability.

---

# Key Takeaways

- Incident response provides a structured approach to handling security incidents.
- Preparation establishes the foundation for effective response.
- Detection and analysis identify and investigate suspicious activity.
- Containment limits the potential impact of an incident.
- Eradication focuses on removing malicious activity and addressing its causes.
- Recovery returns affected systems and services to normal operation.
- Post-incident activity captures lessons and improves future security operations.
- SOC Analysts contribute throughout the incident response lifecycle.
- Documentation and evidence are important throughout the response process.

---

# Review Questions

1. What is the purpose of an incident response framework?
2. What activities take place during preparation?
3. What is the difference between detection and analysis?
4. What is the purpose of containment?
5. What is the purpose of eradication?
6. Why is recovery performed after eradication?
7. Why is post-incident activity important?
8. How does a SOC Analyst contribute during incident response?
9. How does NIST relate to SOC operations?
10. Why should incident response activities be documented?

---

# Further Reading

- NIST SP 800-61 Incident Handling Guide
- NIST Cybersecurity Framework
- Microsoft Security Operations Documentation

---

# Interview Tip

**Question:** How does a SOC Analyst contribute to incident response?

**Answer:**

A SOC Analyst contributes throughout the incident response lifecycle by monitoring security events, triaging and investigating alerts, analyzing evidence, supporting containment and remediation activities, documenting findings, and contributing to lessons learned and detection improvements.

---

# SC-200 Exam Note

When studying for the Microsoft Security Operations Analyst certification, connect incident response concepts to practical security operations.

Important areas include:

- Alert investigation
- Incident management
- Security monitoring
- Threat detection
- Investigation of affected users and devices
- Containment and remediation
- Security automation
- Post-incident improvement

The important connection is between **security telemetry, detection, investigation, incident response, and remediation**.

---

# Key Terms

| Term | Meaning |
|---|---|
| Incident Response | The organized process used to handle cybersecurity incidents |
| Preparation | Activities performed before an incident to establish response capability |
| Detection | Identification of potentially suspicious or malicious activity |
| Analysis | Examination of evidence to understand an event or incident |
| Containment | Actions taken to limit the impact of an incident |
| Eradication | Removal of malicious activity and its causes |
| Recovery | Restoration and validation of affected systems or services |
| Post-Incident Activity | Review and improvement following an incident |
| SIEM | Security platform used to collect, correlate, monitor, and investigate security events |
| SOC Analyst | Security professional responsible for monitoring and investigating security activity |
