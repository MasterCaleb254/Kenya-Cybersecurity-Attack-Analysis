# Appendix C: Defensive Architecture Diagrams  

**Operation "SIMBA SHIELD" – Kenya Government Domain Intrusions (2025)**  
**Prepared by:** Independent Security Research – Caleb Rutto

---

## 1. Zero-Trust Network Architecture (ZTNA) Diagram

                   +----------------------+
                   | Identity Provider IDP|
                   +----------+-----------+
                              |
                Authentication| + MFA
                              |

    +------------+ +------------v-------------+ +-----------+
| User/Host |------>| Zero-Trust Policy Engine |------>| Resources |
+------------+ +------------+-------------+ +-----------+
|
Continuous
Verification

## 2. Centralized Logging & SIEM Pipeline

[Servers] [Routers] [Applications] [Cloud Assets]
\ | | /
\ | | /
----------v--------------v-------------------/
Log Forwarders
|
v
+-----------------------+
| SIEM / Analytics |
| (AI Behavioral Models)|
+----------+------------+
|
Alerts / Dashboards

yaml
Copy code

---

## 3. Decentralized Hosting Model

Before Attack: Recommended Architecture:

Single Hosting Segmented Hosting
+------------+ +-------+ +-------+
| 40 Domains | | 10 | | 10 |
| One Server | | Domains| | Domains|
+------------+ +-------+ +-------+
| |
Independent Failover

yaml
Copy code

---

## 4. National Cyber Range Concept Diagram

+-----------------------------------+
| NATIONAL CYBER RANGE |
| |
| +----------+ +---------------+ |
| | Blue Team| | Red Team APT | |
| +----------+ +---------------+ |
| \ / |
| +-----Simulation-----------+
| Engine |
+-----------------------------------+

yaml
Copy code

---

**End of Appendix C**
