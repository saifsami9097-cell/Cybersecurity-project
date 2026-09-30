## NS-001 — Network Traffic Analysis Using Wireshark

**Domain:** Network Security & Traffic Analysis
**Environment:** Kali Linux VM / VMware
**Tool:** Wireshark
**Project Type:** Cybersecurity Internship — Week 2

### Objective

To capture, filter, and analyze network traffic using Wireshark and understand the behavior of common network protocols.

### Protocols Analyzed

* DNS
* TCP
* UDP
* ICMP
* HTTP

### Practical Work

The project included:

* Network packet capture using Wireshark
* DNS query and response analysis
* TCP three-way handshake analysis
* UDP traffic analysis
* ICMP Echo Request and Reply analysis
* HTTP traffic inspection
* Source/destination IP and port analysis
* Security risk identification
* MITRE ATT&CK mapping

### Evidence

**Screenshots:**
`Screenshots/NS-001/`

**Evidence files:**
`Evidence/NS-001/`

### Documentation

**Report:**
`Documentation/NS-001_Network_Traffic_Analysis_Report.pdf`

### Key Learning

This project provided practical experience in packet capture, protocol analysis, network monitoring, and basic network-security assessment using Wireshark.


## NS-002 – Nessus Vulnerability Assessment

**Target:** Metasploitable (`192.168.52.129`)  
**Scanner:** Kali Linux + Nessus Essentials  
**Scan Policy:** Basic Network Scan

### Assessment Results

The Nessus assessment identified multiple vulnerabilities in the
intentionally vulnerable Metasploitable system.

| ID | Finding | Severity | CVSS | CVE |
|------|---|---|---:|---|
| VUL-001 | Canonical Ubuntu Linux 8.04.x End of Life | Critical | 10.0 | N/A |

### Evidence

Detailed findings, verification results, screenshots, and remediation
recommendations are documented in:

`Documentation/NS-002_Vulnerability_Assessment_Report.md`

Evidence:

`Evidence/NS-002/`

## NS-002 – Vulnerability Assessment Using Nessus

### Objective
Performed a vulnerability assessment of an intentionally vulnerable
Metasploitable virtual machine using Nessus Essentials and Nmap.

### Lab Environment

| Component | Details |
|---|---|
| Scanner | Kali Linux |
| Scanner IP | 192.168.52.128 |
| Target | Metasploitable |
| Target IP | 192.168.52.129 |
| Scanner | Nessus Essentials |
| Discovery Tool | Nmap |
| Virtualization | VMware |

### Assessment Activities

- Discovered target services using Nmap
- Configured a Nessus vulnerability scan
- Performed vulnerability assessment
- Analyzed severity and CVE information
- Reviewed affected services and ports
- Documented Nessus evidence
- Prepared remediation recommendations
- Planned post-remediation validation

### Key Findings

The assessment identified vulnerabilities involving:

- End-of-life operating system
- DNS/BIND
- SMB/Samba
- NFS
- rsh
- SMTP
- PostgreSQL
- SSL/TLS configuration
- HTTP configuration

### Documentation

- [NS-002 Vulnerability Assessment Report](Documentation/NS-002_Vulnerability_Assessment_Report.md)
- [Nessus Scan Evidence](Evidence/NS-002/NS-002-Nessus-Scan-Completed.pdf)

### Skills Demonstrated

`Nessus` `Nmap` `Vulnerability Assessment` `CVE Analysis`
`Risk Analysis` `Network Security` `Linux` `Remediation`
`Security Reporting`
