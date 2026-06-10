# 🛡️ Virtualized Attack & Defense Lab

![Platform](https://img.shields.io/badge/Platform-VirtualBox-blue)
![OS](https://img.shields.io/badge/OS-Kali%20Linux-success)
![Security](https://img.shields.io/badge/Focus-Penetration%20Testing-red)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Overview

This repository documents the creation and operation of a virtualized cybersecurity laboratory designed to simulate real-world attack and defense scenarios. The lab was built to develop practical skills in penetration testing, vulnerability assessment, web application security, privilege escalation, and professional security reporting.

The environment contains intentionally vulnerable systems that allow security practitioners to safely learn, practice, and validate offensive security techniques while understanding defensive remediation strategies.

---

## Table of Contents

* Overview
* Lab Architecture
* Technologies Used
* Environment Setup
* Attack Scenarios
* Vulnerability Findings
* CVSS Risk Assessment
* Sample Penetration Test Reports
* Lessons Learned
* Remediation Strategies
* References
* Disclaimer

---

## Lab Architecture

### Environment Components

| Machine          | Role                         |
| ---------------- | ---------------------------- |
| Kali Linux       | Attacker Machine             |
| Metasploitable 2 | Vulnerable Linux Target      |
| Metasploitable 3 | Enterprise Simulation Target |
| DVWA             | Vulnerable Web Application   |
| VirtualBox       | Virtualization Platform      |

### Network Topology

```text
+------------------+
|   Kali Linux     |
| (Attacker VM)    |
+--------+---------+
         |
         |
---------Virtual Network---------
         |
+--------+---------+
| Metasploitable 2 |
+------------------+

+------------------+
| Metasploitable 3 |
+------------------+

+------------------+
|      DVWA        |
+------------------+
```

---

## Skills Demonstrated

### Offensive Security

* Reconnaissance
* Service Enumeration
* Vulnerability Assessment
* Exploitation
* Post Exploitation
* Privilege Escalation
* Credential Attacks

### Web Application Security

* SQL Injection
* Cross-Site Scripting (XSS)
* Command Injection
* File Inclusion Testing
* Authentication Testing

### Reporting

* CVSS v3.1 Scoring
* Risk Analysis
* Technical Documentation
* Executive Reporting
* Remediation Planning

---

## Tools Used

### Reconnaissance

* Nmap
* Netdiscover
* Gobuster

### Web Security Testing

* Burp Suite
* SQLMap
* Nikto

### Exploitation

* Metasploit Framework
* Hydra
* Netcat

### Privilege Escalation

* LinPEAS
* Linux Exploit Suggester
* Manual Enumeration Techniques

---

## Attack Scenarios

### 1. Network Reconnaissance

#### Objective

Identify live hosts, open ports, and running services.

#### Example

```bash
nmap -sV -sC 192.168.56.0/24
```

#### Learning Outcome

* Service fingerprinting
* OS detection
* Attack surface mapping

---

### 2. SQL Injection

#### Objective

Exploit insecure database queries to access sensitive data.

#### Example Payload

```sql
' OR '1'='1
```

#### Impact

* Authentication bypass
* Database disclosure
* Sensitive information exposure

#### Mitigation

* Parameterized queries
* Input validation
* Least privilege database accounts

---

### 3. Cross-Site Scripting (XSS)

#### Objective

Execute malicious JavaScript within user browsers.

#### Example Payload

```html
<script>alert('XSS')</script>
```

#### Impact

* Session hijacking
* Credential theft
* Defacement

#### Mitigation

* Output encoding
* CSP implementation
* Input sanitization

---

### 4. Brute Force Authentication Attack

#### Objective

Assess password policy effectiveness.

#### Example

```bash
hydra -l admin -P rockyou.txt 192.168.56.101 http-post-form
```

#### Impact

* Unauthorized access
* Credential compromise

#### Mitigation

* MFA
* Account lockout
* Strong password policies

---

### 5. Privilege Escalation

#### Objective

Gain elevated privileges after initial access.

#### Techniques

* Weak sudo permissions
* Misconfigured services
* Vulnerable binaries

#### Example

```bash
sudo -l
```

#### Mitigation

* Principle of Least Privilege
* Regular patching
* Service hardening

---

## Sample Vulnerability Assessment

| Vulnerability        | Severity | CVSS |
| -------------------- | -------- | ---- |
| SQL Injection        | Critical | 9.8  |
| Stored XSS           | High     | 8.8  |
| Weak Credentials     | High     | 8.1  |
| Privilege Escalation | Critical | 9.0  |

---

## Sample Penetration Testing Report Structure

```text
1. Executive Summary

2. Scope

3. Methodology

4. Findings

5. Risk Ratings

6. Evidence

7. Impact Analysis

8. Recommendations

9. Conclusion
```

---

## Screenshots

Create a `/screenshots` folder and include:

* VirtualBox Lab Environment
* Nmap Scan Results
* Burp Suite Interception
* SQL Injection Exploitation
* XSS Demonstration
* Metasploit Sessions
* Privilege Escalation Evidence

Example:

```text
/screenshots
├── virtualbox-lab.png
├── nmap-scan.png
├── sql-injection.png
├── xss-demo.png
├── metasploit-session.png
└── privilege-escalation.png
```

---

## Repository Structure

```text
virtualized-attack-defense-lab/

├── README.md
├── reports/
│   ├── Penetration_Test_Report.pdf
│   ├── Executive_Summary.pdf
│
├── screenshots/
│   ├── nmap-scan.png
│   ├── xss-demo.png
│   └── privilege-escalation.png
│
├── notes/
│   ├── reconnaissance.md
│   ├── sql-injection.md
│   ├── xss.md
│   └── privilege-escalation.md
│
├── diagrams/
│   └── network-topology.png
│
└── LICENSE
```

---

## Key Learning Outcomes

Through this project, I gained practical experience in:

* Penetration Testing Methodologies
* Vulnerability Discovery
* Exploitation Techniques
* Post-Exploitation Activities
* Professional Security Reporting
* Risk Assessment and CVSS Scoring
* Security Control Recommendations

---

## Future Improvements

* Active Directory Lab Integration
* SIEM Monitoring (Splunk)
* Detection Engineering
* Threat Hunting Scenarios
* Purple Team Exercises
* Cloud Security Assessments

---

## References

* OWASP Top 10
* PTES (Penetration Testing Execution Standard)
* MITRE ATT&CK Framework
* NIST Cybersecurity Framework
* CVSS v3.1 Specification

---

## Disclaimer

This repository is intended strictly for educational and authorized security testing purposes. All activities were conducted within isolated virtual environments owned and controlled by the researcher. No unauthorized systems were targeted or affected.

