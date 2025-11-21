CYART SOC Team – Week 2: Alert Management & Evidence Preservation

Week 2 focuses on real-world SOC operations including alert triage, incident response, and forensic evidence preservation.
All data in this repository is collected from live systems, not templates or simulations.

📌 Learning Outcomes

By the end of Week 2, the analyst completes:

Alert triage using SIEM (Wazuh)

IOC validation using threat intelligence

Forensic evidence collection with Velociraptor

Hashing & integrity verification (SHA256)

Chain of custody documentation

End-to-end incident response

Technical and stakeholder reporting

This repository demonstrates practical SOC analyst skills using industry-standard tools and methods.

📁 Week_2/
├── 📂 1_Alert_Management/
│ └── 📄 Alert classification & prioritization
├── 📂 2_Response_Documentation/
│ └── 📄 IR templates, checklists, post-mortem docs
├── 📂 3_Alert_Triage_Practice/
│ └── 📄 Triage exercises + threat intel validation
├── 📂 4_Evidence_Preservation/
│ ├── 📁 REAL_EVIDENCE/
│ │ ├── 📝 netstat_20251121.txt
│ │ ├── 📝 network_connections.csv
│ │ ├── 📝 process_list.csv
│ │ ├── 📝 systeminfo.txt
│ │ └── 🔐 *.sha256
│ ├── 📄 chain_of_custody.md
│ └── 📄 velociraptor_setup.md
└── 📂 5_Capstone_Project/
├── 📄 incident_report.md
├── 📄 stakeholder_briefing.txt
├── 📄 alert_detection.md
└── 🖼️ screenshots/
🛠 Tools Used
Tool	Purpose
Velociraptor	Forensic evidence collection
Wazuh	Alert detection & triage
Metasploit	Attack simulation
CrowdSec	Automated threat blocking
PowerShell	Windows evidence collection
SHA256	Integrity verification
🧪 Week 2 Tasks (Summary)
Alert Management

Classify alerts, assign priority, and map techniques to MITRE ATT&CK.

Response Documentation

Create incident response templates and documentation used during investigations.

Alert Triage

Analyze alerts, validate IOCs with VirusTotal/OTX, and distinguish true vs. false positives.

Evidence Preservation

Collect volatile data (netstat, processes, system info), calculate hashes, and maintain a complete chain of custody.

Capstone Project

A full incident lifecycle:

Attack (Metasploit vsftpd exploit)

Detection (Wazuh)

Response (CrowdSec)

Investigation & reporting

🔍 Evidence Summary (Collected 2025-11-21)

Real forensic evidence gathered from a Windows host:

netstat_20251121.txt

network_connections.csv

process_list.csv

systeminfo.txt

Corresponding *.sha256 integrity hashes

All evidence is preserved using Velociraptor, documented in chain_of_custody.md.

📄 Deliverables

This repository includes:

Alert triage analysis

Incident response templates

IOC validation results

Forensic findings

Chain of custody documents

Capstone incident report

100-word stakeholder briefing

Screenshots of key investigation steps

Everything is based on real system artifacts and real timestamps.

✔ Verification Checklist

Before submission:

Evidence files validated

SHA256 hashes verified

Chain of custody completed

Screenshots from real investigation

All reports based on actual findings
