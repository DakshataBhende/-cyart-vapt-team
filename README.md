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

## 3. Lab Environment

| Component        | Details                                               |
| ---------------- | ----------------------------------------------------- |
| Attacker Machine | Kali Linux                                            |
| Target Machine   | Metasploitable2 / DVWA                                |
| Network          | Internal Host-Only Network   

## 4. Tools Used

- Nmap – Network and service scanning
- Nikto – Web application vulnerability scanning
- OpenVAS – Automated vulnerability assessment
- Shodan – OSINT reconnaissance (theoretical / simulation)
- Metasploit – Exploitation simulation
- sqlmap – SQL injection testing
- Google Docs / PDF – Documentation and reporting

## 5. Methodology

### Phases:
1. Reconnaissance
2. Vulnerability Scanning
3. Exploitation
4. Post-Exploitation
5. Reporting

## 6. Complete Workflow

## 6.1. Reconnaissance (Information Gathering)

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

### Evidence: Week-2/Recon/Recon.pdf

## 6.2. Vulnerability Scanning

### Objective:
- Identify vulnerabilities, misconfigurations, and insecure services.

### 6.2.1 Nmap Scan (Network Scanning)
### Objective:
- To discover open ports and active services on the target system.
  
### Steps:
1. Run: *nmap -sS -sV -O 192.168.72.129 -oN nmap_scan.txt*
2. Identify open ports and running services.
3. Analyze services for potential weaknesses.
4. Save scan results.

### Evidence: Week-2/Scans/Nmap Scan.pdf

### 6.2.2 Nikto Scan (Web Application Scanning)

### Objective:
- Identify web server and application-level vulnerabilities.

### Steps:
1. Identify HTTP/HTTPS service running on the target.
2. Run Nikto scan: *nikto -h http://192.168.72.129*
3. Detect issues such as:
      - Insecure HTTP headers
      - Default files and configurations
4. Save results.

### Evidence: Week-2/ Scans/Nikto Scan.pdf

### 6.2.3 OpenVAS Scan 

### Objective:
- To perform automated vulnerability scanning and assess security risks on the target system.

### Steps:
1. Configure the target in OpenVAS.
2. Run a full vulnerability scan.
3. Analyze detected CVEs and severity levels.
4. Export scan report.

### Evidence: Week-2/Scans/Openvas.pdf

## 6.3. Vulnerability Analysis & CVE Documentation

### Objective:
- Assess the severity and risk of identified vulnerabilities.

### Steps:
1. Review scan results from Nmap, Nikto, and OpenVAS.
2. Identify relevant CVEs.
3. Assign severity using CVSS (Low / Medium / High / Critical).
4. Prepare CVE documentation.

### Evidence: Week-2/CVE Sheet/CVE sheet screenshot.png

## 7. Exploitation 

### Objective:
- Validate vulnerabilities by controlled exploitation.

### Steps:
1. Use Metasploit to simulate exploitation of known vulnerabilities.
2. Perform SQL injection testing using sqlmap on vulnerable applications (DVWA).
3. Observe results such as access gained or payload execution.
4. Capture screenshots for evidence.

### Evidence: 
1. Week-2/Exploitation/metasploit_screenshots/Exploitation & Post-Exploitation.pdf (Metaploit Exploitation)
2. Week-2/Exploitation/DVWA/DVWA_screenshots.pdf (DVWA Exploitation)
              
## 8. Post-Exploitation 

### Objective:
- Understand the impact after successful exploitation.

### Steps:
1. Analyze the level of access achieved.
2. Study privilege escalation concepts.
3. Avoid destructive or unauthorized actions.

### Evidence: 1. Week-2/Exploitation/metasploit_screenshots/Exploitation & Post-Exploitation.pdf (Metaploit Exploitation)

## 9. Reporting & Documentation

### Objective:
- To document findings in a clear and professional manner.

### Steps:
- Compile scanning and exploitation results.
- Organize evidence such as PDFs and screenshots.
- Document workflow and observations.

## 10. Conclusion

This project demonstrates a complete VAPT workflow including reconnaissance, vulnerability scanning, exploitation simulation,post-exploitation, and documentation while adhering to ethical standards and industry-recognized methodologies.
