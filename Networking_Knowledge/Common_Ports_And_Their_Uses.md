# Common Ports And Their Uses

## Understanding Network Ports: A Cybersecurirty Essential
Network ports are standardized communication endpoints that facilitate data exchange between applications on different devices. They're integral to cybersecurity, enabling effective firewall configuration, threat detection, and network traffic management. A deep understanding of these ports is a cornerstone for any security professional.

While seeminly abstract, ports provide crucial context when analyzing network activity. Deviations from expected port usage can indicate malicious behaviour or misconfigured services.

Here's a breakdown of some key ports:

- HTTP/HTTPS (80/443): The backbone of web communications; monitoring these ports is essential for detecting eavesdropping attempts and unauthorized access.

- SSH (22): Secure Shell provides remote administration capabilities, making port 22 a frequent target for brute-force attacks.

- SMTP (25): Used for outbound email transmission; securing this port helps prevent spam relaying and phishing campaigns.

- DNS (53): Critical for name resolution; vulnerabilities in DNS servers can lead to widespread outages or redirection of traffic.

- FTP (21/20): While largely superseded by more secure protocols, FTP's control (21) and data (20) ports remain relevant in legacy systems.

- SMB (137-139/445): File sharing services; vulnerabilities in SMB have historically been exploited for wide-spread attacks like WannaCry.

- Database Ports (3306/1433): MySQL and Microsoft SQL Server, respectively - securing these ports is vital to protect sensitive data.

Cybersecurity professionals leverage port scanning tools (nmap) and Intrusion Detection Systems (IDSes) to monitor network traffic, identify anomalies, and proactively defend against attacks targeting specific services associated with these common ports. 

### Next Step
- [SSL And TLS Basics](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/SSL_And_TLS_Basics.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
