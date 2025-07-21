# Subnet Mask

## Understanding the Subnet Mask
In IP networking, a subnet mask is a 32-bit numerical value employed to delineate the network prefix from the host identifier within an IPv4 address. This partitioning facilitates the logical segmentation of a larger IP network into smaller, more manageable subnets. The subnets mask's bit pattern directly corresponds to the contigous block of '1' bits representing the network portion of the address; remaining bits are represented by '0' and define the host portion.

The primary function of a subnet mask is to enable routers and hsots to determine whether a destination IP address resides on the same local network segment or rquires transmission across an inter-network gateway. This determination is achieved through a bitwise AND operation between the source IP address, the destination IP address, and the subnet mask. A matching result indicates that both addresses belong to the same network.

Subnetting provides several operational advantages including optimized IP address utilization by reducing overall address space required for a given number of devices, localized broadcast domains which minimize unnecessary traffic propagation, and enhanced network security through granular access control policies implemented at the subnet level. Common examples include masks such as 255.255.255.0 (equivalent to a /24 CIDR notation) and 255.255.0.0 (/16), which represent different levels of network segmentation granularity.

A foundational understanding of subnet mask principles is essential for effective netowrk administration tasks, including IP address allocation, routing configuration, troubleshooting connectivity issues, and implementing robust network security architectures through logical isolation.

### Next Step
- [Default Gateway]()
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
### Resources
[https://www.spiceworks.com/tech/networking/articles/what-is-subnet-mask/](https://www.spiceworks.com/tech/networking/articles/what-is-subnet-mask/)

