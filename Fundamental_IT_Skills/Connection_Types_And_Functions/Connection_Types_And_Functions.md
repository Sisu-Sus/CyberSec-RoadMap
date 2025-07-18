# Connection Types and their Functions
## Roadmap.sh Summary
There are several types of network connections that enable communcication between devices. Methods listed are:

- Ethernet: A wired connection type commonly used in LAN networks. Ethernet is ideal for businesses and environments where reliability is crucial, offering speeds from 100Mbps to several Gbps

- Wi-Fi: Wireless connection that enables devices to connect to a network. While convenient, it can be less reliable and slower than ethernet.

- Bluetooth: A short range wireless technology primarily used for peripherals such as headphones, keyboards, speakers and other devices. Bluetooth is much more vital for personal device communications rather than large network communications.

- Fiber-Optic: Uses light signals to transmit data at very highspeeds over long distances. Fiber is much faster and more reliable than trabitional copper cables, but it is also more expensive to implement.

- Cullular Connections: Cellular connections such as 4G and 5G, allow mobile devices to connect through cellular networks, speeds and reliability vary depending on network.

Each connection type plays a specific role, balancing factors like speed, distance, and convenience.

### Resources
[https://www.techtarget.com/searchnetworking/definition/Ethernet](https://www.techtarget.com/searchnetworking/definition/Ethernet)

## Ethernet
### How Ethernet Works
IEEE specifies in the IEEE 802.3 family of standards that the Ethernet protocol touches both Layer 1 (physical layer) and Layer 2(data link layer) on the Open Systems Interconnections (OSI) model.

Etheret defines two units of transmissions: packet and frame. The frame includes the paylod as well as physical Media Access Control (MAC) addresses of both sender and reciever, Virtual LAN (VLAN) tagging and quality of service information, and error correction information to detect transmission problems. Each frame is wrapped in a packet that contains several byte of information to establish the connection and mark where the fram starts. Engineers at Xerox first developed Ethernet in the 1970's. Ethernet initally ran over coaxial cables. Early Ethernet connected multiped devices into network segments through hubs-- Layer 1 devices responsible for transporting network data--using either daisy or star topology. Currently, a typical Ethernet LAN uses special grades of twisted-pair cables or fiber optic cabling.

I feel it is worth noting that if two devices share a hub and try to transmit data at the same time, packet collision occurs and creates connectivity problems. To alleviate this, IEEE developed the Carrier Sense Multiple Access with Collision Detection protocol. 

This is where things like IEEE 802.3 and collision domains get fascinating. If you're into signal-level behavior and medium access control, I took a deep dive in in my [Signal Path notes](https://github.com/Sisu-Sus/Signal_Path/blob/main/signal_path.txt).

Later, Ethernet hubs largely gave way to network switches. Becasue a hub cannot descriminate between points on a network segment, it can't send data directly from point A to point B. Instead, whenever a network device sends a transmission via an input port, the hub copies the data and distributes it to all available output ports.

In contrast, a switch intelligently sends any given port only the traffic intended for its devices rather than copies of any and all the transmissions on the network segment, thus improving security and efficiency. Like with other network types, invloved computers must include a Network Interface Card (NIC) to connect to Ethernet.

### Next Step
- [NFC](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Fundamental_IT_Skills/Connection_Types_And_Functions/NFC.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

















