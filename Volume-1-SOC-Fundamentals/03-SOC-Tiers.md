# SOC Tiers

A Security Operations Center (SOC) may organize its security operations into different tiers or levels of responsibility. Tiering helps organizations manage security alerts efficiently by assigning activities according to their complexity, required expertise, and potential impact.

Although the terms Tier 1, Tier 2, and Tier 3 are commonly used, SOC structures are not universal. Organizations may use different names, responsibilities, or numbers of tiers depending on their size, technology, security maturity, and operational model.

---

# Why SOCs Use Tiers

SOC tiering helps organizations:

* Manage large volumes of security alerts
* Prioritize potential security incidents
* Assign investigations to appropriate levels of expertise
* Establish clear escalation procedures
* Improve consistency in incident handling
* Separate initial triage from deeper investigation
* Support specialized security functions
* Improve the efficient use of SOC resources

Tiering does not necessarily represent organizational rank. It is primarily an operational model for distributing security responsibilities.

---

# Tier 1 — Monitoring and Triage

Tier 1 is commonly responsible for the initial monitoring and triage of security alerts.

Tier 1 analysts may:

* Monitor security alerts and notifications
* Review SIEM, EDR, XDR, and other security alerts
* Validate whether an alert requires investigation
* Identify potential false positives
* Collect initial information about the alert
* Classify and prioritize alerts
* Document observations and actions
* Correlate basic supporting information
* Escalate suspicious or confirmed incidents
* Continue monitoring after escalation when required

The objective of Tier 1 is not necessarily to perform the entire investigation. Instead, the analyst determines what the alert represents, gathers the initial evidence, and ensures that important events are escalated appropriately.

### SOC Analyst Perspective

During initial triage, an analyst may receive an alert showing multiple failed login attempts followed by a successful login.

The analyst may examine:

* Source IP address
* Username
* Authentication timestamps
* Device information
* Geographic location
* Authentication method
* Related alerts
* Other activity associated with the account

The analyst then determines whether the activity appears benign, suspicious, or potentially malicious and documents the reasoning before escalating when necessary.

---

# Tier 2 — Investigation and Response

Tier 2 generally performs deeper investigation after an alert has been escalated from initial triage.

Tier 2 responsibilities may include:

* Conducting detailed alert investigations
* Correlating events across multiple security sources
* Determining the scope of an incident
* Building an incident timeline
* Investigating affected users and devices
* Reviewing process, authentication, and network activity
* Supporting containment activities
* Coordinating with other security teams
* Collecting additional evidence
* Determining whether escalation to advanced specialists is required

Tier 2 analysts typically work with more detailed evidence and investigate incidents that cannot be resolved through initial triage alone.

---

# Tier 3 — Advanced Analysis and Threat Hunting

Tier 3 generally handles more complex security investigations and advanced analysis.

Depending on the organization's structure, Tier 3 responsibilities may include:

* Advanced incident investigation
* Complex threat analysis
* Threat hunting
* Malware analysis
* Advanced detection analysis
* Investigation of sophisticated attack activity
* Supporting complex containment and remediation
* Developing or improving advanced detections
* Identifying previously undetected threats
* Providing technical guidance to lower tiers

Threat hunting is often associated with Tier 3 activities, but it is **not universally restricted to Tier 3**. Some organizations maintain dedicated threat-hunting teams, while others distribute hunting responsibilities across several SOC functions.

This distinction is important because SOC structures vary between organizations.

---

# Tier 4 and Specialized Security Functions

Some organizations may use a Tier 4 model or separate specialized security functions instead of placing every advanced activity into Tier 3.

Examples of specialized functions may include:

* Digital forensics and incident response (DFIR)
* Malware reverse engineering
* Threat intelligence
* Security engineering
* Detection engineering
* Purple teaming
* Advanced threat research

These functions may operate independently from the traditional SOC tier structure or work closely with SOC analysts during complex incidents.

There is therefore no single universal SOC tier model that applies to every organization.

---

# Incident Escalation

Escalation is the process of transferring an alert or incident to an analyst or team with the appropriate level of expertise or authority.

An incident may require escalation because of:

* High potential impact
* Increased confidence that malicious activity is occurring
* Complex or unclear attack activity
* Compromise of privileged accounts
* Evidence of lateral movement
* Malware execution
* Possible data exfiltration
* Multiple affected systems
* Inability to contain the activity at the current level
* Organizational policy or escalation requirements

Effective escalation ensures that incidents receive appropriate attention without unnecessarily consuming advanced security resources.

Escalation should not be viewed as a failure by the initial analyst. It is a normal part of structured security operations.

---

# How the Tiers Work Together

SOC tiers operate as a coordinated process rather than isolated teams.

A typical workflow may look like:

**Tier 1 → Tier 2 → Tier 3 / Specialized Function**

For example:

1. Tier 1 receives a suspicious authentication alert.
2. Tier 1 validates the alert and collects initial evidence.
3. Tier 1 determines that the activity requires deeper investigation.
4. Tier 2 investigates the affected account, devices, authentication events, and related activity.
5. Tier 2 determines whether additional systems or users are affected.
6. Tier 3 or a specialized team performs advanced analysis if the incident is complex.
7. Detection or security engineering teams may improve security controls based on lessons learned.
8. The SOC continues monitoring for related activity.

This workflow allows different levels of expertise to contribute to the same security operation.

---

# SOC Analyst Perspective

A SOC analyst should understand that tiering is primarily a **process for managing security operations**, not simply a hierarchy of job titles.

An analyst should know:

* What responsibilities belong to their role
* What evidence must be collected
* When an alert should be escalated
* Which team should receive the escalation
* How incidents should be documented
* How to communicate findings clearly
* How to maintain an accurate investigation timeline

Good escalation depends on good documentation.

An analyst should therefore be able to explain not only **what** was detected, but also:

* Why it is suspicious
* What evidence supports the finding
* What systems or users may be affected
* What actions have already been taken
* What additional investigation is required

---

# Real-World Example

Consider an endpoint that generates an alert for suspicious PowerShell activity.

### Tier 1 — Initial Triage

The Tier 1 analyst:

1. Reviews the alert.
2. Identifies the affected endpoint.
3. Identifies the user associated with the activity.
4. Reviews the PowerShell command or available event information.
5. Checks related alerts.
6. Determines that the activity appears suspicious.
7. Documents the initial findings.
8. Escalates the investigation.

### Tier 2 — Investigation

The Tier 2 analyst:

1. Reviews the process tree.
2. Examines parent and child processes.
3. Reviews user activity.
4. Checks network connections.
5. Searches for related events on the endpoint.
6. Determines whether other systems show similar activity.
7. Establishes an incident timeline.
8. Supports containment when required.

### Tier 3 / Specialized Analysis

If the activity is complex, advanced analysts or specialists may:

* Perform deeper threat analysis
* Conduct threat hunting
* Examine additional telemetry
* Develop or modify detection rules
* Investigate possible malware behaviour
* Determine whether similar activity exists elsewhere in the environment

The investigation may then produce improvements to detections and monitoring.

This demonstrates how SOC tiers can work together throughout the incident lifecycle.

---

# SOC Career Progression

A common SOC career progression may involve movement from:

**Tier 1 → Tier 2 → Tier 3 / Specialist**

However, this progression is not universal or necessarily linear.

Career progression depends on:

* Organization structure
* Technical skills
* Security specialization
* Experience
* Certifications
* Performance
* Available roles
* Individual career objectives

Some analysts may move into specialized areas such as:

* Threat Hunting
* Detection Engineering
* DFIR
* Threat Intelligence
* Security Engineering
* Cloud Security

Understanding SOC tiers therefore provides a useful foundation for understanding both SOC operations and possible cybersecurity career paths.

---

# Summary

SOC tiers provide a structured approach for managing security monitoring, investigation, response, and advanced analysis.

Tier 1 commonly focuses on monitoring and initial triage. Tier 2 generally performs deeper investigation and response activities. Tier 3 commonly handles advanced analysis and may include threat hunting, although organizational structures differ.

Specialized security functions may operate alongside or outside the traditional tier structure.

The key principle is that security alerts should be handled at the appropriate level of expertise, with clear escalation, documentation, communication, and collaboration between teams.

---

# Key Takeaways

* SOCs may use tiers to organize security responsibilities.
* Tier 1 commonly performs monitoring and initial alert triage.
* Tier 2 commonly performs deeper investigation and response.
* Tier 3 commonly handles advanced investigations and analysis.
* Threat hunting may be performed by Tier 3 or a dedicated threat-hunting function.
* Some organizations use specialized security teams instead of traditional tier structures.
* Escalation is a normal part of SOC operations.
* Good documentation supports effective escalation.
* SOC tiers work together throughout the incident lifecycle.
* SOC structures vary between organizations.

---

# Review Questions

1. What are the responsibilities of Tier 1?
2. Why are incidents escalated?
3. What does Tier 3 focus on?
4. Which tier usually performs Threat Hunting?
5. What is the normal SOC career progression?

---

# Further Reading

* Microsoft Security Operations
* NIST Incident Response Guide
* MITRE ATT&CK

> **Interview Tip:**
> Be prepared to explain the difference between Tier 1, Tier 2, and Tier 3 SOC responsibilities and describe how an alert moves through escalation and investigation.

> **SC-200 Exam Note:**
> SOC tiering is an operational model rather than a specific Microsoft framework. For SC-200-related work, understand how analysts use Microsoft Sentinel and Microsoft Defender security alerts and incidents during triage, investigation, response, and escalation.

# Key Terms

* **SOC:** Security Operations Center
* **SOC Tier:** A level of operational responsibility within a SOC
* **Triage:** Initial assessment and prioritization of a security alert
* **Escalation:** Transfer of an alert or incident to an appropriate analyst or team
* **Tier 1:** Initial monitoring and alert triage
* **Tier 2:** Deeper investigation and response
* **Tier 3:** Advanced analysis and investigation
* **Threat Hunting:** Proactive searching for potentially malicious activity
* **DFIR:** Digital Forensics and Incident Response
* **Detection Engineering:** Development and improvement of security detections
* **Incident:** A security event requiring investigation or response

