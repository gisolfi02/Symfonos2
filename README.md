# Symfonos: 2 - Penetration Testing

> Academic penetration testing documentation for the **Symfonos: 2** vulnerable virtual machine, performed in an isolated and authorized laboratory environment.

![Symfonos: 2](Assets/Symfonos2.jpg)

## Overview

This repository contains the documentation and assessment reports produced during a penetration testing activity targeting **Symfonos: 2**, a deliberately vulnerable virtual machine available through VulnHub.

The project was developed for educational purposes to apply the main stages of a structured penetration test, from target discovery and service enumeration to vulnerability validation, controlled exploitation, post-exploitation, privilege escalation, and reporting.

All activities were performed exclusively in a personal, isolated, non-production virtual lab.


## Project Objectives

The assessment aimed to:

- identify the target host within an isolated virtual network;
- discover exposed ports, services, and software versions;
- enumerate network services and accessible resources;
- identify vulnerable software and insecure configurations;
- validate relevant weaknesses through controlled testing;
- obtain initial access to the target;
- perform post-exploitation and privilege escalation activities;
- assess the security impact of the identified weaknesses;
- produce reproducible technical documentation and a structured penetration testing report.

## Laboratory Environment

| Component | Configuration |
|---|---|
| Attacking system | Kali Linux |
| Target system | Symfonos: 2 |
| Hypervisor | Oracle VirtualBox |
| Network type | Isolated Host-Only network |
| Target IP address | `192.168.56.109` |
| Assessment approach | Black-box |
| Initial credentials | None |

The test simulated an attacker connected to the same local network as the target, without initial credentials or prior knowledge of the target configuration.

## Methodology

The activity followed the main phases of the General Penetration Testing Framework:

1. **Target Scoping**: definition of scope, rules of engagement, and objectives.
2. **Information Gathering**: collection of publicly available and initial target-related information.
3. **Target Discovery**: identification of the target host in the virtual network.
4. **Enumeration**: identification of open ports, exposed services, software versions, and relevant configurations.
5. **Vulnerability Mapping**: correlation of discovered services with known vulnerabilities and insecure configurations.
6. **Target Exploitation**: controlled validation of exploitable weaknesses to obtain initial access.
7. **Post-Exploitation**: local enumeration, internal-service analysis, and privilege escalation.
8. **Documentation and Reporting**: creation of technical evidence and final assessment reports.

## Assessment Outcome

The activity demonstrated that the target could be fully compromised through a chain of vulnerabilities and insecure configurations. The final assessment classified the overall security risk as **Critical**, because an initially unauthenticated attacker could ultimately obtain administrative control of the virtual machine.

The complete technical chain, supporting evidence, impact assessment, and remediation recommendations are documented in the reports available below.

## Available Documentation

| Document | Description |
|---|---|
| [Reproducibility Document](Docs/Documento_di_Replicabilit%C3%A0.pdf) | Full technical documentation including methodology, commands, outputs, screenshots, and the complete assessment workflow. |
| [Penetration Testing Report](Docs/Penetration_Testing_Report.pdf) | Management-oriented report containing the Executive Summary, Engagement Highlights, Vulnerability Report, Remediation Report, Findings Summary, and Detailed Summary. |
| [Nessus Basic Network Scan](Reports/Nessus_Basic_Scan.pdf) | Nessus report covering network services, exposed configurations, and vulnerability scan results. |
| [Nessus Web Application Scan](Reports/Nessus_Web_Application_Scan.pdf) | Nessus report focused on the web application attack surface exposed by the target. |

## Repository Structure

```text
.
├── Assets/
│   └── Symfonos2.jpg
│
├── Docs/
│   ├── Documento_di_Replicabilità.pdf
│   └── Penetration_Testing_Report.pdf
│
├── Reports/
│   ├── Nessus_Basic_Scan.pdf
│   └── Nessus_Web_Application_Scan.pdf
│
├── LICENSE
└── README.md
```

## Tools Used

The following tools were used during the assessment:

- Kali Linux
- Nmap
- arp-scan
- arping
- p0f
- Unicornscan
- smbclient
- Netcat
- Gobuster
- Nikto
- Nessus
- Searchsploit
- John the Ripper
- Metasploit Framework
- snmpwalk
- SSH and SCP

## Ethical Notice

This repository is intended **solely for educational and training purposes**.

The procedures documented here were performed against a deliberately vulnerable machine in an isolated environment owned and controlled by the author. Do not apply the described techniques to systems, networks, or services without explicit authorization from their owner.

## License

This repository is distributed under the terms specified in the [LICENSE](LICENSE) file.
