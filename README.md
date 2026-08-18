# SOC Home Lab

> A hands-on cybersecurity lab for learning Security Operations, Wazuh, SIEM monitoring, alert triage, log analysis, incident response, and cyber threat intelligence.

## About This Project

This repository documents my learning journey while building and improving a personal SOC home lab.

The lab is designed to help me understand how security events are collected, monitored, investigated, and documented in a controlled environment.

## Current Focus

- Wazuh deployment and configuration
- SOC and SIEM fundamentals
- Security alert triage
- Linux and Windows log analysis
- Incident investigation and response
- Cyber threat intelligence enrichment
- MITRE ATT&CK technique mapping

## Planned Lab Components

| Component | Purpose |
| --- | --- |
| **Wazuh** | Security monitoring and alert management |
| **Linux agent** | Linux endpoint monitoring and log collection |
| **Windows agent** | Windows event monitoring and analysis |
| **VirusTotal** | Public indicator enrichment |
| **AbuseIPDB** | IP reputation and threat-intelligence enrichment |
| **MITRE ATT&CK** | Understanding adversary tactics and techniques |

## Learning Roadmap

- [ ] Deploy Wazuh manager and dashboard
- [ ] Connect a Linux endpoint
- [ ] Connect a Windows endpoint
- [ ] Learn basic alert triage
- [ ] Analyze authentication and system logs
- [ ] Document the first investigation
- [ ] Add VirusTotal and AbuseIPDB enrichment
- [ ] Create detection notes and queries
- [ ] Map relevant activity to MITRE ATT&CK
- [ ] Document lessons learned

## Investigation Method

For each investigation, I will document:

1. The alert or security question
2. The affected lab system
3. Relevant logs and evidence
4. Analysis and timeline
5. Investigation conclusion
6. Recommended response
7. Detection improvements
8. Lessons learned

## Repository Structure

```text
SOC-home-lab/
├── README.md
├── docs/
├── investigations/
├── detections/
├── cti/
├── scripts/
└── screenshots/
