# Understand The OSI Model

## Introduction
The Open Systems Interconnection (OSI) model is a conceptual framework, not a protocol itself. It's a standardized abstraction used to describe and understand how data communication occurs across networks, particularly in heterogeneous environments where different systems need to interoperate. Developed by the International Organization for Standardization (ISO), it divides network communication into seven distinct layers, each responsible for specific functions. Understanding the OSI model is crucial for cybersecurity professionals as it provides a structured approach to analyzing network traffic, identifying vulnerabilities, and designing secure architectures.

## The Seven Layers
Each layer interacts with the layers directly above and below it. Data travels down the stack on transmission (encapsulation) and up the stack on reception (decapsulation). Let's examine each layer in detail:

### 1. Physical Layer:
  - **Function:** This is the lowest layer, dealing with the physical medium used for data transmission. It defines characteristics like voltage levels, bit timing, cabling standards (e.g., Ethernet Cat5e/6, fiber optic), and radio frequencies. It's concerned with how bits are transmitted, not what those bits represent.
  - **Data Unit:** Bits
  - **Relevant Technologies:** Ethernet cables, wireless signals (Wi-Fi), optical fibers, hubs, repeaters.
  - **Cybersecurity Implications & Attack Vectors:**
    - **Physical Tampering:** Direct physical access to cabling can allow for eavesdropping or data injection.
    - **Electromagnetic Interference (EMI):** Malicious devices could generate EMI to disrupt communication.
    - **Signal Injection/Spoofing:** Sophisticated attacks might involve injecting false signals onto the medium, though this is typically difficult without physical proximity and specialized equipment.
   
### 2. Data Link Layer:
  - **Function:** Provides reliable error-free transmission of data frames between two directly connected nodes (e.g., a computer and a switch). It handles addressing at the MAC address level. This layer divides the bit stream from the Physical Layer into frames.
  - **Data Unit:** Frames
  - **Sublayers:** Logical Link Control (LLC) & Media Access Control (MAC)
  - **Relevant Technologies:** Ethernet, switches, MAC addresses, Frame Relay, PPP.
  - **Cybersecurity Implications & Attack Vectors:**
    - **MAC Address Spoofing:** An attacker can change their device's MAC address to impersonate another device on the network, potentially gaining unauthorized access or disrupting services. ARP poisoning is a common technique leveraging this.
    - **Switch Flooding/MAC Table Poisoning:** Attackers might flood a switch with traffic to overwhelm it and disrupt its ability to forward frames correctly (Denial of Service). They can also poison the MAC table, directing traffic to unintended destinations.

### 3. Network Layer:
  - **Function:** Responsible for routing data packets from source to destination across multiple networks. It handles logical addressing using IP addresses. This layer determines the best path for a packet to take.
  - **Data Unit:** Packets
  - **Relevant Technologies:** IP (IPv4, IPv6), routers, ICMP, ARP.
  - **Cybersecurity Implications & Attack Vectors:**
    - **IP Spoofing:** An attacker can forge the source IP address in a packet to impersonate another host or evade detection.
    - **Routing Protocol Attacks:** Attacks targeting routing protocols (e.g., BGP hijacking) can redirect traffic through malicious nodes.
    - **Denial of Service (DoS):** ICMP flood attacks (ping floods) exploit this layer to overwhelm network resources.
   
### 4. Transport Layer:
  - **Function:** Provides end-to-end data delivery and flow control between applications on different hosts. It ensures reliable or unreliable data transfer, segmentation/reassembly of data streams, and port addressing.
  - **Data Unit:** Segments (TCP) / Datagrams (UDP)
  - **Protocols:** TCP (Transmission Control Protocol - connection-oriented, reliable), UDP (User Datagram Protocol – connectionless, unreliable).
  - **Cybersecurity Implications & Attack Vectors:**
    - **Port Scanning:** Attackers scan ports to identify open services and potential vulnerabilities.
    - **TCP Session Hijacking:** An attacker intercepts an established TCP connection and takes control of it.
    - **SYN Flood Attacks:** Exploits the TCP handshake process to exhaust server resources, leading to a denial-of-service condition.
   
### 5. Session Layer:
- **Function:** Establishes, manages, and terminates connections (sessions) between applications. It handles authentication, authorization, and session recovery. This layer is often integrated with the Presentation or Application layers in modern implementations.
- **Relevant Technologies:** NetBIOS, RPC, TLS/SSL handshakes (can be considered a session management component).
- **Cybersecurity Implications & Attack Vectors:**
  - **Session Hijacking:** An attacker gains control of an established session, impersonating the legitimate user. (Often overlaps with Transport Layer attacks)
  - **Authentication Bypass:** Exploiting vulnerabilities in session establishment or authentication mechanisms.

### 6. Presentation Layer:
- **Function:** Concerned with data formatting, encryption/decryption, and character set conversion. It ensures that data is presented in a format understandable by the receiving application. This layer handles tasks like compression, encoding (e.g., ASCII, UTF-8), and SSL/TLS encryption.
- **Relevent Technologies:** SSL/TLS, SSH, JPEG, MPEG.
- **Cybersecurity Implications & Attack Vectors:**
  - **SSL/TLS Vulnerabilities:** Exploiting weaknesses in the implementation or configuration of SSL/TLS protocols (e.g., Heartbleed).
  - **Man-In-The-Middle Attacks (MITM):** Intercepting and potentially modifying encrypted data if encryption is not properly implemented or keys are compromised.
 
### 7. Application Layer:
- **Function:** Provides network services to end-user applications, such as web browsing (HTTP), email (SMTP, IMAP), file transfer (FTP), and remote access (SSH). This layer interacts directly with the user.
- **Relevant Technologies:** HTTP, FTP, SMTP, DNS, SSH, Telnet.
- **Cybersecurity Implications & Attack Vectors:**
  - **Application-Specific Vulnerabilities:** Exploiting flaws in application code (e.g., SQL injection, cross-site scripting).
  - **DNS Spoofing/Cache Poisoning:** Manipulating DNS records to redirect users to malicious websites.
  - **Malware Distribution:** Using applications like FTP or HTTP servers to distribute malware.
 
The OSI model provides a valuable framework for understanding network communication and identifying potential security vulnerabilities at each layer. Cybersecurity professionals must be familiar with the functions of each layer and the associated attack vectors to effectively design, implement, and maintain secure networks. While modern networking often deviates from strict adherence to the OSI model (e.g., TCP/IP model), the conceptual framework remains a vital tool for analysis and troubleshooting.

### Next Step
- [Common Protocols And Their Uses](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Common_Protocols_And_Their_Uses.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resource
- [https://aws.amazon.com/what-is/osi-model/](https://aws.amazon.com/what-is/osi-model/)
