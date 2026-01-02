# -cyart-vapt-team
vapt_task02 

# Week 2 – Vulnerability Assessment & Penetration Testing (VAPT)

## 1. Project Overview

This repository documents Week-2 Vulnerability Assessment and Penetration Testing (VAPT) activities performed in a controlled laboratory environment.
The objective is to understand reconnaissance, vulnerability scanning, exploitation, post-exploitation, and reporting, using industry-standard tools and methodologies in an ethical and controlled lab environment.

## 2. Scope

- Target: Local lab virtual machines (e.g., Metasploitable2, DVWA)
- Testing Type: Internal VAPT
- Environment: Isolated lab setup

## 3. Tools Used

- Nmap – Network and service scanning
- Nikto – Web application vulnerability scanning
- OpenVAS – Automated vulnerability assessment
- Shodan – OSINT reconnaissance (theoretical / simulation)
- Metasploit – Exploitation simulation
- sqlmap – SQL injection testing
- Google Docs / PDF – Documentation and reporting

## 4. Complete Workflow

## 1. Reconnaissance (Information Gathering)

### Objective:
- Gather initial information about the target to understand its attack surface.

### Steps:
- Perform OSINT study using Shodan (simulated / theoretical).
- Identify exposed services, ports, and technologies.
- Map available information related to the target.
- Document all findings.

### Output:
- IP address details
- Exposed services
- Technology stack information

### Evidence: Recon/Recon.pdf

## 2. Vulnerability Scanning

### Objective:
- Identify vulnerabilities, misconfigurations, and insecure services.

### 2.1 Nmap Scan (Network Scanning)
### Objective:
- To discover open ports and active services on the target system.
  
### Steps:
1. Run: nmap -sS -sV -O 192.168.72.129 -oN nmap_scan.txt
2. Identify open ports and running services.
3. Analyze services for potential weaknesses.
4. Save scan results.

### Evidence: Scans/Nmap Scan.pdf

### 2.2 Nikto Scan (Web Application Scanning)

### Objective:
- Identify web server and application-level vulnerabilities.

### Steps:
1. Identify HTTP/HTTPS service running on the target.
2. Run Nikto scan: nikto -h http://192.168.72.129
3. Detect issues such as:
      - Insecure HTTP headers
      - Default files and configurations
4. Save results.

### Evidence: Scans/Nikto Scan.pdf

### 2.3 OpenVAS Scan 

### Objective:
- To perform automated vulnerability scanning and assess security risks on the target system.

### Steps:
1. Configure the target in OpenVAS.
2. Run a full vulnerability scan.
3. Analyze detected CVEs and severity levels.
4. Export scan report.

### Evidence: Scans/Openvas.pdf

## 3. Vulnerability Analysis & CVE Documentation

### Objective:
- Assess the severity and risk of identified vulnerabilities.

### Steps:
1. Review scan results from Nmap, Nikto, and OpenVAS.
2. Identify relevant CVEs.
3. Assign severity using CVSS (Low / Medium / High / Critical).
4. Prepare CVE documentation.

### Evidence: CVE Sheet/CVE sheet screenshot.png

## 4. Exploitation 

### Objective:
- Validate vulnerabilities by controlled exploitation.

### Steps:
1. Use Metasploit to simulate exploitation of known vulnerabilities.
2. Perform SQL injection testing using sqlmap on vulnerable applications (DVWA).
3. Observe results such as access gained or payload execution.
4. Capture screenshots for evidence.

### Evidence: Exploitation/

## 5. Post-Exploitation 

### Objective:
- Understand the impact after successful exploitation.

### Steps:
1. Analyze the level of access achieved.
2. Study privilege escalation concepts.
3. Avoid destructive or unauthorized actions.

### Evidence: Exploitation/

## 6. Reporting & Documentation

### Objective:
- To document findings in a clear and professional manner.

### Steps:
- Compile scanning and exploitation results.
- Organize evidence such as PDFs and screenshots.
- Document workflow and observations.

## 7. Conclusion

This project demonstrates a complete VAPT workflow including reconnaissance, vulnerability scanning, exploitation simulation, risk analysis, and documentation while adhering to ethical standards and industry-recognized methodologies.
