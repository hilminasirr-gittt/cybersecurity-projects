# Home Network Vulnerability Assessment Using Kali Linux and Nmap

## Project Overview

This project performs a basic internal vulnerability assessment of a home network using Kali Linux and Nmap. The objective was to identify active devices on the network, discover exposed services, and evaluate potential security risks.

The assessment follows a typical vulnerability assessment workflow including network discovery, port scanning, service detection, vulnerability identification, and risk analysis.

---

## Tools Used

- Kali Linux
- Nmap
- Oracle VirtualBox

---

## Network Scope

Target Network: 192.168.0.0/24

Devices discovered during the assessment:

| IP Address | Device |
|------------|--------|
| 192.168.0.1 | Router / Gateway |
| 192.168.0.X | Internal Host |
| 192.168.0.X | Kali Assessment Machine |

---

## Methodology

The following steps were performed during the assessment:

1. Environment Setup
2. Network Discovery
3. Port Scanning
4. Service Enumeration
5. Vulnerability Identification
6. Risk Analysis

---

## Key Findings

- Router exposes web management services on ports 80 (HTTP) and 443 (HTTPS)
- Administrative services such as SSH, FTP, and Telnet are filtered by the firewall
- A Windows host was discovered running multiple HTTP services
- No critical vulnerabilities were identified during the scan
- Router login form showed a possible CSRF exposure

Overall risk level: **Low**

---

## Example Commands Used

Network discovery:
nmap -sn 192.168.0.0/24


Router port scan
nmap 192.168.0.1


Service and OS detection
nmap -sV -O 192.168.0.1


Vulnerability scan
nmap --script vuln 192.168.0.1

---

## Project Outcome

This project demonstrates the workflow of a basic vulnerability assessment including reconnaissance, service enumeration, vulnerability scanning, and security reporting.
The project provides hands-on experience using Kali Linux and Nmap to evaluate the security posture of a local network environment.

---

## Author

Cybersecurity learning project
