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
