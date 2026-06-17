# Daniel Urgessa - Cybersecurity Portfolio

## Cybersecurity Analyst | CompTIA Security+ Certified  
U.S. Citizen | Eligible for U.S. Secret Security Clearance  
📍 Laurel, MD  

---

## 🔐 About Me
Cybersecurity Analyst with experience in SOC operations, vulnerability assessment, incident response, and threat analysis. Skilled in SIEM tools, security frameworks, and risk-based security decision-making.

---

# Deploy a SIEM Plan Proposal


**NAME:** Daniel Urgessa  
**DATE SUBMITTED:** 12/05/2025  
**STATUS:** Approved

---

## Introduction 
### Hook/Teaser
Ever wondered how attackers slip past endpoint protection? I enhanced my SIEM by integrating Windows Defender logs with Wazuh to catch regsvr32 abuse, credential dumping, and scheduled task persistence—techniques that often evade basic detection.

### Personal Connection
As a cybersecurity pro, I see attackers exploit SIEM vs. endpoint security gaps. This initiative bridges it by uniting Windows Defender's real-time protection with Wazuh's analytics.

### Preview
You'll learn how to: 
* Include the logs for Windows Defender in the Wazuh SIEM. 
* Identify three important MITRE ATT&CK methods (T1218.010, T1003, T1053.005). 
* Build detection rules that catch what traditional monitoring misses.

---

## Setup Story 
### Starting Point 
* **Baseline SIEM state:** Wazuh manager collecting basic Windows Event Logs from ad01.
* **Detection gap:** No insight into real-time Windows Defender protection events.
* **Chosen modification:** Incorporate Windows Defender operational logs (Event IDs 1116, 1117, 2001, 2004).

### Implementation Steps 
**Week 1: Agent Configuration** 1. Verified Wazuh agent status on ad01: `Get-Service WazuhSvc`
2. Modified `ossec.conf` to include Windows Defender log path.
3. Enabled operational logging: `wevtutil sl "Microsoft-Windows-Windows Defender/Operational" /e:true`

**Week 2: Rule Development** 1. Created custom rules for Event IDs 1116/1117.
2. Tested log forwarding with PowerShell simulation.
3. Validated rule triggering in Wazuh dashboard.

### The Mistake: Permission Problems 
* **What went wrong:** Wazuh agent lacked rights to read Defender logs. The agent service kept failing to start, and Event Viewer showed "Access Denied" errors.
* **How I fixed it:** 1. Added the Wazuh service account to the "Event Log Readers" group.
    2. Granted "Log on as a service" rights via Local Security Policy.
    3. Restarted both Wazuh agent and Windows Event Log services.
* **Lesson learned:** Always verify service account permissions before assuming configuration syntax is the problem.

---

## Experiment Time 
| Experiment | Objective | Detection Rate |
| :--- | :--- | :--- |
| **1: Regsvr32 Abuse (T1218.010)** | Detect signed binary proxy execution | 100% |
| **2: Credential Dumping (T1003)** | Catch SAM, LSASS, and cached credentials | 85% |
| **3: Scheduled Task Persistence (T1053.005)** | Distinguish malicious vs. legitimate tasks | 95% |
## 🛠 Hands-On Project Portals
## 🛠️ Hands-On Project Portals

### 🛠 Operational Projects & Dashboards

* **Project 2 (SOC Operations Log Analytics)**
  * Developed a professional [DEPLOY A SIEM Plan Proposal](https://docs.google.com/document/d/1MFeAzZRd2LEjIDgZlJqBle2h6V4VBP-_zbYgqI3TqEg/edit?usp=sharing) by engineering log pipeline metrics across local networks. Configured telemetry streams to route directly into a centralized security dashboard for continuous adversarial tracking using the [MegaQuagga Tool Output Data](https://docs.google.com/spreadsheets/d/1Mc0azxY1Rqq9hlBNejzq-tECjUKKUmBmWES6B3ggOWo/edit?usp=sharing).

* **Project 3 (Infrastructure Baseline Evaluation)**
  * Authored the comprehensive [RCI Analysis (0x2A) Cybersecurity Recommendation Platform](https://docs.google.com/spreadsheets/d/1D0QSnxsNDu0rDSCwaPePFsGlmfcCputjf_quSrmvG7A/edit?usp=sharing). Evaluated business-critical continuity risks, identifying immediate administrative configuration prioritization tasks and infrastructure backup visibility gaps for stakeholders.

* **Project 7 (Nessus Enterprise Vulnerability Scans)**
  * Produced the detailed risk breakdown: [From Security Blind Spots to Actionable Intelligence: 18 Critical Vulnerabilities Discovered with CVSS Scores Up to 9.8](https://docs.google.com/document/d/1KfHFSJnBLheNt9dAbNKX9MyAEKdGlxedP6K8v2S0x1U/edit?usp=sharing). Mapped architectural threat surfaces across domain networks using specialized endpoint vulnerability evaluations.

* **Project 8 (Penetration Testing Reporting Framework)**
  * Engineered a complete asset validation and post-incident investigation layout matching the criteria inside your [IR Triage Report](https://docs.google.com/document/d/1Nqf751s_ZjH7zaFfk9SX5vGeerwFx2sHJZRcOUXNT6c/edit?usp=sharing). Formatted structural response documentation converting dense terminal outputs into remediation workflows.





---

## Final Thoughts
### Coolest Learning
The most fascinating discovery was how Windows Defender's Event ID 1116 provides real-time malware detection context that traditional Sysmon logs miss. 

### Advice for Others 
Start small with one Event ID (1116) before expanding. Test your rules with PowerShell simulations before running actual attack techniques—it saves hours of troubleshooting.

---

## References
1. [Atomic Red Team - T1218.010 Regsvr32](https://github.com)
2. [Windows Defender Event Log Analysis](https://otr.io) (Roberto Rodriguez)
3. [Wazuh Documentation](https://wazuh.com)
4. [MITRE ATT&CK Framework](https://mitre.org)


[View My Resume](Daniel%20Urgessa%20%E2%80%93%20SOC%20Resume.pdf)
If you have any questions or would like to discuss my projects, feel free to reach out via LinkedIn or email me at danielurgessaofficial@gmail.com

If you have any questions or would like to discuss my projects, feel free to reach out via LinkedIn or email me at danielurgessaofficial@gmail.com
If you have any questions or would like to discuss my projects, feel free to reach out via LinkedIn or email me at danielurgessaofficial@gmail.com
---
## 🛠 Projects
- **[SOC Monitoring & Incident Detection](Projects/SOC-Monitoring/README.md):** Enhanced Wazuh SIEM by integrating Windows Defender logs to detect advanced persistence and credential dumping.
- **[Vulnerability Assessment](Projects/Vulnerability-Scan/README.md):** Conducted automated vulnerability scans using Nessus to discover enterprise exposure risks, rank patching priorities, and verify system remediation.

---
## 🎓 Education
- **Ph.D. in Psychology** | California Pacific University, 2025 
- **M.S. Leadership in Homeland Security & Emergency Management** | Grand Canyon University, 2024
 - **B.A. Christian Studies** | Grand Canyon University, 2023
 

---

## 📫 Contact
- Email: danielurgessaofficial@gmail.com  
- LinkedIn: https://www.linkedin.com/in/daniel-urgessa/  
- Location: Laurel, MD  
---

## 🛠 Additional Projects & Reports
* **[Threat Intelligence](./Projects/Threat-Intelligence/)**
* **[Nessus Report](./Reports/Nessus-Report/)**
* **[Incident Response](./Reports/Incident-Response/)**

## 📜 Certifications & Documents
* **[Security+ Certification](./Certifications/SecurityPlus.pdf)**
* **[Daniel Urgessa Resume](./Resume/Daniel-Urgessa-Resume.pdf)**
