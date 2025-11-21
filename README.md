CYART SOC Team - Week 2: Alert Management & Evidence Preservation
📋 Project Overview
This repository contains hands-on, real-world practice for Security Operations Center (SOC) professionals focusing on alert management, incident response, and evidence preservation.
What's Inside:

Real alert triage and prioritization
Practical evidence collection with hashing
Full incident response workflows
Forensic analysis documentation
Chain of custody procedures


🎯 Learning Objectives
By completing this course, you will:

✅ Triage and prioritize security alerts effectively
✅ Collect forensic evidence using industry-standard tools
✅ Calculate and verify SHA256 hashes
✅ Maintain proper chain of custody
✅ Respond to incidents from detection to resolution
✅ Document findings for legal proceedings
✅ Create incident reports for stakeholders


📁 Repository Structure
cyart-soc-team/
├── Week_2/
│   ├── 1_Alert_Management/
│   │   └── [Alert classification and prioritization exercises]
│   │
│   ├── 2_Response_Documentation/
│   │   └── [Incident templates and procedures]
│   │
│   ├── 3_Alert_Triage_Practice/
│   │   └── [Mock alert analysis with threat intelligence]
│   │
│   ├── 4_Evidence_Preservation/
│   │   ├── REAL_EVIDENCE/
│   │   │   ├── netstat_20251121.txt
│   │   │   ├── network_connections.csv
│   │   │   ├── process_list.csv
│   │   │   ├── systeminfo.txt
│   │   │   └── *.sha256 (hash verification files)
│   │   ├── chain_of_custody.md
│   │   ├── velociraptor_setup.md
│   │   └── README.md
│   │
│   ├── 5_Capstone_Project/
│   │   ├── incident_report.md
│   │   ├── stakeholder_briefing.txt
│   │   ├── alert_detection.md
│   │   └── screenshots/
│   │
│   └── README.md (this file)

🛠️ Tools Used
ToolPurposeVersionVelociraptorEvidence collection agent0.74.1WazuhAlert detection & managementLatestMetasploitAttack simulationLatestCrowdSecThreat response & blockingLatestFTK ImagerForensic imaging (optional)LatestPowerShellWindows evidence collectionBuilt-insha256sumHash verificationBuilt-in

🚀 Quick Start
Week 2 Exercises
1. Alert Management (Days 1-2)
Goal: Learn to classify and prioritize alerts
Tasks: Create classification system, use MITRE ATT&CK mapping
Output: Alert dashboard, prioritization matrix
2. Response Documentation (Days 2-3)
Goal: Document incident response procedures
Tasks: Create templates, checklists, post-mortem docs
Output: Incident response templates in Google Docs
3. Alert Triage (Days 3-4)
Goal: Analyze alerts and validate IOCs
Tasks: Simulate alerts, cross-reference with threat intel
Tools: Wazuh, AlienVault OTX, VirusTotal
Output: Triage analysis with threat intel findings
4. Evidence Preservation (Days 4-5)
Goal: Collect evidence forensically
Tasks: Deploy Velociraptor, collect netstat, hash evidence
Tools: Velociraptor, PowerShell, SHA256
Output: REAL evidence files with chain of custody
5. Capstone Project (Days 5)
Goal: Full incident response cycle
Tasks: Attack simulation → Detection → Response → Reporting
Tools: Metasploit, Wazuh, CrowdSec
Output: Incident report + stakeholder briefing
