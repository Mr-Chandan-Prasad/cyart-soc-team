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

## 📁 Repository Structure (Mermaid Diagram)


📁 Week_2 

    A --> B["📂 1_Alert_Management"]:::folder
    B --> B1["📄 Alert classification & prioritization"]:::file

    A --> C["📂 2_Response_Documentation"]:::folder
    C --> C1["📄 IR templates, checklists,<br/>post-mortem docs"]:::file

    A --> D["📂 3_Alert_Triage_Practice"]:::folder
    D --> D1["📄 Triage exercises +<br/>threat intel validation"]:::file

    A --> E["📂 4_Evidence_Preservation"]:::folder

    E --> EA["🧪 REAL_EVIDENCE"]:::evidence
    EA --> EA1["📝 netstat_20251121.txt"]:::file
    EA --> EA2["📝 network_connections.csv"]:::file
    EA --> EA3["📝 process_list.csv"]:::file
    EA --> EA4["📝 systeminfo.txt"]:::file
    EA --> EA5["🔐 *.sha256 files"]:::file

    E --> EB["📄 chain_of_custody.md"]:::file
    E --> EC["📄 velociraptor_setup.md"]:::file

    A --> F["📂 5_Capstone_Project"]:::folder
    F --> F1["📝 incident_report.md"]:::file
    F --> F2["📄 stakeholder_briefing.txt"]:::file
    F --> F3["📊 alert_detection.md"]:::file
    F --> F4["🖼️ screenshots/"]:::folder

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
