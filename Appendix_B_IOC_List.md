# Appendix B: Indicators of Compromise (IOCs)  
**Operation "SIMBA SHIELD" – Kenya Government Domain Intrusions (2025)**  
**Prepared by:** Independent Security Research – Caleb Rutto

---

## 1. Compromised Domains (Partial List)

president.go.ke
health.go.ke
education.go.ke
labour.go.ke
lands.go.ke
environment.go.ke
ict.go.ke
[40+ additional .go.ke domains]


---

## 2. Malicious IP Addresses



192.168.100.1 (Router compromise)
154.236.112.44 (Attack infrastructure)
102.223.45.19 (Cloud proxy node)
185.234.219.72 (SSL enumeration hub)


*Note: Some IPs belong to hosting providers used as disposable staging servers.*

---

## 3. Malicious File Hashes

**Web Shells**



f3a5b3e29cb24c36c0f4819123d049fa shell.php
ac3f22d98172a2ab0bdc99d8e6b19c12 admin_sync.php


**Modified .htaccess Files**



d2c6c7b4ed821a0ce1bf5692b1ca9932


---

## 4. Unauthorized Accounts



sys_maint01
webadmin2
sync-admin
redirect-user


---

## 5. Suspicious DNS Changes



education.go.ke — A record changed to 185.234.219.72
health.go.ke — NS entries modified
president.go.ke — TTL abnormalities detected


---

## 6. Behavioral IOCs

- Simultaneous file changes across >40 servers  
- DNS modifications outside maintenance windows  
- Mass login attempts across unrelated systems  
- Coordinated defacement timestamp (06:00 EAT)  
- SSL certificate anomalies in CT logs  

---

**End of Appendix B**