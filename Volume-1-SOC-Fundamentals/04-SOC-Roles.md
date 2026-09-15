# SOC Roles

A Security Operations Center (SOC) depends on multiple security roles working together to detect, investigate, respond to, and prevent cyber threats.

Although specific job titles and responsibilities vary between organizations, SOC teams commonly include SOC Analysts, Threat Hunters, Detection Engineers, and SOC Operations management. Specialized security professionals may also work closely with the SOC.

Understanding these roles helps security professionals understand how security operations are organized and how different areas of expertise contribute to incident response.

---

# Why SOC Roles Matter

Cybersecurity operations involve more than monitoring alerts.

Different roles contribute different skills and responsibilities, including:

* Security monitoring
* Alert triage
* Incident investigation
* Incident response
* Threat hunting
* Detection engineering
* Threat intelligence
* Digital forensics
* Security engineering
* SOC operations management

Clear responsibilities help prevent important security activities from being overlooked and allow incidents to be handled by people with the appropriate expertise.

However, responsibilities are not identical across all organizations. A smaller SOC may require analysts to perform several functions, while a larger organization may have dedicated specialists.

---

# Tier 1 SOC Analyst

The Tier 1 SOC Analyst commonly performs the initial monitoring and triage of security alerts.

Typical responsibilities include:

* Monitoring security alerts
* Reviewing SIEM and security platform notifications
* Validating alerts
* Identifying potential false positives
* Collecting initial evidence
* Classifying alerts
* Prioritizing suspicious activity
* Documenting findings
* Escalating incidents when required

The Tier 1 analyst is often the first security professional to examine an alert.

The objective is to establish whether the alert requires further investigation and ensure that relevant information is passed to the appropriate team.

### SOC Analyst Perspective

A Tier 1 analyst should avoid simply closing an alert because it initially appears unusual or benign.

Instead, the analyst should ask:

* What generated the alert?
* Which user or device is involved?
* When did the activity occur?
* What supporting events exist?
* Does the activity match normal behaviour?
* Are there related alerts?
* Does the evidence justify escalation?

Good initial triage provides a strong foundation for further investigation.

---

# SOC Analyst / Tier 2

A SOC Analyst operating at a deeper investigation level commonly handles alerts escalated from initial triage.

Responsibilities may include:

* Performing detailed investigations
* Correlating multiple events
* Reviewing authentication activity
* Examining endpoint activity
* Investigating network activity
* Establishing incident timelines
* Determining the scope of incidents
* Identifying affected users and systems
* Supporting containment
* Coordinating with other security teams
* Escalating complex incidents

The deeper investigation role requires analysts to move beyond individual alerts and understand the broader security event.

For example, a suspicious PowerShell alert may require examination of:

* The parent process
* Child processes
* Command-line activity
* User context
* Network connections
* File activity
* Related endpoint events
* Other systems showing similar behaviour

---

# Threat Hunter

A Threat Hunter proactively searches for malicious or suspicious activity that may not have generated a traditional security alert.

Threat Hunters may:

* Develop hypotheses about attacker behaviour
* Search security telemetry
* Investigate unusual patterns
* Look for indicators of compromise
* Search for known attacker techniques
* Investigate gaps in existing detections
* Identify previously undetected activity
* Collaborate with Detection Engineers
* Contribute findings to incident investigations

Threat hunting is different from traditional alert-driven monitoring because the analyst begins with a question, hypothesis, behaviour, or threat intelligence lead rather than waiting for an alert.

### Example

A Threat Hunter may ask:

> "Are there any endpoints showing suspicious PowerShell activity that has not triggered an existing detection?"

The hunter can then search available telemetry for relevant activity and investigate unusual results.

Threat hunting may be performed by a dedicated team or incorporated into the responsibilities of SOC Analysts and other security professionals.

---

# Detection Engineer

A Detection Engineer develops and improves security detections used to identify suspicious or malicious activity.

Responsibilities may include:

* Developing detection rules
* Writing detection logic
* Creating queries
* Testing detections
* Tuning existing rules
* Reducing false positives
* Mapping detections to attacker techniques
* Monitoring detection effectiveness
* Collaborating with SOC Analysts
* Improving security visibility

Detection Engineering connects security monitoring with practical threat detection.

For example, a Detection Engineer may develop a rule designed to identify suspicious PowerShell behaviour based on known attacker techniques.

The resulting detection can then generate an alert for SOC Analysts to investigate.

### SOC Analyst Perspective

SOC Analysts provide valuable feedback to Detection Engineers.

If analysts repeatedly receive alerts that are legitimate activity, the detection may require tuning.

If analysts identify malicious activity that was not detected, a new or improved detection may be required.

This creates a continuous feedback cycle:

**Detection → Alert → Investigation → Feedback → Detection Improvement**

---

# SOC Operations and Management

SOC Operations management is responsible for coordinating the overall operation of the SOC.

Depending on the organization, management responsibilities may include:

* Coordinating SOC activities
* Establishing operational procedures
* Managing workloads
* Defining escalation processes
* Monitoring operational performance
* Supporting staffing and training
* Coordinating incident response activities
* Managing relationships with other security teams
* Reporting security operations information to management
* Supporting continuous improvement

SOC management may also establish processes for ensuring that incidents are handled consistently and according to organizational requirements.

---

# Specialized Security Roles

A SOC may work closely with specialized security professionals.

Examples include:

### Digital Forensics and Incident Response

DFIR specialists may perform detailed forensic examination and support complex incident response activities.

### Threat Intelligence

Threat Intelligence professionals research information about threats, threat actors, indicators, and attacker behaviour.

Their findings can provide useful context for SOC investigations and threat hunting.

### Security Engineering

Security Engineers may design, implement, and maintain security technologies and controls.

### Malware Analysis

Malware analysts examine suspicious files and malicious software to understand their behaviour and capabilities.

### Security Architecture

Security Architects may design security controls and architectures that reduce organizational risk.

These roles may exist as separate teams or may be combined within smaller security organizations.

---

# How SOC Roles Work Together

SOC roles are most effective when they operate as a coordinated security function.

A simplified workflow may look like:

**Monitoring → Triage → Investigation → Response → Hunting → Detection Improvement**

For example:

1. A security platform generates an alert.
2. A Tier 1 analyst performs initial triage.
3. The alert is escalated for deeper investigation.
4. A SOC Analyst investigates the activity and determines its scope.
5. Incident responders or specialized teams assist with containment when required.
6. A Threat Hunter searches for related activity elsewhere in the environment.
7. A Detection Engineer improves detections based on the findings.
8. The SOC continues monitoring for related activity.

This creates a continuous security operations cycle rather than a single isolated response.

---

# SOC Analyst Perspective

A SOC Analyst should understand the responsibilities of the wider SOC team.

Knowing who performs each function helps an analyst:

* Escalate incidents correctly
* Request appropriate expertise
* Communicate findings clearly
* Understand investigation responsibilities
* Work effectively with Threat Hunters
* Provide useful feedback to Detection Engineers
* Support incident response
* Understand the wider security operation

Security operations depend heavily on communication and collaboration.

A technically strong investigation can still become ineffective if important findings are not documented or communicated to the appropriate team.

---

# Real-World Example

Consider an organization where a workstation generates an alert for suspicious PowerShell activity.

### Tier 1 SOC Analyst

The analyst:

1. Reviews the alert.
2. Identifies the affected endpoint.
3. Identifies the associated user.
4. Reviews the available PowerShell information.
5. Checks related alerts.
6. Determines that the activity requires investigation.
7. Documents the initial findings.
8. Escalates the alert.

### SOC Analyst / Tier 2

The analyst:

1. Reviews the process tree.
2. Examines parent and child processes.
3. Reviews command-line activity.
4. Checks network connections.
5. Searches for related endpoint events.
6. Determines whether other systems are affected.
7. Establishes an incident timeline.
8. Supports containment where required.

### Threat Hunter

The Threat Hunter may search the wider environment for:

* Similar PowerShell activity
* The same command pattern
* Related indicators
* Similar process relationships
* Evidence of lateral movement

### Detection Engineer

The Detection Engineer may then:

* Review the existing detection
* Determine why the activity was detected or missed
* Tune the detection
* Develop additional detection logic
* Map the behaviour to relevant attacker techniques

The result is not only investigation of the individual incident but also improvement of the organization's future detection capability.

---

# SOC Career Progression

SOC career progression can vary significantly between organizations.

A commonly encountered progression is:

**Tier 1 → Tier 2 → Tier 3 / Specialist**

However, this is not a mandatory or universal career path.

Security professionals may move into areas such as:

* Threat Hunting
* Detection Engineering
* DFIR
* Threat Intelligence
* Security Engineering
* Cloud Security
* Security Architecture
* SOC Management

Progression may depend on:

* Technical skills
* Experience
* Certifications
* Organizational structure
* Available positions
* Individual specialization
* Professional development

A SOC Analyst should therefore view the different roles as possible areas of specialization rather than assuming that every security professional must follow exactly the same career path.

---

# Summary

SOC operations depend on multiple roles working together.

Tier 1 SOC Analysts commonly perform monitoring and initial triage. SOC Analysts performing deeper investigations examine alerts in greater detail and determine incident scope.

Threat Hunters proactively search for suspicious activity, while Detection Engineers develop and improve security detections.

SOC Operations management coordinates the wider security operation, while specialized professionals such as DFIR, Threat Intelligence, Malware Analysis, and Security Engineering teams may provide additional expertise.

The exact responsibilities and job titles vary between organizations, but effective communication, escalation, investigation, and collaboration remain important across SOC environments.

---

# Key Takeaways

* SOC teams depend on multiple specialised roles.
* SOC Analysts are responsible for detecting and investigating threats.
* Threat Hunters proactively search for attackers.
* Detection Engineers improve security monitoring.
* Team collaboration is essential for effective incident response.
* SOC responsibilities may vary between organizations.
* Tier 1 commonly focuses on monitoring and initial triage.
* Deeper SOC investigations examine scope, timelines, and supporting evidence.
* Threat Hunting is proactive and may be performed by dedicated teams or SOC Analysts.
* Detection Engineering improves the organization's ability to identify threats.
* Specialized security functions can support complex SOC investigations.

---

# Review Questions

1. What is the role of a Tier 1 SOC Analyst?
2. What makes a Threat Hunter different from a SOC Analyst?
3. What does a Detection Engineer create?
4. Who manages SOC operations?
5. Describe the SOC career progression.

---

# Further Reading

* Microsoft Security Operations Analyst Documentation
* MITRE ATT&CK Framework
* NIST Cybersecurity Framework

> **Interview Tip:**
> Be prepared to explain the responsibilities of a Tier 1 SOC Analyst, Threat Hunter, Detection Engineer, and other SOC roles. Also explain how these roles collaborate during an incident.

> **SC-200 Exam Note:**
> The SC-200 focuses heavily on security operations using Microsoft security technologies. Understand how security analysts work with Microsoft Sentinel and Microsoft Defender to monitor, investigate, respond to, and improve detection of security threats.

# Key Terms

* **SOC:** Security Operations Center
* **SOC Analyst:** Security professional responsible for monitoring, investigating, and responding to security activity
* **Tier 1:** Initial monitoring and alert triage
* **Tier 2:** Deeper security investigation and response
* **Threat Hunter:** Security professional who proactively searches for threats
* **Detection Engineer:** Security professional who develops and improves security detections
* **DFIR:** Digital Forensics and Incident Response
* **Threat Intelligence:** Information used to understand threats, threat actors, indicators, and attacker behaviour
* **SIEM:** Security Information and Event Management
* **EDR:** Endpoint Detection and Response
* **XDR:** Extended Detection and Response
* **Escalation:** Transfer of an alert or incident to an appropriate analyst or team

