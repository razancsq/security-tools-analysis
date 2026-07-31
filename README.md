# Security Tools Analysis

A hands-on analysis of four security tools included in Kali Linux, each representing a different category of security assessment: information gathering, web application testing, password auditing, and database exploitation. Each tool was installed, configured, and run against a designated test target, with results documented and paired with recommended countermeasures.

## Repository Contents

| File | Description |
|---|---|
| `Security_Tools_Analysis.docx` | Full report in Microsoft Word format |
| `Security_Tools_Analysis.pdf` | Full report in PDF format |
| `README.md` | Repository overview |

## Tools Covered

| Tool | Category | Purpose |
|---|---|---|
| NMAP / ZenMAP | Information Gathering | Host discovery, port scanning, service and OS detection |
| Nikto | Web Application Testing | Web server vulnerability and misconfiguration scanning |
| Hydra | Password Auditing | Dictionary and brute-force login testing |
| SQLmap | Database Exploitation | Automated detection and exploitation of SQL injection |

## Test Environment

| Item | Detail |
|---|---|
| Operating system | Kali Linux |
| Virtualization | Oracle VirtualBox |
| NMAP / ZenMAP target | demo.testfire.net |
| Hydra target | 127.0.0.1 (SSH service) |
| Nikto target | demo.testfire.net/login.jsp |
| SQLmap targets | testasp.vulnweb.com, testphp.vulnweb.com |

All targets are publicly available test and demo applications intended for security testing practice.

## Summary of Findings

| Tool | Key Result |
|---|---|
| NMAP / ZenMAP | Identified open ports 80, 443, and 8080, and fingerprinted the web service as Apache Tomcat/Coyote |
| Hydra | Recovered a weak SSH credential pair through a dictionary attack in under a few minutes |
| Nikto | Detected eight issues, including missing security headers, unsafe HTTP methods, and server banner disclosure |
| SQLmap | Confirmed SQL injection in a URL parameter and extracted database, table, and user data from the backend |

## Countermeasures Overview

| Area | Recommended Controls |
|---|---|
| Network exposure | Disable unused ports and services, apply firewall rules, use IDS/IPS, segment the network |
| Authentication | Enforce strong password policies, enable account lockout, add multi-factor authentication |
| Web server configuration | Add missing security headers, disable unsafe HTTP methods, mask server banners |
| Application layer | Use parameterized queries, validate all input, deploy a web application firewall, hash stored credentials |

## Report Structure

1. Introduction
2. Tool Presentation
3. NMAP and ZenMAP - Deep Dive
4. Hydra - Deep Dive
5. Nikto - Deep Dive
6. SQLmap - Deep Dive
7. Conclusion
8. References

The full methodology, command-line usage, screenshots, and detailed analysis for each tool are available in the report files above.
