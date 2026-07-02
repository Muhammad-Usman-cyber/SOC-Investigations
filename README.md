# SOC Investigation Writeups 🔍

> Real-world SOC investigations completed as part of the **TryHackMe SOC Level 1 Learning Path** (65 hours 29 minutes) — completed 17th June 2026.

[![TryHackMe](https://img.shields.io/badge/TryHackMe-Top%201%25-red?style=flat&logo=tryhackme)](https://tryhackme.com/p/muhammadusman.khurram2007)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/muhammad-usman-cyber)
[![Portfolio](https://img.shields.io/badge/Portfolio-GitHub-black?style=flat&logo=github)](https://github.com/Muhammad-Usman-cyber/Portfolio)

---

## About This Repository

This repository contains detailed writeups of four capstone SOC investigations from the TryHackMe SOC L1 pathway. Each investigation simulates a real-world incident response scenario requiring full triage, log analysis, threat hunting, and MITRE ATT&CK mapping.

These are not guided tutorials — they are independent investigations conducted using professional SOC analyst methodology and tooling.

---

## Investigations

| # | Case | Difficulty | Status |
|---|------|------------|--------|
| 01 | [Tempest](#-tempest) | ⚡ Medium | ✅ Complete |
| 02 | [Boogeyman 1](#-boogeyman-1) | ⚡ Medium | ✅ Complete |
| 03 | [Boogeyman 2](#-boogeyman-2) | 🔥 Hard | ✅ Complete |
| 04 | [Boogeyman 3](#-boogeyman-3) | 🔥 Hard | ✅ Complete |

---

## Tools Used Across Investigations

| Category | Tools |
|----------|-------|
| **Email Analysis** | Thunderbird, Olevba |
| **Log Analysis** | EvtxEcmd, Timeline Explorer, SysmonView, Event Viewer |
| **Memory Forensics** | Volatility |
| **Network Analysis** | Wireshark, Elastic Stack |
| **Endpoint Monitoring** | Sysmon Logs, Native Windows Utilities |
| **File Analysis** | LNKParse3, Strings, md5sum |
| **Data Processing** | jq, grep, sed, Base64 |
| **Threat Simulation** | Mimikatz |

---

## 🔵 Tempest

**Scenario:** Investigation of a suspected network intrusion involving malicious traffic, threat actor C2 communication, and data exfiltration indicators.

**Key Skills Demonstrated:**
- Network traffic analysis using Wireshark
- Identifying C2 communication patterns
- IOC extraction and threat intelligence correlation
- MITRE ATT&CK technique mapping

**Primary Tools:** Wireshark, Elastic Stack, grep, jq

**MITRE ATT&CK Techniques Identified:**

| Technique ID | Technique Name |
|-------------|----------------|
| T1071 | Application Layer Protocol |
| T1041 | Exfiltration Over C2 Channel |
| T1082 | System Information Discovery |

---

## 🔵 Boogeyman 1

**Scenario:** Investigation of an initial access event via phishing email containing a malicious attachment leading to endpoint compromise.

**Key Skills Demonstrated:**
- Phishing email analysis using Thunderbird
- Malicious document analysis with Olevba
- Windows Event Log investigation with EvtxEcmd
- LNK file forensics with LNKParse3
- Process execution chain reconstruction

**Primary Tools:** Thunderbird, Olevba, LNKParse3, EvtxEcmd, Timeline Explorer, Event Viewer

**MITRE ATT&CK Techniques Identified:**

| Technique ID | Technique Name |
|-------------|----------------|
| T1566.001 | Phishing — Spearphishing Attachment |
| T1059 | Command and Scripting Interpreter |
| T1547 | Boot or Logon Autostart Execution |
| T1204 | User Execution |


---

## 🔴 Boogeyman 2

**Scenario:** Extended investigation covering post-exploitation activity including lateral movement, persistence mechanisms, and credential access following initial compromise.

**Key Skills Demonstrated:**
- Sysmon log analysis using SysmonView
- Timeline reconstruction with Timeline Explorer
- Credential dumping detection — Mimikatz indicators
- Lateral movement path identification
- String analysis of malicious binaries

**Primary Tools:** SysmonView, Timeline Explorer, Sysmon Logs, Strings, md5sum, Native Windows Utilities

**MITRE ATT&CK Techniques Identified:**

| Technique ID | Technique Name |
|-------------|----------------|
| T1003 | OS Credential Dumping |
| T1021 | Remote Services — Lateral Movement |
| T1053 | Scheduled Task Persistence |
| T1112 | Modify Registry |
| T1070 | Indicator Removal |


---

## 🔴 Boogeyman 3

**Scenario:** Full attack chain investigation from initial phishing through to memory forensics, covering the complete lifecycle of an advanced threat actor operation.

**Key Skills Demonstrated:**
- Memory forensics using Volatility
- Full attack timeline reconstruction
- Base64 encoded payload decoding
- Advanced log correlation across multiple sources
- Complete attack chain documentation

**Primary Tools:** Volatility, EvtxEcmd, Base64, grep, sed, Timeline Explorer, Elastic Stack

**MITRE ATT&CK Techniques Identified:**

| Technique ID | Technique Name |
|-------------|----------------|
| T1055 | Process Injection |
| T1027 | Obfuscated Files or Information |
| T1083 | File and Directory Discovery |
| T1005 | Data from Local System |
| T1041 | Exfiltration Over C2 Channel |


---

## Investigation Methodology

Every investigation in this repository follows this structured SOC analyst approach:

```
1. TRIAGE
   └── Read scenario, identify scope, define investigation questions

2. LOG COLLECTION
   └── Identify relevant log sources — Windows Events, Sysmon, Network, Email

3. TIMELINE RECONSTRUCTION
   └── Build chronological attack timeline from multiple log sources

4. THREAT HUNTING
   └── Hunt for IOCs, suspicious processes, anomalous network connections

5. MITRE ATT&CK MAPPING
   └── Map all attacker actions to ATT&CK tactics and techniques

6. DOCUMENTATION
   └── Write structured findings report with evidence and recommendations
```

---

## Key Takeaways

**What these investigations taught me:**

- Real SOC investigations require correlating evidence across multiple log sources simultaneously — no single log tells the full story
- Attackers consistently try to blend into normal traffic and processes — knowing what normal looks like is as important as knowing what malicious looks like
- MITRE ATT&CK is not just a framework to memorize — it is a live reference that guides your hunting logic during active investigations
- Timeline reconstruction is the foundation of every good incident report — without a clear timeline you cannot understand the full attack scope
- Tools are only as useful as the analyst using them — methodology and thinking process matter more than tool knowledge

---


## Coming Soon

| Project | Description | Status |
|---------|-------------|--------|
| Home SIEM Lab | Built personal detection lab using Elastic SIEM | 🔄 In Progress |
| Phishing Analysis Report | Real phishing sample analysis with IOC extraction | 📅 Planned |
| Threat Intelligence Report | APT threat actor profile with full ATT&CK mapping | 📅 Planned |
| IR Playbook | Professional incident response playbook for ransomware | 📅 Planned |

---

## Connect

- 🌐 **Main Portfolio:** [github.com/Muhammad-Usman-cyber](https://github.com/Muhammad-Usman-cyber/Portfolio)
- 💼 **LinkedIn:** [muhammad-usman-cyber](https://www.linkedin.com/in/muhammad-usman-cyber)
- 🎯 **TryHackMe:** [muhammadusman.khurram2007](https://tryhackme.com/p/muhammadusman.khurram2007)
- 📧 **Email:** [muhammadusman.khurram2007@gmail.com](mailto:muhammadusman.khurram2007@gmail.com)

---

*SOC L1 Learning Path completed 17th June 2026 — 65 hours 29 minutes | TryHackMe Top 1% Globally*

