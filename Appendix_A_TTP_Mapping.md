# Appendix A: Detailed TTP Mapping  
**Operation "SIMBA SHIELD" – Kenya Government Domain Intrusions (2025)**  
**Prepared by:** Independent Security Research – Caleb Rutto

---

## MITRE ATT&CK Technique Mapping

This appendix provides a detailed breakdown of all identified attacker behaviors mapped to the MITRE ATT&CK® framework across all phases of the intrusion.

---

## 1. Reconnaissance (PRE-ATT&CK)

| Phase | Technique ID | Technique Name | Evidence |
|-------|--------------|----------------|----------|
| Recon | T1595.002 | Active Scanning: Vulnerability Scanning | Mass scanning of `.go.ke` web servers |
| Recon | T1588.002 | Obtain Capabilities: Tool | Use of custom DNS enumeration tools |
| Recon | T1592 | Gather Victim Host Information | SSL certificate correlation, shared hosting mapping |
| Recon | T1590.001 | Gather Victim Network Information | DNS zone probing, NS delegation enumeration |

---

## 2. Initial Access

| Phase | Technique ID | Technique Name | Evidence |
|-------|--------------|----------------|----------|
| Initial Access | T1133 | External Remote Services | Compromised admin panels |
| Initial Access | T1078.002 | Valid Accounts | Credential reuse across `.go.ke` domains |
| Initial Access | T1190 | Exploit Public-Facing Application | Vulnerable CMS components |

---

## 3. Execution

| Phase | Technique ID | Technique Name | Evidence |
|--------|-------------|---------------|----------|
| Execution | T1059.004 | Command & Scripting Interpreter: Unix Shell | Web shells invoking bash commands |
| Execution | T1204 | User Execution | Phishing-based password capture (suspected) |

---

## 4. Persistence

| Phase | Technique ID | Technique Name | Evidence |
|--------|-------------|---------------|----------|
| Persistence | T1053.005 | Scheduled Task/Job | Unauthorized cron jobs |
| Persistence | T1547 | Boot or Logon Autostart | New service creation |
| Persistence | T1136 | Create Account | Rogue admin accounts created |

---

## 5. Privilege Escalation

| Phase | Technique ID | Technique Name | Evidence |
|--------|-------------|---------------|----------|
| Priv. Esc. | T1068 | Exploitation for Privilege Escalation | CMS privilege bypass |
| Priv. Esc. | T1078 | Valid Accounts | Admin credential reuse |

---

## 6. Defense Evasion

| Phase | Technique ID | Technique Name | Evidence |
|--------|-------------|---------------|----------|
| Defense Evasion | T1562.001 | Disable Security Tools | Logging services modified |
| Defense Evasion | T1027 | Obfuscated Files | Web shell obfuscation |
| Defense Evasion | T1036 | Masquerading | Files disguised as maintenance scripts |

---

## 7. Credential Access

| Phase | Technique ID | Technique Name | Evidence |
|--------|-------------|---------------|----------|
| Credential Access | T1552 | Unsecured Credentials | Plaintext admin creds found in config files |
| Credential Access | T1110 | Brute Force | Automated credential attempts (low volume) |

---

## 8. Lateral Movement

| Phase | Technique ID | Technique Name | Evidence |
|--------|-------------|---------------|----------|
| Lateral Movement | T1021.004 | SSH | SSH pivoting across related systems |
| Lateral Movement | T1080 | Resource Hijacking | Cross-domain session token reuse |

---

## 9. Impact

| Phase | Technique ID | Technique Name | Evidence |
|--------|-------------|---------------|----------|
| Impact | T1491.002 | Website Defacement | Coordinated multi-domain defacement |
| Impact | T1485 | Data Destruction | Limited evidence — controlled, not destructive |
| Impact | T1565.001 | Stored Data Manipulation | Modified `.htaccess` for redirection |

---

**End of Appendix A**
