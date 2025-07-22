# Networking Fundamentals
This document outlines essential networking principles and technologies crucial for cybersecurity professionals. A solid foundation in networking is paramount for understanding vulnerabilities, implementing effective defenses, and responding to incidents.

## Network Protocols: The Langauge of Communication
Network protocols define the rules and formats governing data transmission across a network. Understanding these protocols is vital for identifying anomalies and potential attacks.

### TCP/IP (Transmission Control Protocol / Internet Protocol)
 - The foundational protocol suite for the internet. TCP provides reliable, connection-oriented communication; IP handles addressing and routing of packets. *Attack Vector: TCP SYN Flood – exploits the three-way handshake process to exhaust server resources.*

### DNS (Domain Name System)
 - Translates human-readable domain names (e.g., google.com) into numerical IP addresses. *Attack Vector: DNS Spoofing/Cache Poisoning - attackers inject false DNS records, redirecting users to malicious sites.*

### DHCP (Dynamic Host Configuration Protocol)
 - Automatically assigns IP addresses and other network configuration parameters to devices. *Attack Vector: Rogue DHCP Server – an attacker sets up a fake DHCP server to distribute incorrect configurations, potentially leading to man-in-the-middle attacks or denial of service.*

### HTTP/HTTPS (Hypertext Transfer Protocol/Secure)
 - Used for web communication. HTTPS provides encrypted communication using TLS/SSL. Attack Vector: HTTP Request Smuggling – exploits discrepancies in how front-end and back-end servers handle HTTP requests, allowing attackers to bypass security controls.

### SMTP (Simple Mail Transfer Protocol)
 - Used for sending email. *Attack Vector: Email Spoofing - forging the "From" address of an email to appear as if it originated from a trusted source.*

## Network Topologies: Architectural Layouts and Implications
Network topology describes the physical or logical arrangement of devices on a network. The chosen topology impacts performance, scalability, and resilience.

### Star Topology
Devices connect to a central hub (switch or router). *Advantages:* Easy management, fault isolation. *Disadvantages:* Central point of failure.

### Ring Topology
Devices connected in a circular fashion. Data travels unidirectionally. *Advantages:* Relatively simple implementation. *Disadvantages:* Single point of failure; difficult troubleshooting.

### Mesh Topology
Each device is interconnected with multiple others, providing redundancy. *Advantages:* High fault tolerance. *Disadvantages:* Complex and expensive to implement.

### Hybrid Topology
A combination of different topologies. Common in larger networks.

## IP Addressing & Subnetting: Organizing Network Space
Efficient network management relies on organized addressing schemes.

### IP Addresses (IPv4/IPv6)
Unique numerical identifiers assigned to devices on a network. IPv4 addresses are becoming scarce; IPv6 offers a vastly expanded address space.

### Subnetting
Dividing a larger IP network into smaller, more manageable subnetworks. This improves security by isolating traffic and reduces broadcast domains.

### CIDR (Classless Inter-Domain Routing)
 A method for representing IP address ranges using a slash notation (e.g., 192.168.1.0/24). This allows for more efficient allocation of IP addresses. *Understanding CIDR is crucial when analyzing routing tables and network configurations.*

 ## Network Devices: The Building Blocks of Connectivity & Security
 These devices perform specific functions within a network.

 ### Routers
Forward data packets between networks based on destination IP addresses. Critical for internet connectivity.

 ### Switches
Connect devices within the same network (LAN). Operate at Layer 2 (Data Link Layer) using MAC addresses.

 ### Firewalls
Act as a barrier between networks, controlling inbound and outbound traffic based on predefined rules. *Attack Vector: Firewall Rule Bypass – exploiting misconfigured or poorly designed firewall rules.*

 ### Access Points (APs)
Provide wireless network connectivity. Often vulnerable to unauthorized access if not properly secured. *Attack Vector: Rogue Access Point - an attacker sets up a fake AP to capture credentials or launch man-in-the-middle attacks.*

 ### Intrusion Dectection/Prevention Systems (IDS/IPS)
Monitor network traffic for malicious activity and either alert administrators (IDS) or actively block suspicious traffic (IPS).

## Network Security Measures: Protecting Data & Infastructure
Security measures are essential to protect the confidentiality, integrity, and availability of network resources.

### VPNs (Virtual Private Networks)
Create secure, encrypted tunnels for remote access or site-to-site connectivity.

### Encryption
Protecting data in transit and at rest using cryptographic algorithms.

### Network Segmentation
Dividing a network into isolated segments to limit the impact of security breaches.

### NAC (Network Access Control)
Controls access to the network based on device posture and user identity.

## Network Troubleshooting: Diagnosis & Resolution
Effective troubleshooting skills are vital for maintaining network stability and responding to incidents

### Ping
Tests basic connectivity to a host by sending ICMP echo requests

### Traceroute (or tracert)
Maps the path packets take to reach a destination, identifying potential bottlenecks or routing issues

### Network Analyzers (e/g. Wireshark)
Capture analyze network traffic for detailed inspection of protocols and data content. *Essential for forensic analysis and understanding complex network behavior.*

### Next Step
- [Understanding The OSI Model](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Understand_The_OSI_Model.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resources
- [RFCs (Request for Comments)](www.rfc-editor.org)
- [Wireshark Documentation](www.wireshark.org/docs/)
