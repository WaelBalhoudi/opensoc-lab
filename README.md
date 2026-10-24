# OpenSOC Lab — Network Defense & Threat Detection

**Build. Monitor. Detect. Investigate.**

OpenSOC Lab is a hands-on cybersecurity lab designed to demonstrate network defense, intrusion detection, centralized security monitoring, and incident investigation in an isolated virtual environment.

The project integrates **pfSense**, **Suricata IDS**, and **Wazuh SIEM** to explore how security tools work together to monitor network activity, detect suspicious behavior, collect endpoint logs, and support incident response.

> **Project status:** In development

## Objectives

- Configure firewall rules and network segmentation using pfSense.
- Deploy Suricata to detect suspicious network traffic.
- Centralize and analyze security events using Wazuh.
- Collect and investigate Linux and Windows endpoint logs.
- Run controlled security tests in an isolated lab.
- Document alerts, findings, and remediation recommendations.

## Architecture

The planned environment consists of a firewall, an IDS sensor, a SIEM platform, and test endpoints.

```text
              Isolated Test Environment
                         |
                      [Kali VM]
                         |
                    [pfSense]
                         |
                Internal Lab Network
                         |
            +------------+------------+
            |            |            |
        [Wazuh SIEM] [Linux Host] [Windows Host]
            |
      Alerts & Dashboards
```

*This is a conceptual overview. The final topology and Suricata sensor placement will be documented after implementation and testing.*

## Technology Stack

| Component | Purpose |
|---|---|
| pfSense | Firewall and network traffic control |
| Suricata | Network intrusion detection |
| Wazuh | Security event collection, analysis, and alerting |
| Linux | Server logging and security monitoring |
| Windows | Endpoint logging and monitoring |
| VMware Workstation | Virtual lab environment |

## Planned Security Tests

- **SSH authentication testing:** Generate controlled failed-login events and validate detection.
- **Web traffic testing:** Generate controlled traffic against a lab web service and examine the resulting logs and alerts.
- **Detection validation:** Compare generated activity with firewall logs, Suricata events, and Wazuh alerts.
- **Incident investigation:** Document evidence, analysis, and recommended remediation.

All tests will run only against authorized lab systems in an isolated environment.

## Repository Structure

```text
OpenSOC-Lab/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── network-design.md
│   └── detection-matrix.md
├── configs/
│   ├── pfsense/
│   ├── suricata/
│   └── wazuh/
├── tests/
│   ├── ssh-authentication/
│   └── web-traffic/
├── reports/
├── screenshots/
└── LICENSE
```

*Directories and files will be added as the project progresses.*

## Implementation Roadmap

- [ ] Phase 1 — Prepare the lab environment and verify host connectivity.
- [ ] Phase 2 — Design and validate the virtual network.
- [ ] Phase 3 — Configure pfSense firewall rules.
- [ ] Phase 4 — Deploy and validate Suricata.
- [ ] Phase 5 — Deploy Wazuh and connect endpoint agents.
- [ ] Phase 6 — Generate controlled test events and validate detections.
- [ ] Phase 7 — Write incident reports and document results.

## Expected Deliverables

- Network architecture and IP addressing documentation.
- Sanitized configuration examples.
- Screenshots of verified dashboards and security alerts.
- Detection test results and incident reports.
- Setup instructions and troubleshooting notes.

## Disclaimer

This repository is intended for educational and defensive cybersecurity purposes. Security testing must be restricted to systems you own or have explicit permission to test. Attack simulations must remain within the isolated lab environment.

## Project Status

OpenSOC Lab is under active development. Planned features will be marked as completed only after they have been implemented and validated.
