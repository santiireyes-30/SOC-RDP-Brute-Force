# SOC-RDP-Brute-Force

Alert Details:
  Event ID: 234
  
  Date: Mar 07, 2024 – 11:44 AM
  
  Rule Name: SOC176 – RDP Brute Force Detected
  
  Severity Level: Security Analyst
  
  Source IP: 218.92.0.56 (External)
  
  Destination IP: 172.16.17.148 (Internal)
  
  Hostname: Matthew
  
  Protocol: RDP (TCP 3389)
  
  Firewall Action: Allowed
  
  Trigger Reason: Multiple login failures from a single source using different non-existing accounts


IOC: 

- Source IP: 218.92.0.56
  
- Protocol: RDP (3389)

IOA: 
  
  Commands history in terminal
  
  - whoami

  - net user

  - net localgroup administrators

  - netstat -ano


Executive Summary of the Incident:

March 7, 2024, an alert was triggered due to multiple failed RDP login attempts from a single external IP address targeting a Windows endpoint inside the internal network.  The activity indicates a brute force attack attempt against the Remote Desktop Protocol (RDP) service.  No successful authentication was observed.
