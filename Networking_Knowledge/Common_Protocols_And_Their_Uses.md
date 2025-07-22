# Essential Networking Protocols

## Introduction
Effective cybersecurity practice necessitates a thorough comprehension of network protocols. These protocols govern communication between devices and systems, forming the backbone of data transmission across networks. Understanding their functionality, inherent vulnerabilities, and potential attack vectors is paramount for proactive security measures, incident response, and overall risk mitigation. This guide provides an overview of key protocols relevant to cybersecurity professionals.

## The TCP/IP Suite: Foundation of Internet Communication
The Transmission Control Protocol/Internet Protocol (TCP/IP) suite isn't a single protocol but a layered framework defining how data is packaged, addressed, transmitted, routed, and received over the internet. It comprises multiple protocols working in conjunction.

### Key Protocols within TCP/IP:
- **IP (Internet Protocol):** Responsible for addressing and routing packets across networks. It's connectionless and unreliable – packets may arrive out of order or be lost.

- **TCP ( Transmission Control Protocol):** Provides reliable, ordered, and error-checked delivery of data between applications. It establishes a connection before data transfer and guarantees delivery through acknowledgements and retransmissions. This makes it suitable for applications like web browsing and file transfer.

- **UDP (User Datagram Protocol):** A connectionless protocol offering faster transmission but without the reliability features of TCP. Suitable for real-time applications where occasional packet loss is acceptable (e.g., streaming media, online gaming).

### Attack Vectors:
- IP spoofing (falsifying source IP addresses), ICMP flooding (Denial of Service attacks exploiting ping requests), TCP SYN flood attacks (exploiting the TCP handshake process to exhaust server resources).


### Next Steps
- [Common Ports and Their Uses](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Common_Ports_And_Their_Uses.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resource 
- [https://www.techtarget.com/searchnetworking/feature/12-common-network-protocols-and-their-functions-explained](https://www.techtarget.com/searchnetworking/feature/12-common-network-protocols-and-their-functions-explained)

