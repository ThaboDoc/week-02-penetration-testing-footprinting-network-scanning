# 🛡️ CYBERSECURITY PROJECT REPORT
## WEEK 02 | PENETRATION TESTING

### FOOTPRINTING • RECONNAISSANCE • NETWORK SCANNING

---

**NETWORKWALKS CYBERSECURITY PROGRAMME**

| Project information | Details |
|---|---|
| Prepared by | Thabo Mhlongo |
| Programme | Networkwalks |
| Programme / Batch | B084 |
| Project modules | W2-PM1 & W2-PM5 |
| Report date | 11 November 2026 |
| Operating environments | Kali Linux & Windows |
| Project category | Cybersecurity / Ethical Hacking |

---

## 📌 TABLE OF CONTENTS

1. Executive Summary
2. Project Objectives
3. Scope and Authorization
4. Tools and Technologies
5. Methodology and Activities
6. Findings and Risk Observations
7. Security Recommendations
8. Learning Outcomes
9. Challenges and Verification
10. Conclusion
11. Supporting Evidence
12. Disclaimer

---

# 01 | EXECUTIVE SUMMARY

This report presents the practical cybersecurity activities completed during Week 2 of the Networkwalks Cybersecurity Programme.

The project focused on two important stages of penetration testing: **Reconnaissance and Footprinting**, followed by **Network Scanning and Discovery**.

The first phase involved gathering publicly available information about the `networkwalks.com` domain using various Kali Linux security tools.

The second phase involved performing network discovery on my own local network using Zenmap to identify active hosts, IP addresses, MAC addresses and network topology.

These practical exercises provided hands-on experience in information gathering, DNS enumeration, website technology identification, HTTP response analysis and network discovery.

<blockquote>
**PROJECT FOCUS**

Understand how information gathering and network discovery contribute to identifying and assessing an organization's digital environment.
</blockquote>

# 02 | PROJECT OBJECTIVES

The primary objectives of this project were to:

- Perform reconnaissance and footprinting activities.
- Gather publicly available domain information.
- Identify DNS records and domain information.
- Discover website technologies and exposed application information.
- Identify web application firewall technology.
- Resolve domain names to IP addresses.
- Perform network discovery using Zenmap.
- Identify active hosts and network information.
- Document findings and potential security risks.

# 03 | SCOPE AND AUTHORIZATION

The practical activities covered two phases.

### Phase 1 — Reconnaissance and Footprinting

<badge color="info">W2-PM1</badge>

| Item | Description |
|---|---|
| Target | `networkwalks.com` |
| Environment | Kali Linux |
| Activities | Domain information gathering, DNS enumeration and website fingerprinting |

### Phase 2 — Network Scanning and Discovery

<badge color="success">W2-PM5</badge>

| Item | Description |
|---|---|
| Target | Own local LAN network |
| Environment | Windows with Zenmap |
| Activities | Host discovery, IP and MAC identification, network topology |

All activities were performed within the authorized scope of the educational practical exercises and on my own network.

No exploitation or vulnerability validation was conducted.

# 04 | TOOLS AND TECHNOLOGIES

The following tools were used throughout the practical exercises.

| Tool | Purpose |
|---|---|
| 🐉 Kali Linux | Penetration testing environment |
| WHOIS | Domain registration information |
| WhatWeb | Website technology identification |
| Nslookup | DNS resolution |
| Curl | HTTP response header inspection |
| Wafw00f | Web Application Firewall identification |
| DNSRecon | DNS enumeration |
| Zenmap | Graphical network scanning |
| Nmap | Network discovery engine |
| Windows CMD | Local network configuration |

# 05 | METHODOLOGY AND ACTIVITIES

## 5.1 Reconnaissance and Footprinting

The first phase involved using six Kali Linux tools to gather information about the target domain.

### 5.1.1 WHOIS — Domain Information Gathering

WHOIS was used to retrieve publicly available domain registration information.

**Information collected included:**
- Domain registration details.
- Registrar information.
- Domain creation and expiry dates.
- Name server information.
- Domain status.

**Objective:** Understand how publicly available domain registration information can assist with infrastructure reconnaissance.

### 5.1.2 WhatWeb — Website Technology Identification

WhatWeb was used to identify technologies associated with the target website.

The original report recorded WordPress and WP Download Manager version information, together with other website technology details.

**Objective:** Understand how website fingerprinting can reveal information about a web application's underlying technologies.

### 5.1.3 Nslookup — DNS Resolution

Nslookup was used to resolve the target domain name to its associated IP address.

<badge color="info">Recorded result</badge>

`192.232.216.135`

**Objective:** Understand how DNS translates domain names into IP addresses.

### 5.1.4 Curl — HTTP Response Analysis

Curl was executed using the `-I` option to inspect the website's HTTP response headers.

The activity also identified the WordPress REST API endpoint:

`/wp-json/`

**Objective:** Examine HTTP responses and identify technical information exposed by a web application.

### 5.1.5 Wafw00f — Firewall Identification

Wafw00f was used to identify whether a Web Application Firewall was present.

<badge color="success">Identified technology</badge>

**ModSecurity (SpiderLabs)**

**Objective:** Understand how security professionals identify technologies used to protect web applications.

### 5.1.6 DNSRecon — DNS Enumeration

DNSRecon was used to enumerate DNS-related information.

The report covered:
- Name server records.
- Mail server records.
- SPF and TXT records.
- Service records.
- DNS infrastructure information.

**Objective:** Understand how DNS enumeration contributes to the reconnaissance process.

---

## 5.2 Network Scanning and Discovery

The second phase focused on discovering active devices within my own local network using Zenmap.

### 5.2.1 Local Network Identification

The Windows `ipconfig` command was used to identify the local IP configuration and subnet.

The identified subnet was then used as the scanning target in Zenmap.

### 5.2.2 Host Discovery Using Zenmap

Zenmap was configured to perform a Ping Scan against the local subnet.

The practical report recorded the following live host addresses:

| Host | IP address |
|---|---|
| Host 01 | `10.0.0.1` |
| Host 02 | `10.0.0.2` |
| Host 03 | `10.0.0.5` |

The risk assessment section of the original report refers to four live hosts. This discrepancy requires verification against the original scan evidence.

### 5.2.3 IP and MAC Address Identification

The practical included identifying IP and MAC address information for discovered devices.

This information supports basic network inventory management and helps establish which devices are connected to a network.

### 5.2.4 Network Topology

Zenmap was also used to generate a network topology, providing a visual representation of discovered network devices.

**Objective:** Develop practical experience in network discovery and understanding network structure.

# 06 | FINDINGS AND RISK OBSERVATIONS

The practical exercises produced several observations relating to publicly available information and local network visibility.

| No. | Observation | Recorded risk |
|---|---|---|
| 01 | Website technology information was publicly identifiable | Low |
| 02 | Domain and DNS information was publicly available | Medium |
| 03 | HTTP response headers exposed technical information | Low |
| 04 | ModSecurity technology was identifiable | Low |
| 05 | DNS infrastructure information was discoverable | Medium |
| 06 | Multiple active hosts were identified on the local network | Medium |

**Risk interpretation:** These are observations from information gathering and host discovery. They do not represent confirmed vulnerabilities. Further authorized security testing would be necessary to validate any actual vulnerability.

# 07 | SECURITY RECOMMENDATIONS

Based on the observations recorded during the practical exercises, the following recommendations are proposed.

| Area | Recommended action |
|---|---|
| Website security | Review publicly exposed technology information |
| Software maintenance | Keep CMS platforms and plugins updated |
| HTTP security | Review response headers for unnecessary technical exposure |
| DNS security | Regularly review DNS records and exposed services |
| Firewall protection | Keep the WAF properly configured and monitored |
| Network visibility | Perform regular authorized internal network discovery |
| Device management | Investigate unknown or unexpected devices |
| Documentation | Maintain updated network topology and device inventories |
| Authorization | Ensure all security testing is performed within an approved scope |

# 08 | LEARNING OUTCOMES

Through these practical exercises, I developed a better understanding of the following cybersecurity concepts:

<badge color="success">Practical skills developed</badge>

- Reconnaissance and footprinting techniques.
- Kali Linux security tools.
- DNS resolution and enumeration.
- Website technology fingerprinting.
- HTTP response header analysis.
- Web Application Firewall identification.
- Network discovery using Zenmap.
- IP and MAC address identification.
- Network topology generation.
- Cybersecurity reporting and documentation.
- Responsible and authorized security testing.

# 09 | CHALLENGES AND AREAS FOR VERIFICATION

Before final publication, certain details in the original report should be checked against the supporting screenshots and command outputs.

These include:

1. Differences in the recorded WordPress and WP Download Manager versions.
2. The difference between three live hosts in the activity description and four in the risk assessment.
3. Availability of separate DNSRecon output as supporting evidence.

Verifying these details will improve the accuracy and reliability of the final project documentation.

# 10 | CONCLUSION

During Week 2 of the Networkwalks Cybersecurity Programme, I completed practical activities covering reconnaissance, footprinting and network scanning.

The first phase provided hands-on experience using Kali Linux tools to gather domain information, identify website technologies, inspect HTTP responses and enumerate DNS information.

The second phase provided practical experience using Zenmap to identify active hosts, examine local network information and generate a network topology.

These activities strengthened my understanding of how information gathering and network discovery contribute to cybersecurity assessments.

They also reinforced the importance of analysing technical findings, documenting observations and conducting all security activities within an authorized environment.

**This project represents an important step in developing my practical cybersecurity and ethical hacking skills.**

# 11 | SUPPORTING EVIDENCE

The following evidence should be included in the repository to support the documented activities.

| Evidence folder | Supporting material |
|---|---|
| `whois/` | WHOIS command output |
| `whatweb/` | Website fingerprinting results |
| `nslookup/` | DNS resolution results |
| `curl/` | HTTP response headers |
| `wafw00f/` | WAF identification results |
| `dnsrecon/` | DNS enumeration output |
| `zenmap/` | Network scan screenshots |
| `topology/` | Network topology screenshot |

# 12 | DISCLAIMER

This documentation is intended for educational and research purposes.

All security testing activities must be conducted only on systems and networks owned by the tester or where appropriate authorization has been obtained.

Unauthorized access, scanning or testing may violate applicable laws and organizational policies.

---

## PROJECT DETAILS

**Project:** Week 02 – Penetration Testing  
**Programme:** Networkwalks Cybersecurity Programme  
**Prepared by:** Thabo Mhlongo  

**Focus areas:** Reconnaissance | Footprinting | DNS Enumeration | Network Scanning

*End of Report*
