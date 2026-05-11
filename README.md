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
