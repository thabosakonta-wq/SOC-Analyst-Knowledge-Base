# Incident Lifecycle

The incident lifecycle is a structured process used by Security Operations teams to manage cybersecurity incidents from preparation through recovery and post-incident improvement.

A well-defined incident lifecycle helps SOC teams respond consistently, reduce the impact of security incidents, restore affected services, and improve security controls after an incident.

---

# What is Incident Response?

Incident response is the process of identifying, investigating, containing, and recovering from cybersecurity incidents.

A cybersecurity incident may include:

* Malware infections
* Phishing attacks
* Compromised user accounts
* Unauthorized access
* Suspicious network activity
* Data security incidents

Incident response requires coordination between people, processes, and security technologies.

---

# Phase 1 — Preparation

Preparation establishes the people, processes, technologies, and procedures needed to respond to security incidents.

Activities include:

* Defining incident response procedures
* Establishing roles and responsibilities
* Configuring security monitoring
* Preparing communication procedures
* Maintaining security tools
* Developing incident response playbooks
* Training security personnel

Preparation allows SOC teams to respond more effectively when an incident occurs.

---

# Phase 2 — Detection and Analysis

Detection and analysis identifies potentially malicious activity and determines whether an event represents a security incident.

Activities include:

* Monitoring security alerts
* Reviewing logs
* Analysing suspicious activity
* Validating alerts
* Identifying affected users and systems
* Determining the scope of the incident
* Assigning an appropriate severity level
* Escalating confirmed incidents

SOC Analysts play an important role in distinguishing genuine security incidents from false positives.

---

# Phase 3 — Containment

Containment limits the spread and impact of a security incident.

Activities may include:

* Isolating affected endpoints
* Disabling compromised accounts
* Blocking malicious IP addresses or domains
* Restricting network access
* Blocking malicious processes
* Applying temporary security controls

Containment should reduce the attacker's ability to continue operating while preserving information required for investigation.

---

# Phase 4 — Eradication

Eradication removes the cause of the security incident and eliminates the attacker's presence from affected systems.

Activities may include:

* Removing malware
* Deleting malicious files
* Removing persistence mechanisms
* Resetting compromised credentials
* Removing unauthorized accounts
* Patching exploited vulnerabilities
* Rebuilding compromised systems when necessary

The objective is to remove the threat before systems are returned to normal operation.

---

# Phase 5 — Recovery

Recovery restores normal business operations.

Activities include:

* Restoring systems
* Monitoring for additional threats
* Confirming systems are secure
* Returning services to users

---

# Phase 6 — Lessons Learned

After an incident, teams review what happened.

Activities include:

* Writing incident reports
* Identifying weaknesses
* Improving detection rules
* Updating procedures
* Sharing knowledge

Lessons learned help organizations improve their ability to prevent, detect, investigate, and respond to future incidents.

---

# SOC Analyst Role During Incident Response

A SOC Analyst may:

* Monitor alerts
* Investigate suspicious activity
* Collect evidence
* Document findings
* Escalate incidents
* Support containment activities

The SOC Analyst works with other security and IT teams when an incident requires additional investigation, containment, remediation, or recovery.

---

# Real-World Example

A user reports a suspicious email.

The SOC:

1. Receives the alert.
2. Analyses the email headers.
3. Checks if the link was accessed.
4. Searches for similar emails.
5. Blocks the malicious domain.
6. Removes the email from other inboxes.
7. Updates detection rules.

This example demonstrates how detection, investigation, containment, remediation, and continuous improvement can work together during incident response.

---

# Incident Lifecycle and NIST

The incident lifecycle aligns closely with the NIST Incident Response Framework:

* Preparation
* Detection and Analysis
* Containment, Eradication, and Recovery
* Post-Incident Activity

The terminology used by different incident response frameworks may vary, but the underlying objective is to prepare for incidents, identify and analyse them, contain and remediate the threat, recover affected services, and improve future response capabilities.

---

# Key Takeaways

* Incident response follows a structured process.
* Preparation establishes the capability to respond to incidents.
* Detection and analysis identify and investigate suspicious activity.
* Containment limits the spread and impact of an incident.
* Eradication removes the underlying threat.
* Recovery restores affected systems and services.
* Lessons learned improve future security operations.
* SOC Analysts play an important role in detection, investigation, documentation, and escalation.

---

# Review Questions

1. What is a cybersecurity incident?
2. What happens during detection and analysis?
3. Why is containment important?
4. What is the purpose of lessons learned?
5. Which security framework includes incident response guidance?
6. What is the purpose of the preparation phase?
7. What is the difference between containment and eradication?
8. Why is recovery performed after eradication?
9. What role does a SOC Analyst play during incident response?
10. Why are lessons learned important after an incident?

---

# Further Reading

* NIST SP 800-61 Incident Handling Guide
* Microsoft Security Operations Documentation
* MITRE ATT&CK Framework

> **Interview Tip:**
> When explaining incident response in an interview, describe the lifecycle in order and explain what the SOC Analyst contributes at each stage.

> **SC-200 Exam Note:**
> Understand how security alerts move from detection and investigation through response and remediation. Be familiar with the role of Microsoft security technologies in monitoring, investigation, incident response, and automated response.

# Key Terms

* **Incident Response:** The process of identifying, investigating, containing, and recovering from cybersecurity incidents.
* **Preparation:** Activities performed before an incident to establish response capability.
* **Detection:** Identification of potentially suspicious or malicious activity.
* **Analysis:** Investigation and validation of activity to determine its nature and scope.
* **Containment:** Actions taken to limit the spread and impact of an incident.
* **Eradication:** Removal of the threat and its persistence from affected systems.
* **Recovery:** Restoration of affected systems and services to normal operation.
* **Lessons Learned:** Review of an incident to identify improvements for future security operations.
* **SOC Analyst:** A security professional who monitors, investigates, documents, and escalates security events and incidents.

