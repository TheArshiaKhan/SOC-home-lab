# SOC Home Lab

> A practical cybersecurity home lab focused on Security Operations, Wazuh, SIEM monitoring, endpoint log analysis, detection engineering, incident response, cyber threat intelligence and SOAR automation.

## About This Repository

This repository documents a controlled Security Operations Center (SOC) learning environment built for authorized laboratory practice.

The lab is organized into three connected projects. The first project establishes the Wazuh and SOC foundation. The second project focuses on Windows and Linux endpoint monitoring and log analysis. The third project develops an automated SOAR and CTI workflow using Wazuh, Shuffle, TheHive, VirusTotal, and AbuseIPDB.

The purpose of this repository is to understand how security alerts move from detection to enrichment, investigation, case creation, analyst review, and recommended response.

## Project Overview

| Project | Main Focus | Technologies |
| --- | --- | --- |
| **Project 1: Wazuh SOC Foundation** | Wazuh deployment, SOC and SIEM concepts, event analysis, logs, decoders, rules, alerts, and IOCs | Wazuh, SIEM, decoders, detection rules |
| **Project 2: Endpoint Log Ingestion and Analysis** | Windows and Linux agent installation, log ingestion, endpoint monitoring, and event analysis | Wazuh agents, Windows Event Logs, Linux logs |
| **Project 3: SOAR and CTI Automation** | Automated alert processing, IOC enrichment, TheHive case creation, workflow testing, and error handling | Wazuh, Shuffle, TheHive, VirusTotal, AbuseIPDB |

---

## Project 1: Wazuh SOC Foundation

### Purpose

This project establishes the foundation of the home SOC and focuses on understanding how Wazuh supports security monitoring, event analysis, alert triage, and investigation.

### Main Learning Areas

- Wazuh manager and dashboard deployment
- SOC and SIEM concepts
- Security event and log analysis
- Alert generation and alert triage
- Wazuh decoders and rule logic
- Indicators of Compromise (IOCs)
- True-positive and False-positive
- Detection rule analysis
- Custom detection rule development
- False-positive review
- Investigation documentation

### Detection Engineering

Detection engineering includes understanding existing Wazuh rules, reviewing rule logic, analyzing false positives, and creating new rules for authorized laboratory events.

The detection process includes:

1. Identify a behavior that should be detected.
2. Review the available log source and event fields.
3. Understand the relevant decoder and existing rule logic.
4. Create or modify a detection rule in the authorized lab.
5. Test the rule with safe and controlled events.
6. Review the generated alert.
7. Check for false positives and missing context.
8. Document the rule purpose, severity, evidence, and limitations.
9. Map the behavior to MITRE ATT&CK when appropriate.

---

## Project 2: Endpoint Log Ingestion and Analysis

### Purpose

This project focuses on monitoring authorized Windows and Linux endpoints with Wazuh agents and analyzing the logs collected from those systems.

### Windows Monitoring

Windows monitoring focuses on collecting and analyzing security-relevant Windows events, including authentication activity, account changes, process activity, system events, and other authorized endpoint telemetry.

### Linux Monitoring

Linux monitoring focuses on collecting and analyzing authentication, system, service, and security logs from authorized Linux endpoints.

### Endpoint Log Ingestion Workflow

1. Install and configure the authorized Wazuh agent.
2. Connect the agent to the Wazuh manager.
3. Confirm that the agent is communicating correctly.
4. Configure the appropriate Windows or Linux log sources.
5. Generate or observe safe laboratory events.
6. Confirm that events are ingested by Wazuh.
7. Analyze the decoder, rule, alert, and event fields.
8. Document the investigation and detection result.

### Endpoint Analysis Areas

- Successful and failed authentication events
- Account and privilege changes
- Suspicious process activity
- SSH-related events
- Windows Event Logs
- Linux authentication and system logs
- Service and system activity
- File and process monitoring
- Alert severity and event context

---

## Project 3: SOAR and CTI Automation

### Purpose

This project develops an automated Security Orchestration, Automation, and Response (SOAR) workflow for processing Wazuh alerts, extracting observables, enriching indicators with public CTI services, creating TheHive cases, and supporting analyst review.

### Main Components

| Component | Role |
| --- | --- |
| **Wazuh** | Generates and sends security alerts |
| **Shuffle** | Receives alerts and orchestrates the automation workflow |
| **VirusTotal** | Enriches supported indicators with public reputation and analysis data |
| **AbuseIPDB** | Enriches IP addresses with abuse and reputation information |
| **TheHive** | Creates and manages investigation cases |
| **Analyst** | Reviews results and makes the final investigation decision |

### SOAR and CTI Workflow

The final workflow follows this sequence:

```text
Wazuh Alert
    ↓
Shuffle Webhook / Trigger
    ↓
Extract IOC / Observable
    ↓
Automated IOC Enrichment
    ↓
Evaluate Enrichment Results
    ↓
Assign Preliminary Classification + Severity
    ↓
Create TheHive Case when Criteria Are Met
    ↓
Add Wazuh Alert + IOC + Enrichment + Findings to Case
    ↓
Analyst Review
    ↓
Final True Positive / False Positive Decision + Recommended Response

SOC-home-lab/
├── README.md
│
├── projects/
│   ├── 01-wazuh-soc-foundation/
│   │   └── README.md
│   │
│   ├── 02-endpoint-log-ingestion/
│   │   └── README.md
│   │
│   └── 03-soar-cti-automation/
│       └── README.md
│
├── investigations/
│   └── README.md
│
├── detections/
│   └── README.md
│
├── diagrams/
├── screenshots/
└── .gitignore
