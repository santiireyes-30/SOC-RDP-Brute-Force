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

Successful Authentication Detected During further log analysis, it was identified that after multiple failed login attempts (Event ID 4625), a successful authentication occurred.  Event ID: 4624  Logon Type: 10 (RemoteInteractive – RDP)  Source IP: 218.92.0.56  Destination IP: 172.16.17.148  Username: Matthew  This indicates that the brute force attack was ultimately successful, allowing the attacker to gain remote access to the system via RDP.  The presence of Logon Type 10 confirms that the authentication was performed through Remote Desktop Protocol.  This escalates the incident from an attempted brute force attack to a confirmed security compromise.

Clasification: True Positive


Action: Host Contained - Isolate Endpoint
