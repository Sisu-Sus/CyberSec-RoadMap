# Understand The OSI Model

## Roadmap.sh Summary:
The Open Systems Interconnection(OSI) Model is a conceptual framework that describes how data communication occurs between devices in a network. It consists of seven layers, each with specific fucntions:

1. Physical - Deals with physical transmission media
2. Data Link - Handles error-free transfer between adjacent nodes
3. Network - Manages addressing and routing
4. Transport - Ensure end-to-end data delivery and flow control
5. Session - Establishes, manages, and terminates connections
6. Presentation - Formats and encrypts data for the application
7. Application - Provides network services to end-user applications

### Resource
[https://aws.amazon.com/what-is/osi-model/](https://aws.amazon.com/what-is/osi-model/)

### Physical Layer
The physical layer refers to the physical communication medium, and the technologies to transmit data across that medium. At its core, data communication is the transfer of digital and electronic signals through various physical channels like fiber-optic cables, copper cabling, and air. The physical layer includes standards for technologies and metrics closely related with channels, such as Bluetooth, NFC, and data transmission

### Data Link Layer
The data link layer refers to the technologies used to connect two machines across a network where the physical layer already exists. It manages data frames, which are digital signals encapsulated into data packets. Flow control and error control of data are often key focuses of the data link layer. Ethernet is an example of a standard at this level. The data link layer is often split into two sub-layers: the Media Access Control (MAC) layer and Logical Link Control (LLC) layer

### Network Layer
The network layer is concerned with concepts such as routing, forwarding, and addressing across a dispersed network or multiple connected networks of nodes or machines. The network layer may also manage flow control. Across the internet, the Internet Protocol v4 (IPv4) and IPv6 are used as the main network layer protocols.

### Transport Layer
The primary focus of the transport layer is to ensure that data packets arrive in the right order, without losses or errors, or can be seamlessly recovered if required. Flow control, along with error control, is often a focus at the transport layer. At this layer, commonly used protocols include the Transmission Control Protocol (TCP), a near-lossless connection-based protocol, and the User Datagram Protocol (UDP), a lossy connectionless protocol. TCP is commonly used where all data must be intact (e.g file share), whereas UDP is used when retaining all packets is less critical (e.g, video streaming).

### Session Layer
The session layer is responsible for network coordination between two seperate applications in a session. A session manages the beginning and ending of a one-to-one application connection and synchronization conflicts. Network File System (NFS) and Server Message Block (SMB) are commonly used protocols at the session layer.

### Presentation Layer
The presentation layer is primarily concerned with the syntax of the data itself for applications to send and consume. For example, Hypertext Markup Language (HTML), JavaScript Object Notation (JSON), and Comma Seperate Values (CSV) are all modeling langauges to describe the structure of data at the presentation layer

### Application Layer
The application layer is concerned with the specific type of application itself and its standardized communication methods. For example, browsers can communicate using HyperText Transer Protocol Secure (HTTPS), and HTTP and email clients can communicate using POP3 ( Post Office Protocol version 3) and SMTP ( Simple Mail Transfer Protocol).

Not all systems that use the OSI model implement every layer.


### Next Step
- [Common Protocols And Their Uses](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Common_Protocols_And_Their_Uses.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
