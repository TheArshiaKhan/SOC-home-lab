SOC Home Lab

An educational home laboratory for learning security monitoring, SIEM concepts, alert triage, log analysis, incident response, and cyber threat intelligence.


This repository documents my legal and controlled cybersecurity learning environment. It is intended for defensive education, reproducible experiments, and professional documentation.

Objectives

This project aims to help me understand how a small SOC operates from an analyst’s perspective. I will gradually learn how to collect security telemetry, review alerts, investigate suspicious activity, connect threat intelligence to observations, and document conclusions clearly.

The main objectives are to:

•
Deploy and understand Wazuh components.

•
Connect authorized Linux and Windows endpoints.

•
Learn how security events are generated, collected, and investigated.

•
Practice alert triage and log analysis using controlled test data.

•
Document basic detection ideas and investigation timelines.

•
Enrich selected indicators with approved public CTI services.

•
Map relevant observed behavior to MITRE ATT&CK where appropriate.

•
Record limitations, false positives, and lessons learned.

Planned Architecture

The lab will be developed in stages:

Component
Purpose
Wazuh manager and dashboard
Central monitoring, alert review, and security analysis
Linux endpoint
Agent deployment and Linux log collection
Windows endpoint
Windows event collection and endpoint monitoring
Analyst workstation
Reviewing alerts, writing notes, and managing the lab
VirusTotal and AbuseIPDB
Optional public indicator enrichment using protected API credentials
GitHub
Version-controlled documentation, scripts, detection notes, and learning history




The architecture will be updated as the lab grows. Screenshots and diagrams will be added only after removing private IP addresses, usernames, hostnames, tokens, and other sensitive information.

Learning Roadmap




Document the lab environment and safety boundaries




Deploy the Wazuh manager and dashboard




Connect an authorized Linux agent




Connect an authorized Windows agent




Review normal logs and establish basic context




Generate safe test events in the lab




Investigate and document the first alert




Practice a repeatable alert-triage process




Add basic detection notes or queries




Add VirusTotal and AbuseIPDB enrichment securely




Write a CTI-informed investigation




Map supported behavior to MITRE ATT&CK




Document false positives and lessons learned




Add tests and lightweight GitHub automation

Repository Structure

Plain Text


.
├── README.md
├── SECURITY.md
├── .gitignore
├── docs/
│   ├── lab-architecture.md
│   ├── setup-notes.md
│   ├── soc-and-siem-concepts.md
│   ├── alert-triage-process.md
│   └── lessons-learned.md
├── investigations/
│   ├── README.md
│   └── case-001-first-alert.md
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
├── diagrams/
└── screenshots/



Investigation Method

Each investigation will use a consistent structure so that another learner can understand the reasoning:

1.
Question: What security question is being investigated?

2.
Scope: Which authorized systems and time period are included?

3.
Alert or trigger: What caused the investigation to begin?

4.
Evidence: Which logs, fields, timestamps, users, processes, or network events are relevant?

5.
Analysis: What does the evidence indicate, and what alternative explanations exist?

6.
Assessment: Is the event benign, suspicious, or malicious within this lab scenario?

7.
Response: What containment, remediation, or monitoring action would be appropriate?

8.
Detection improvement: What rule, query, logging change, or enrichment could help next time?

9.
Limitations: What evidence was unavailable or uncertain?

10.
Lessons learned: What will be improved in the next exercise?

Observed evidence, assumptions, and conclusions will be clearly separated.

CTI Workflow

The CTI portion of the project will focus on using public and authorized information to answer defensive questions. A CTI note may include the intelligence question, source details, indicator type, confidence level, limitations, relevant ATT&CK behavior, and possible defensive use.

External enrichment services will be used carefully. API keys will remain in local environment variables or protected repository secrets. They will never be committed to GitHub. Public indicators will be handled according to the service’s terms and the safety requirements of the lab.

Safety and Ethics

All testing is performed only on systems I own or intentionally authorized training environments. No confidential internship data, course materials, credentials, customer information, private hostnames, personal data, or internal screenshots are stored in this repository.

This repository will not be used to scan, attack, access, or disrupt systems without explicit authorization. Malware samples and dangerous payloads will not be uploaded merely to make the project appear advanced. Synthetic logs, approved training data, screenshots with sensitive details removed, and links to reputable public sources will be preferred.

Current Status

The repository is currently in the planning and initial documentation stage. The next milestone is to document the Wazuh lab architecture and complete the first controlled alert-triage exercise.

Learning Resources

•
Wazuh Documentation

•
MITRE ATT&CK

•
TryHackMe SOC Level 1

•
PortSwigger Web Security Academy

•
GitHub Docs

Disclaimer
This is a personal educational project. It does not contain confidential internship procedures, employer information, or production security data. Technical decisions may change as my understanding and the lab architecture develop.

