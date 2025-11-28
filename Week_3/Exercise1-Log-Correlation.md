# Exercise 1: Advanced Log Analysis - Task 1: Log Correlation

## Objective
Correlate logs from multiple sources to identify attack patterns linking failed logins with suspicious outbound traffic.

---

## Correlated Events Table

| Timestamp            | Event ID | Source IP      | Destination IP | Notes                          |
|----------------------|----------|----------------|----------------|--------------------------------|
| 2025-11-26 12:00:00  | 4625     | 192.168.1.100  | 192.168.1.50   | Failed login attempt #1        |
| 2025-11-26 12:00:15  | 4625     | 192.168.1.100  | 192.168.1.50   | Failed login attempt #2        |
| 2025-11-26 12:00:30  | 4625     | 192.168.1.100  | 192.168.1.50   | Failed login attempt #3        |
| 2025-11-26 12:01:00  | 4624     | 192.168.1.100  | 192.168.1.50   | Successful login (brute force) |
| 2025-11-26 12:02:00  | 5156     | 192.168.1.50   | 8.8.8.8        | Suspicious DNS query           |
| 2025-11-26 12:03:00  | 5156     | 192.168.1.50   | 185.220.101.50 | Large data transfer (1.5MB)    |

---

## Attack Pattern Analysis

### Timeline Reconstruction
1. **12:00-12:01 (60 seconds):** Attacker from 192.168.1.100 performs brute force attack
   - 3 failed login attempts (Event ID 4625)
   - Successful authentication after 3rd attempt
   
2. **12:02 (1 minute after compromise):** Reconnaissance phase
   - DNS query to external server (8.8.8.8)
   - Likely C2 connectivity check
   
3. **12:03 (2 minutes after compromise):** Data exfiltration
   - Large outbound transfer to 185.220.101.50
   - 1.5MB of data sent over HTTPS (port 443)

### Attack Chain
```
Initial Access → Credential Access → Discovery → Exfiltration
(Brute Force) → (Valid Account)  → (DNS Query) → (C2 Channel)
```

---

## MITRE ATT&CK Mapping

| Phase | Tactic | Technique | Evidence |
|-------|--------|-----------|----------|
| 1 | Credential Access | T1110.001 - Password Guessing | 3 failed logins, 1 success |
| 2 | Initial Access | T1078 - Valid Accounts | Event ID 4624 success |
| 3 | Discovery | T1018 - Remote System Discovery | DNS query to 8.8.8.8 |
| 4 | Exfiltration | T1041 - Exfiltration Over C2 | 1.5MB to 185.220.101.50:443 |

---

## Elasticsearch Query Used
```json
{
  "query": {
    "bool": {
      "should": [
        {"term": {"event.id": 4625}},
        {"term": {"event.id": 4624}},
        {"term": {"event.id": 5156}}
      ],
      "minimum_should_match": 1
    }
  },
  "sort": [{"@timestamp": "asc"}]
}
```

---

## Correlation Logic

**Correlation Rule:**
```
IF (Event 4625 count >= 3 within 2 minutes from same source)
AND (Event 4624 follows within 2 minutes)
AND (Event 5156 to external IP within 5 minutes)
THEN Alert: "Brute Force → Compromise → Exfiltration Chain"
```

---

## Key Findings

✅ **True Positive Identification:** Confirmed attack chain from brute force to data exfiltration  
✅ **Time Delta:** Total attack duration: 3 minutes (extremely fast)  
✅ **IOCs Identified:** 
- Attacker IP: 192.168.1.100
- C2 Server: 185.220.101.50
- Compromised Account: admin
- Compromised Host: 192.168.1.50

---

## Recommendations

**Immediate:**
1. Isolate 192.168.1.50 from network
2. Block 185.220.101.50 at firewall
3. Disable 'admin' account and reset password
4. Review data accessed by compromised account

**Short-term:**
1. Implement account lockout after 3 failed attempts
2. Enable MFA for all administrative accounts
3. Deploy network segmentation
4. Enhance monitoring for Event IDs 4625, 4624, 5156

**Long-term:**
1. Implement behavioral analytics for anomaly detection
2. Deploy deception technology (honeypots)
3. Regular penetration testing
4. Security awareness training

---

**Analyst:** SOC Tier 1  
**Analysis Date:** 2025-11-26  
**Tools Used:** Elasticsearch 7.17.18, Kibana 7.17.18  
**Confidence Level:** HIGH (95%)  
