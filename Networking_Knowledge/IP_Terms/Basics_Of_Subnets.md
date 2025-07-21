# Basics Of Subnets

## Demystifying Subnetting: Your Guide to Network Segmentation
Ever wondered how massive networks stay organized and efficient? The secret lies in a technique called subnetting. Think of it like dividing a large city into distinct neighborhoods - each with its own purpose and rules. In the world of computer networking, subnetting does exactly that: it breaks down a big network into smaller, more manageable pieces we call 'subnets.'

Why is this important? Well, imagine trying to deliver mail to every house in a sprawling metropolis without any organized districts! It would be chaos. Subnetting helps prevent that kind of congestion on your network. By dividing the network, you reduce unneccasary 'broadcast traffic' - essentially, messages sent out to everyone - and give administrators more control over how IP addresses are assigned.

### How Does It Work? The Basics:
Every device connected to a network has an IP address--its unique identifier. This address is like a combination of a street name (the network portion) and a house number (the host portion). Subnetting allows us to adjust how we divide that address creating muliple 'neighborhoods' within the larger network.

A subnet mask acts as the key to this process. It tells your computer which part of the IP address identifies the network itself and which part is for individual devices (hosts) on that subnet. By tweaking the subnet mask, you can create numerous subnets from a single original network - each with its own limited number of available addresses.

### Why Use Subnetting? Real-World Benefits:

- Improved Performance: Less broadcast traffic means faster data transmission and a smoother online expeirence.

- Enhanced Security: Segmenting your network allows you to isolate sensitive areas, making it harder for threats to spread. Imagine having seperate security zones within that city.

- Efficient IP Address Management: Subnetting helps organizations make the most of their limited pool of IP addresses.

- Better Traffic Control: You can direct data flow more effectively, preventing bottlenecks and optimizing network performance.


**--Authors Note--** I bought a $20 edge-router and did a whole subnet practice in my homelab. If anyone reads this and feels like a writeup on that would greatly help them please reach out so I can do that for you.

### Resources
- [https://roadmap.sh](https://roadmap.sh/cyber-security)
- [https://www.cbtnuggets.com/blog/technology/networking/networking-basics-what-is-ipv4-subnetting](https://www.cbtnuggets.com/blog/technology/networking/networking-basics-what-is-ipv4-subnetting)

### Next Step
- [Public vs Private IP Adresses](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/IP_Terms/Public_vs_Private_IP_Addresses.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
