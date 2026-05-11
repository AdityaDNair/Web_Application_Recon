# Web Reconnaissance and Service Enumeration Lab

## Overview
This project demonstrates basic web reconnaissance and service enumeration techniques using Nmap NSE scripts and browser-based analysis. The objective was to identify exposed web services, analyse HTTP responses, enumerate web resources, and understand how reconnaissance is performed against internet-facing systems.

## Tools Used
- Nmap
- Nmap NSE (Nmap Scripting Engine)
- Web Browser
- Windows Command Prompt

## Target
- scanme.nmap.org

## Objectives
- Perform web reconnaissance
- Analyse exposed HTTP services
- Enumerate web resources using NSE scripts
- Understand filtered ports and firewall behaviour
- Interpret reconnaissance results

---

# Reconnaissance Steps

## 1. Service Detection
Performed service version detection to identify exposed services and gather basic target information.

### Command Used
```bash
nmap -Pn -sV scanme.nmap.org
```

---

## 2. HTTP Header Enumeration
Used Nmap NSE HTTP header scripts to inspect HTTP response headers and identify server information.

### Command Used
```bash
nmap --script http-headers scanme.nmap.org
```

---

## 3. HTTP Enumeration
Performed web resource enumeration using Nmap NSE scripts to discover accessible web paths and services.

### Command Used
```bash
nmap --script http-enum scanme.nmap.org
```

---

## 4. Combined NSE Reconnaissance Scan
Executed multiple NSE scripts together and exported results to a file for documentation and analysis.

### Command Used
```bash
nmap --script http-headers,http-enum -oN results/web-recon.txt scanme.nmap.org
```

---

# Findings and Analysis

## Observations
- The target host was reachable and responded to reconnaissance attempts.
- Multiple ports were filtered, indicating firewall protections.
- HTTP-related reconnaissance scripts successfully gathered additional information about the target web service.
- NSE scripts demonstrated how automated enumeration can assist during the reconnaissance phase of a security assessment.

## Security Analysis
Filtered ports reduce exposure and limit information disclosure during reconnaissance attempts. HTTP enumeration and header analysis help identify server technologies and potential security configurations.

---

# Screenshots

## Service Detection
![Service Detection]()

## HTTP Header Enumeration
![HTTP Headers]()

## HTTP Enumeration
![HTTP Enumeration]()

---

# Skills Demonstrated
- Web reconnaissance
- Service enumeration
- HTTP analysis
- NSE script usage
- Reconnaissance documentation
- Security analysis
- Network scanning

---

# Conclusion
This project provided hands-on experience with reconnaissance techniques used during web application and network security assessments. It demonstrated how Nmap NSE scripts can be used to gather information about web services and analyze internet-facing infrastructure.

# Web_Application_Recon
Performed web application reconnaissance and security assessment using Nikto and Nmap. Identified exposed services, HTTP headers, web technologies, and potential web server misconfigurations.

## Reconnaissance Findings
The target host was reachable and resolved to an AWS EC2 cloud instance.

### Observations
- All scanned TCP ports were filtered
- No direct service enumeration was possible
- The target likely uses firewall filtering or IDS/IPS protections
- Packet filtering prevented Nmap from identifying exposed services

### Security Analysis
Filtering all inbound probes reduces attack surface visibility and helps protect internet-facing infrastructure from reconnaissance attempts.

### Skills Demonstrated
- Host discovery
- Service enumeration attempts
- Firewall detection
- Interpreting filtered port responses
- Reconnaissance analysis
