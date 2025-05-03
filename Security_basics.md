# Security Basics: Confidentiality, Integrity, Availability

The **CIA Triad** is a fundamental model in information security that outlines the three core principles for securing data and systems. These principles are:

1. **Confidentiality**
2. **Integrity**
3. **Availability**

---

## 1. Confidentiality

**Definition:** Ensuring that information is accessible only to those authorized to have access.

**Key Objectives:**

* Prevent unauthorized access to sensitive data.
* Protect against data breaches and leaks.

**Common Controls:**

* Encryption (e.g., AES, RSA)
* Access Control Lists (ACLs)
* Multi-Factor Authentication (MFA)
* Data Classification and Labeling

**Example:**

> Only HR personnel can view employee salary records. Any attempt by unauthorized users is blocked.

---

## 2. Integrity

**Definition:** Maintaining and assuring the accuracy and completeness of data over its entire lifecycle.

**Key Objectives:**

* Prevent unauthorized modification of data.
* Detect and correct improper data changes.

**Common Controls:**

* Hashing (e.g., SHA-256)
* Digital Signatures
* Checksums
* Version Control Systems

**Example:**

> A software update package is validated by comparing its checksum to the published hash before installation.

---

## 3. Availability

**Definition:** Ensuring that authorized users have reliable and timely access to information and resources when needed.

**Key Objectives:**

* Minimize downtime of systems and applications.
* Protect against denial-of-service attacks.

**Common Controls:**

* Redundant Hardware and Failover Systems
* Regular Backups and Disaster Recovery Plans
* Load Balancing
* Network and Application Monitoring

**Example:**

> Critical hospital systems have backup power generators to remain operational during a power outage.

---

## Interrelationships and Trade-offs

* **Balancing Act:** Enhancing one aspect (e.g., confidentiality via strict access controls) may impact availability (e.g., slower access times).
* Organizations must evaluate risk appetite to determine the right balance among the three principles.

---

## Conclusion

The CIA Triad provides a clear framework for designing, assessing, and implementing security measures. By understanding and applying these principles, organizations can better protect their information assets and ensure resilient operations.
