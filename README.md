# SOC Home Lab

> A practical cybersecurity home lab focused on Security Operations, Wazuh, SIEM monitoring, alert triage, log analysis, incident response, and cyber threat intelligence.

## About the Project

This repository documents a controlled Security Operations Center (SOC) learning environment.

The purpose of this lab is to understand how security events are collected, processed, monitored, investigated, enriched with threat intelligence, and used to support defensive security decisions.

The project focuses on practical learning through authorized laboratory systems, simulated security events, endpoint telemetry, log analysis, and structured investigation documentation.

## Core Areas

- Security Operations Center (SOC) fundamentals
- Security Information and Event Management (SIEM)
- Wazuh deployment and monitoring
- Security event and log analysis
- Alert triage and investigation
- Wazuh decoders and rule analysis
- Indicators of Compromise (IOCs)
- Linux and Windows endpoint monitoring
- Incident response concepts
- Cyber threat intelligence (CTI)
- VirusTotal and AbuseIPDB enrichment
- MITRE ATT&CK technique mapping
- Security automation and detection improvement

## Lab Architecture

| Component | Role |
| --- | --- |
| **Wazuh Manager** | Collects, processes, and manages security events from authorized endpoints |
| **Wazuh Dashboard** | Provides a central interface for monitoring alerts, events, and security data |
| **Linux Agent** | Collects Linux system, authentication, and security logs |
| **Windows Agent** | Collects Windows event logs and endpoint security telemetry |
| **Analyst Workstation** | Used for investigation, analysis, documentation, and lab administration |
| **VirusTotal** | Provides public intelligence enrichment for selected indicators |
| **AbuseIPDB** | Provides reputation information for selected IP addresses |
| **MITRE ATT&CK** | Helps organize and understand adversary behavior and techniques |

## SOC Workflow

1. **Deployment** – Deploy the monitoring platform and connect authorized lab endpoints.
2. **Monitoring** – Collect and review security events, alerts, and endpoint logs.
3. **Initial Investigation** – Validate alerts and identify the relevant systems, users, timestamps, and evidence.
4. **CTI Enrichment** – Enrich selected indicators using approved public intelligence sources.
5. **Analysis** – Correlate evidence, build a timeline, and determine the likely meaning of the activity.
6. **Escalation** – Escalate serious, suspicious, or confirmed events for deeper investigation.
7. **Incident Response** – Document appropriate containment, remediation, recovery, and follow-up actions.
8. **Automation** – Improve repetitive enrichment, detection, reporting, and analysis workflows.

## Investigation Approach

Each investigation in this lab follows a structured process:

- Define the security question or alert.
- Identify the affected authorized lab system.
- Collect relevant logs and evidence.
- Analyze timestamps, users, processes, network information, and event context.
- Build an investigation timeline.
- Determine whether the activity is benign, suspicious, or malicious within the lab scenario.
- Document recommended response actions.
- Identify detection improvements and lessons learned.

Observed evidence, assumptions, and conclusions are documented separately to support clear and repeatable analysis.

## Repository Structure

```text
SOC-home-lab/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── deployment.md
│   ├── log-analysis.md
│   └── soc-workflow.md
├── investigations/
│   ├── README.md
│   └── case-studies/
├── detections/
│   ├── README.md
│   └── detection-notes.md
├── cti/
│   ├── README.md
│   ├── indicator-enrichment.md
│   └── reports/
├── scripts/
│   ├── README.md
│   └── log-analysis/
└── screenshots/
