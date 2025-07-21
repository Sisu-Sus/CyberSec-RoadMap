# VLAN

## Introduction to Virtual Local Area Networks (VLANs)
Virtual Local Area Networks (VLANs) represent a fundamental network virtualization techique enabling the logical partioning of a physical infrastructure. This segmentation allows for the creation of multiple, isolated broadcast domains operating concurrently on shared switching hardware. VLAN membership is typically determined by organization function, application requiements, or security policies, irrespective of device physical location within the network topology.

### Technical Benefits and Funtionality
The implementation of VLANs yield several key operational advantages:
- Broadcast Domain Containment: VLANs significantly reduce unnecessary broadcast traffic by limiting its scope to members of a specific VLAN. This improves overall network performance and reduces contention for shared resources.

- Enhanced Security Posture: Isolation between VLANs restricts unauthorized access and lateral movement within the network, enhancing security for sensitive systems and data. This isolation is achieved through Access Control Lists (ACLs) applied at Layer 3 interfaces or via port-based VLAN assignments.

- Network Agility & Scalability: VLANs facilitate flexible network design and management by allowing logical groupings of devices without requiring physical relocation or re-cabling. This promotes scalability and simplifies administrative tasks during network modifications.

IEEE 802.1Q Tagging Mechanism
The predominant standard for VLAN configuration is IEEE 802.1Q. This standard defines a tagging mechanism that inserts a four-byte (32-bit) tag into the Ethernet frame header. This tag, known as the VLAN ID (VID), identifies the VLAN to which the frame belongs. The VID ranges from 0 to 4095, with specific values reserved for management purposes (e.g, native VLAN). Trunk ports, capable of carrying traffic for multiple VLANs, utilize this tagging mechanism to encapsulate frames belonging to different VLANs within a single physical link. The standard also defines Priority Code Point (PCP) bits within the 802.1Q tag, enabling Qaulity of Service (QOS) prioritization based on VLAN membership


### Next Step
- [DMZ]()
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resources
[https://www.solarwinds.com/resources/it-glossary/vlan](https://www.solarwinds.com/resources/it-glossary/vlan)
