# CIDR

## Understanding CIDR: A Technical Overview
### Introduction to Classless Inter-Domain Routing (CIDR)
CIDR represents a significant architectural shift in IP address allocation and routing protocol design, introduced in the early 1990s as a response to limitations inherent in earlier classful network addressing schemes. The primary motivations for CIDR's adoption were to mitigate IPv4 address exhuastion and optimize routing table scalability within the Internet infastructure. Classful addressing suffered from inefficient address utilization due to fixed-size networks, leading to substantial address wastage.

### Variable Length Subnet Masking (VLSM) and CIDR's Core Functionality
CIDR fundamentally replaces the rigid Class A, B, and C network classifications with a flexible system employing Variable Length Subnet Masks (VLSM). This allows for subnetting at arbitrary granularities, optimizing address allocation to match actual network requirements. Instead of fixed subnet masks ( e.g, /8, /16, /24), CIDR enables the creation of subnets of varying sizes within a larger IP address block.

### CIDR Notation: Representation and Interpretation
CIDR introduces a concise notation to represent an IP address and its associated subnet mask as a single, unified entity. This is commonly referred to as CIDR notation. The format consists of an IPv4 address followed by a forward slash (/) and an integer representing the prefix length. For example, 192.168.1.0/24.

- **IP Address:** The 32-bit network identifier.
- **Prefix Length:** An integer value indicating the number of leading bits in the subnet mask that are set to '1'. This defines the network portion of the address.
- **Subnet Mask:** Derived from the prefix length, the subnet mask is constructed by setting the first n bits (where n is the prefix length) t0 1 and the remaining bits to 0. For /24, the corresponding subnet mask would be 255.255.255.0.

### Implications and Benefits
The adoption of CIDR has had profound implications for Internet scalability and efficiency:
- **Reduced Routing Table Size:** Aggregation of routing entries through supernetting (combining smaller networks into larger blocks) significantly reduces the size of routing tables, minimizing proagation delays.
- **Improved Address Utilization:** VLSM allows for more efficient allocation of IP addresses, reducing address wastage compared to classful addressing.
- **Enhanced Network Flexibility:** CIDR provides network administrators with greater flexibility in designing and managing their networks.


### Next Step
- [Subnet Mask]()
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resource
[https://aws.amazon.com/what-is/cidr/](https://aws.amazon.com/what-is/cidr/)

This work builds upon and explains concepts originally developed by the IETF (Internet Engineering Task Force) and other contributors to RFC 1519 and related documents.
