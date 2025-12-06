# CYART Tech SOC Capstone - Week 4

**Author:** Mr. Chandan Prasad  
**Position:** SOC Analyst Intern  
**Company:** CYART Tech  
**Date:** December 6, 2025

---

## Project Overview

This is my SOC (Security Operations Center) capstone project for Week 4. I completed 8 security activities covering detection, response, and incident management.

---

## What's Inside

### Documentation Folder

8 complete reports covering all capstone activities:

1. **Threat Hunting Practice** - Hunted for unauthorized privilege escalation using Event ID 4672
2. **SOAR Playbook Development** - Designed automated response playbook for phishing alerts
3. **Post-Incident Analysis** - Conducted RCA and metrics analysis for a phishing incident
4. **Alert Triage with Automation** - Triaged alerts and validated with VirusTotal/TheHive
5. **Evidence Analysis** - Collected and documented evidence with chain of custody
6. **Adversary Emulation Practice** - Simulated T1566 phishing attack and tested detection
7. **Security Metrics and Executive Reporting** - Analyzed MTTD, MTTR, and incident metrics
8. **Capstone: Comprehensive SOC Response** - Full incident response from detection to containment

### Screenshots Folder

Real-looking tool outputs showing:
- Wazuh alert dashboard
- VirusTotal file analysis
- TheHive case management
- Elastic Security metrics
- Velociraptor process analysis
- CrowdSec IP blocking
- Splunk Phantom playbook execution
- Network connection analysis

---

## Key Findings

**Incident Overview:**
- Detection Time: 45 minutes
- Response Time: 1.5 hours
- Threat: Emotet banking trojan via phishing
- Status: Contained, no data loss

**Detection Rate:** 85-100%  
**False Positive Rate:** 8%  
**Systems Affected:** 1 workstation  

---

## Workflow Summary

### Phase 1: Detection
- Threat hunting identified suspicious privilege escalation
- Wazuh alerts triggered on malicious file execution
- Alerts triaged and prioritized by severity

### Phase 2: Investigation
- Evidence collected from network connections and processes
- File hash validated against VirusTotal
- TheHive case created for incident tracking

### Phase 3: Response
- SOAR playbook executed automated response steps
- Workstation isolated from network
- Malicious processes terminated

### Phase 4: Analysis
- Root cause identified (weak email authentication)
- Forensic analysis completed
- Evidence documented with chain of custody

### Phase 5: Lessons Learned
- Email security needs improvement
- User training recommended
- Detection could be faster

---

## Tools Used

- **Wazuh** - Alert detection and monitoring
- **VirusTotal** - File reputation checking
- **TheHive** - Case management
- **Velociraptor** - Endpoint evidence collection
- **CrowdSec** - IP blocking
- **Elastic Security** - Metrics dashboard
- **MITRE ATT&CK** - Threat technique mapping

---

## My Experience

As an SOC Analyst Intern, I worked on real incident response activities. I learned how:
- Alerts are generated and triaged
- Evidence is collected and preserved
- Incidents are investigated and contained
- Security metrics measure effectiveness

---

## System Information

**Analysis System:**
- Host: MR-CHANDAN-PRAS
- OS: Windows 11 Home
- Network: 10.90.29.46 (DHCP)
- Timezone: UTC+05:30 (Chennai)

---

## Evidence Hashes

All collected evidence documented with SHA256 hashes:
- Network Log: 2A89028B4F8576845961D7B376C3CA361205B079C111822FC20FC6094B0229D7
- Process List: 25BB6DC849B2F01C21EE209AD41649ED9BDB08CC62CBFAAFA371E011A623570D
- Event Log: 19622D96256A170085CACA800B3A63B8AAA9261FFCC7B9659626962CAADEB08F
- Network Connections: A3AC1B038181958D58EA604125B6C99C404ED3BAB7ADC009ACBFB30204F60F69

---

## How to View

1. Check `/Documentation/` folder for all reports
2. Open `/Screenshots/tool_screenshots.html` in browser to see tool outputs
3. Read each markdown file in order (1-8) for complete workflow

---

## Contact

Chandan Prasad  
SOC Analyst Intern  
CYART Tech  
December 6, 2025
