# SOC Analyst Knowledge Base

A structured cybersecurity handbook designed to document the knowledge, concepts, tools, and methodologies used by Security Operations Center (SOC) Analysts.

This repository combines theory, practical examples, industry frameworks, and Microsoft security technologies to support continuous learning, interview preparation, and real-world SOC operations.

## Who is this for?

* Aspiring SOC Analysts
* Blue Team professionals
* Cybersecurity students
* Microsoft SC-200 learners
* Threat Hunters
* Detection Engineers

---

# Zero Trust

Zero Trust is a cybersecurity security model based on the principle that users, devices, applications, and network connections should not be trusted automatically.

Instead of assuming that activity is safe because it originates from inside an organization's network, Zero Trust requires access requests to be evaluated and verified.

For a SOC Analyst, Zero Trust is important because identity, device, access, and risk signals can generate security events that require investigation.

---

# Core Principles of Zero Trust

Zero Trust is commonly described through three core principles:

### Verify Explicitly

Authentication and authorization decisions should consider available information such as:

* User identity
* Device state
* Location
* Application
* Sign-in risk
* Other relevant security signals

Authentication alone does not necessarily mean that access should automatically be granted.

### Use Least Privilege Access

Users and systems should receive only the access required to perform their legitimate activities.

Least privilege helps reduce the potential impact of compromised accounts and unauthorized access.

### Assume Breach

Security teams should operate with the assumption that attackers may already have access to part of the environment.

This encourages continuous monitoring, verification, detection, and response rather than relying on a trusted network boundary.

---

# Zero Trust and SOC Operations

Zero Trust generates security signals that can be useful to SOC teams.

Examples include:

* Unusual sign-in activity
* Risky authentication attempts
* Access from unexpected locations
* Non-compliant devices
* Suspicious application access
* Privilege-related activity
* Conditional Access events

A SOC Analyst can investigate these signals by correlating identity, device, authentication, and other security telemetry.

---

# SOC Analyst Perspective

When investigating a Zero Trust-related alert, a SOC Analyst may examine:

* User identity
* Authentication history
* Sign-in location
* Device information
* Device compliance
* Sign-in risk
* Conditional Access results
* Related security alerts
* User activity

The objective is to determine whether the activity is legitimate, suspicious, or malicious.

If malicious activity is confirmed, the analyst follows the organization's incident response procedures and supports appropriate containment and remediation actions.

---

# Real-World Example

An employee attempts to sign in from a new country using an unmanaged device.

Zero Trust policies:

1. Detect the unusual sign-in.
2. Require Multi-Factor Authentication (MFA).
3. Evaluate device compliance.
4. Assess the user's sign-in risk.
5. Block or restrict access if the calculated risk exceeds organizational policy.
6. Generate an alert for the Security Operations Center (SOC).

The SOC Analyst investigates the event by reviewing authentication logs, device information, user activity, and related alerts to determine whether the sign-in is legitimate or malicious.

If the activity is confirmed to be malicious, the analyst escalates the incident, revokes active sessions, resets the user's credentials, and documents the investigation according to the organization's incident response procedures.

---

# Benefits of Zero Trust

Implementing a Zero Trust security model provides several advantages:

* Stronger identity protection
* Reduced attack surface
* Continuous verification of users and devices
* Improved visibility across the environment
* Faster threat detection and response
* Better protection against credential theft
* Reduced impact of compromised accounts
* Support for regulatory and compliance requirements

---

# Summary

Zero Trust replaces implicit trust with continuous verification of users, devices, applications, and access requests.

The model focuses on verifying access explicitly, applying least privilege, and assuming that compromise may already exist within the environment.

For SOC Analysts, Zero Trust provides valuable identity, device, access, and risk telemetry that can support detection, investigation, and incident response.

---

# Key Takeaways

* Do not automatically trust users, devices, applications, or network locations.
* Verify access requests using relevant identity, device, and risk information.
* Apply the principle of least privilege.
* Assume that attackers may already have access to part of the environment.
* Continuously monitor identities, devices, and security activity.
* Zero Trust can improve detection and response capabilities.

---

# Review Questions

1. What is the primary purpose of the Zero Trust security model?
2. What does "verify explicitly" mean?
3. Explain the principle of least privilege.
4. Why does Zero Trust operate under the assumption of breach?
5. What identity and device signals can help a SOC Analyst investigate a Zero Trust alert?
6. Name at least three technologies or security capabilities commonly associated with Zero Trust.
7. How does Zero Trust improve the work of a SOC Analyst?

---

# Further Reading

* Microsoft Zero Trust Guidance
* NIST SP 800-207: Zero Trust Architecture
* Microsoft Security Documentation
* Microsoft Entra ID Documentation

---

# Interview Tip

**Question:** What are the three core principles of Zero Trust?

**Answer:**

The three commonly stated principles are:

* Verify explicitly
* Use least privilege access
* Assume breach

These principles help organizations continuously evaluate access and reduce the potential impact of compromised identities, devices, and applications.

---

# SC-200 Exam Note

Understand how Microsoft Entra ID, Conditional Access, Microsoft Defender XDR, and Microsoft Sentinel can work together to support Zero Trust security operations.

Focus on the relationship between:

**Identity → Device → Risk → Access Control → Detection → Investigation → Response**

Scenario-based questions may require identifying the appropriate security control or interpreting security signals associated with an access attempt.

---

# Key Terms

| Term                              | Meaning                                                                                             |
| --------------------------------- | --------------------------------------------------------------------------------------------------- |
| Zero Trust                        | Security model based on continuous verification rather than implicit trust                          |
| Multi-Factor Authentication (MFA) | Authentication using multiple factors to verify identity                                            |
| Conditional Access                | Policy-based access control that can evaluate users, devices, applications, and risk                |
| Least Privilege                   | Providing only the access required to perform authorized activities                                 |
| Assume Breach                     | Operating on the assumption that compromise may already exist                                       |
| Device Compliance                 | Evaluation of whether a device meets defined security requirements                                  |
| Identity Protection               | Security capabilities used to detect and respond to identity-related risks                          |
| Risk-Based Access                 | Adjusting access decisions based on assessed security risk                                          |
| Sign-In Risk                      | Assessment indicating the likelihood that an authentication attempt may be compromised              |
| Security Telemetry                | Security-related data collected from identities, devices, applications, networks, and other sources |

