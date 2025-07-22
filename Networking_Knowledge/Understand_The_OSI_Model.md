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

### 3. Network Layer


### Next Step
- [Common Protocols And Their Uses](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Common_Protocols_And_Their_Uses.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resource
- [https://aws.amazon.com/what-is/osi-model/](https://aws.amazon.com/what-is/osi-model/)
