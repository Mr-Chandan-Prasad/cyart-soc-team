CYART SOC Team - Week 2
Project Overview
This repository contains Week 2 coursework for SOC (Security Operations Center) training.
Focus: Alert management, incident response, and evidence preservation.

Repository Structure
Week_2 Folder Contains:
3_Alert_Triage_Practice/

alert_triage_simulation.md
threat_intel_validation.txt
README.md

4_Evidence_Preservation/

chain_of_custody.md
velociraptor_setup.md
README.md
REAL_EVIDENCE/

netstat_20251121.txt
network_connections.csv
process_list.csv
systeminfo.txt
*.sha256 (hash files)

5_Capstone_Project/

incident_report.md
stakeholder_briefing.txt
alert_detection.md
response_actions.md
forensic_findings.md
screenshots/
README.md
     

Week 2 Tasks
Task 3: Alert Triage Practice

Simulate triage with sample alerts
Validate IOCs with threat intelligence
Cross-reference with AlienVault OTX and VirusTotal

Tools: Wazuh, VirusTotal, AlienVault OTX
Output: Triage analysis documentation

Task 4: Evidence Preservation

Deploy Velociraptor on Windows system
Collect volatile data (netstat, processes, system info)
Calculate SHA256 hashes for all evidence
Maintain chain of custody documentation

Tools: Velociraptor, PowerShell, SHA256
Evidence Files:

netstat_20251121.txt
network_connections.csv
process_list.csv
systeminfo.txt

Collection Date: 2025-11-21

Task 5: Capstone Project

Simulate attack using Metasploit
Detect attack with Wazuh
Triage and classify alerts
Respond to incident (isolate, block)
Document findings in incident report
Create stakeholder briefing

Tools: Metasploit, Wazuh, CrowdSec
Output:

Incident report (SANS template)
Stakeholder briefing (100 words)
Attack timeline
Response documentation


Evidence Collection Summary
System: Windows Host
Collection Method: PowerShell + Velociraptor
Date: 2025-11-21
Evidence Files Collected:

netstat_20251121.txt - Network connections snapshot
network_connections.csv - Network connections (structured)
process_list.csv - Running processes and memory
systeminfo.txt - System configuration

Hash Verification:

All files hashed with SHA256
Hashes documented in .sha256 files
Integrity verified

Chain of Custody:

Collection timestamp recorded
Collection method documented
Handler documented
Evidence secured and preserved


Tools Used
ToolPurposeVersionVelociraptorEvidence collection0.74.1WazuhAlert detectionLatestMetasploitAttack simulationLatestCrowdSecThreat responseLatestPowerShellEvidence collectionBuilt-inSHA256Hash verificationBuilt-in

How to Use This Repository

Review README files in each folder
Check the REAL_EVIDENCE folder for collected evidence
Review chain of custody documentation
Examine incident reports and findings
Reference screenshots for process documentation


Real Data Only
⚠️ Important: This repository contains REAL data only.

✅ Real evidence from actual system (Windows Host)
✅ Real timestamps (2025-11-21)
✅ Real SHA256 hashes
✅ Real collection methods
❌ No fake data
❌ No templates
❌ No examples


Files Description
chain_of_custody.md

Evidence log table
Collection timeline
Handler documentation
Hash verification records

velociraptor_setup.md

Server installation steps
Client deployment process
Configuration details

incident_report.md

SANS incident report template
Executive summary
Incident timeline
Findings and recommendations

stakeholder_briefing.txt

100-word briefing for non-technical managers
Summary of incident
Actions taken
Business impact

alert_detection.md

Alert information
MITRE ATT&CK techniques
Detection timeline

response_actions.md

Response procedures
System isolation
IP blocking
Verification steps

forensic_findings.md

Investigation findings
Evidence analysis
Conclusions


Submission Details
Due Date: Friday 4:30 PM
What's Included:

Real evidence files with SHA256 hashes
Chain of custody documentation
Incident response reports
Stakeholder briefings
Screenshots and timeline documentation
Velociraptor setup guide


Verification Checklist
Before submission, verify:

 All evidence files are REAL (not examples)
 SHA256 hashes calculated and present
 Chain of custody documented
 Timestamps are accurate
 No fake or template data
 Screenshots show actual output
 Reports based on real findings
 All folders properly organized
 README files present in each folder
