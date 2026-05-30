## Sample SOC Analyst Executive Report: Phishing Domain Investigation

## Overview
This project documents an Open-Source Intelligence (OSINT) investigation of a suspicious domain impersonating Booking.com. The investigation was conducted in a controlled cybersecurity laboratory environment using passive reconnaissance techniques to identify indicators associated with phishing infrastructure.

## Objective
The goal was to analyze the domain's DNS records, hosting infrastructure, and web server characteristics to determine whether it exhibited traits commonly associated with phishing campaigns.
Domain Investigated
booking.com-approve-reservation.com

## Methodology
The investigation employed passive OSINT techniques, including:
WHOIS analysis
DNS enumeration
Nameserver analysis
MX record inspection
HTTP header analysis
Infrastructure profiling
Tools Used
WHOIS
DIG
CURL
Ubuntu Linux
VirtualBox

## Key Findings

# Brand Impersonation
The domain name closely mimics legitimate Booking.com reservation processes through the use of terms such as: Booking- approve- reservation. This naming pattern is commonly observed in phishing campaigns designed to deceive users.
# DNS Infrastructure
The domain resolved to:
104.21.62.80
172.67.221.208
The infrastructure was protected by Cloudflare, masking the origin server and complicating attribution efforts.
# Email Infrastructure
No MX records were identified for the domain, suggesting it was not configured for legitimate business email communication.
# Web Server Analysis
HTTP inspection returned:
HTTP/2 403 Forbidden
Headers indicated active Cloudflare protection and challenge mechanisms.
Indicators of Compromise (IOCs)
# Type	Value
Domain	      : booking.com-approve-reservation.com
IP Address    :	104.21.62.80
IP Address    :	172.67.221.208
# Infrastructure	Cloudflare
Threat Category	Brand Impersonation Phishing

## Threat Assessment
Based on the observed indicators, the domain demonstrates several characteristics frequently associated with phishing infrastructure:
Brand impersonation
Infrastructure obfuscation
Lack of legitimate email services
Restricted web access through protective services
While passive OSINT alone cannot conclusively prove malicious intent, the findings warrant treating the domain as potentially malicious until further verification is available.

## Key Management Recommendations
Block identified phishing indicators across DNS filtering, firewalls, and web security gateways. 
Strengthen phishing awareness training to improve employee recognition of brand-impersonation attacks. 
Enhance threat monitoring and detection through SIEM alerts and IOC tracking. 
Improve email and web security controls using SPF, DKIM, DMARC, URL filtering, and DNS reputation services.

## Skills Demonstrated
Threat Intelligence
OSINT Investigation
DNS Analysis
Cyber Threat Hunting
IOC Identification
Linux Command Line
Security Reporting
MITRE ATT&CK Mapping

## Key Lessons Learned
This investigation highlights the importance of combining technical indicators with contextual analysis when assessing suspicious domains. Passive reconnaissance can reveal valuable threat intelligence while maintaining a safe and ethical investigation approach.

## Disclaimer
This investigation was conducted solely for educational, research, and cybersecurity awareness purposes. No attempts were made to access, exploit, or interact with the target infrastructure beyond passive information gathering techniques.
