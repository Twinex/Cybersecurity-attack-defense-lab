# Penetration Test Report

## Executive Summary

A security assessment was conducted against a controlled lab environment containing intentionally vulnerable systems.

The assessment identified multiple critical vulnerabilities including SQL Injection, Cross-Site Scripting, weak authentication controls, and privilege escalation opportunities.

---

## Scope

### In Scope

- DVWA
- Metasploitable 2
- Metasploitable 3

---

## Methodology

- Reconnaissance
- Enumeration
- Vulnerability Assessment
- Exploitation
- Post Exploitation
- Reporting

---

## Findings

### Finding 1: SQL Injection

Severity: Critical

CVSS: 9.8

Description:

Application accepts unsanitized user input resulting in database compromise.

Impact:

- Data disclosure
- Authentication bypass

Recommendations:

- Prepared statements
- Parameterized queries

---

### Finding 2: Stored XSS

Severity: High

CVSS: 8.8

Recommendations:

- Output encoding
- CSP implementation

---

### Finding 3: Weak Credentials

Severity: High

CVSS: 8.1

Recommendations:

- Strong password policy
- MFA

---

## Conclusion

Several critical vulnerabilities were successfully exploited. Immediate remediation is recommended.
