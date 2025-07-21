# Basics of Computer Networking

## Computer Networking Fundamentals
This document provides a detailed overview of computer networking principles, essential for cybersecurity professionals. It assumes familiarity with basic computing concepts but aims to clarify underlying mechanisms and potential vulnerabilities.

### Core Concepts & Terminology
**Network Topology:** The physical or logical arrangement of devices in a network. Common topologies include:
| Topology | Explanation |
|---|---|
| Bus | Simple, single cable; vulnerable to breaks and collisions. (Rarely used today) |
| Star | Central hub/switch connects all nodes; easier management & fault isolation but relies on the central device. |
| Ring | Data travels in a circular path; susceptible to single point of failure. (Historically used, less common now). |
| Mesh | Nodes are interconnected with multiple paths; highly resilient but complex and expensive. |

---

**Network Types:** Categorized by scale and access:
| Network Type | Explanation |
|---|---|
| LAN (Local Area Network) | Confined to a limited geographical area (e.g., home, office). |
| WAN (Wide Area Network) | Spans large geographical areas (e.g., the internet). |
| MAN (Metropolitan Area Network) | Connects LANs within a city or metropolitan area. |
| VPN (Virtual Private Network) | Creates a secure, encrypted connection over a public network (like the Internet), effectively extending a private network. |

---

**Protocols:** Sets of rules governing data communication:
| Protocol | Description |
|---|---|
| TCP/IP (Transmission Control Protocol/Internet Protocol) | The foundational protocol suite for the internet. TCP provides reliable, ordered delivery; IP handles addressing and routing. |
| UDP (User Datagram Protocol) | Connectionless protocol offering faster but unreliable transmission (suitable for streaming or gaming). |
| HTTP/HTTPS (Hypertext Transfer Protocol/Secure HTTP) | Used for web communication; HTTPS adds encryption via TLS/SSL. |
| DNS (Domain Name System) | Translates human-readable domain names into IP addresses. |
| DHCP (Dynamic Host Configuration Protocol) | Automatically assigns IP addresses and other network configuration parameters to devices. |

---

### Addressing & Routing
**IP Addresses:** Unique numerical identifiers assigned to each device on a network. Two versions:
  - **IPv4:** 32-bit address space (e.g., 192.168.1.1). Depleting rapidly.
  - **IPv6:** 128-bit address space, providing vastly more addresses.

**Subnetting:** Dividing a network into smaller subnetworks to improve efficiency and security. Involves borrowing bits from the host portion of an IP address.

**Routing:** The process of forwarding data packets between networks. Routers use routing tables to determine the best path for packet delivery.

**Static Routing:** Manually configured routes; inflexible but predictable.

**Dynamic Routing:** Routes are learned and updated automatically using routing protocols (e.g., OSPF, BGP).


--


### Network Hardware
**Hubs:** Simple devices that broadcast all incoming data to every connected device – inefficient and insecure. (Largely obsolete)

**Switches:** Forward data only to the intended recipient based on MAC addresses; more efficient than hubs.'

**Routers:** Connect different networks together, forwarding packets based on IP addresses.

**Firewalls:** Act as a barrier between networks, controlling traffic based on predefined rules. Can be hardware or software-based.

**Wireless Access Points (WAPs):** Allow devices to connect wirelessly to a network using Wi-Fi standards (e.g., 802.11a/b/g/n/ac/ax).

--

### Security Considerations & Attack Vectors
**MAC Address Spoofing:** An attacker can change their device's MAC address to impersonate another device on the network, potentially bypassing access controls.

**ARP Poisoning (Address Resolution Protocol Poisoning):** An attacker manipulates ARP tables to redirect traffic intended for a legitimate device to an attacker-controlled machine. This allows eavesdropping or man-in-the-middle attacks.

**DNS Spoofing/Cache Poisoning:** An attacker provides false DNS records, directing users to malicious websites.
DHCP Starvation: An attacker exhausts the available IP addresses in a DHCP pool, preventing legitimate devices from connecting.

**Wireless Network Attacks:**
  - **Evil Twin:** Setting up a rogue access point with a similar SSID to trick users into connecting.
  - **WEP/WPA/WPA2 Cracking:** Exploiting vulnerabilities in older wireless encryption protocols. (WPA3 is the current standard and offers improved security).

**Man-in-the-Middle (MITM) Attacks:** Intercepting communication between two parties without their knowledge, often facilitated by ARP poisoning or DNS spoofing.

**Denial of Service (DoS/DDoS):** Overwhelming a network or server with traffic to make it unavailable to legitimate users.

### Next Step
- [Operating Systems](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Operating_Systems/Operating_Systems.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resource / Study Sources
- [https://www.cisco.com/c/en/us/solutions/small-business/resource-center/networking/networking-basics.html](https://www.cisco.com/c/en/us/solutions/small-business/resource-center/networking/networking-basics.html)
- [CompTIA Network+ Certification Objectives](https://www.comptia.org/certifications/network)
