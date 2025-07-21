# Common Protocols And Their Uses

## Roadmap.sh Summary:
Networking protocols are essential for facilitating communication between devices and systems across networks. In cybersecurity, understanding these protocols is crucial for indentifying potential vulnerabilities and securing data transmission. Common protocols include TCP/IP, the foundation if internet communication, which ensures reliable data delivery. HTTP and HTTPS are used for web browsing, with HTTPS providing encrypted connections. FTP and SFTP handle file transfers, while SMTP, POP3, and IMAP manage email services. DNS translates domain names to IP addresses, and DHCP automates IP address assignment. SSH enables secure remote access and management of systems. Other important protocols include TLS/SSL for encryption, SNMP for network manegment, and VPN protocols like IPsec and OpenVPN for secure remote connections. Cybersecurity proffessionals must be well-versed in these protocols to effectively monitor network traffic, implemement security measures, and respond to potential threats targeting specific protocol vulnerabilities.

### Resource 
[https://www.techtarget.com/searchnetworking/feature/12-common-network-protocols-and-their-functions-explained](https://www.techtarget.com/searchnetworking/feature/12-common-network-protocols-and-their-functions-explained)

### 15 Common Protocols

1. Domain Name System

   DNS is an application layer protocol that acts as the internets phone directory. Each device on the internet has a unique and corresponding IP address, similar to a phone number. However, its hard for humans to remember numerical labels, so DNS uses a resolution process to solve this problem.

   When a user types a domain name, such as google.com, into a web browser, the computer sends a request to a DNS nameserver to find the corresponding IP address so the user's computer connects to the correct server. DNS servers also help with the reverse process, resolving numerical IP addresses to their corresponding domain names.

   DNS is essentlly a directory of fully qualified domain names (FQDNs) and their corresponding IPv4 or IPv6 addresses. It contains various types of records including the following:

   - A Record: An A record is used to map an FQDN to an IPv4 address

   - AAAA Record: This record maps an FQDN to an IPv6 address
  
   - Canonical Name Record: A CNAME record works as an alias and maps one domain name to another.
  
   - Mail Exchanger Record: An MX record lists mail servers for domain mail exchange.
  
   - Pointer Record: A PTR record is a reverse lookup that maps an IP address to an FQDN
  
2. Dynamic Host Configuration Protocol (DHCP)
   DHCP Automates the process of assigning IP addresses to network endpoints so they can communicate with other nwtork devices over IP. Whenever a device joins a network with a DHCP server for the first time, DHCP automatically assigns it a new IP address and continues to do so each time a device moves locations on the netowrk. Without DHCP, network admins must manually assign IP addresses to each new device.

   When a device connects to a network, a DHCP handshake takes place. In this handshake process, the device and DHCP server communicate using the following steps:
   1. The device establishes a connection and sends a DHCP broadcast request on the LAN to find a DHCP server that could assign an IP address to it.
   2. One or more DHCP servers respond, offering available IP addresses.
   3. The device selects an address and formally requests it.
   4. If the server approves, it acknowledges the request and records the device's IP address, MAC address, and other relevant details, such as the hostname and subnet mask
   5. The IP address is leased to the device for a short period, after which the lease expires.
   6. Once 50% of the lease time has elapsed, the device can begin requesting a lease renewal
  
   Besides dynamically assigning IP addresses, a DHCP server also passes essential network configuration information, such as subnet masks, defualt gateways, DNS server addresses and domain names, to requesting device. This enables devices to communicate seamlessly within both local and external networks.

3. File Transfer Protocol
     FTP is a client-server protocol that transfers files between a client and a server and operates over TCP/IP. It uses two communication channels: the command channel and the data channel. Clients request files through the command channel and receive access to download, edit and copy the gile, among other actions, through the data channel.

      While FTP is a file-transferring protocol, it doesn't encrypt data and send it in plainetext, making it vulnerable to security risks. Therefore, most businesses opt for file transfer protocols that are secure, such as Secure FTP, to safely transfer files over a network.

4. Hypertext Transfer Protocol
   HTTP operates on a client-server model and is the primary method by which web browsers and servers communicate to share information over the internet. While its main purpose is to transfer webpages and provide other resources during web browsing, it is also able to transfer data, facilitating file sharing.

   Another form of HTTP is HTTP Secure. HTTPS can encrypt a user's HTTP requests and webpages, providing greateR network security and preventing common cybersecurity threats, such as Man In The Middle (MITM) attacks.

   HTTPS has become the new standard for web browsing.

5. Simple Mail Transfer Protocol
   SMTP--The most widely used email protocol--is part of the TCP/IP suite and control how email clients send users' email messages. Email servers use SMTP to send email messages from the client to the email server to the reveiving email server. However, SMTP doesn't control how email clients receive messages -- just how clients send messages. Essentially, it's just a mail delivery protocol and not used for retrieval of messages.

   That said, SMTP requires other protocols to ensure email messages are sent and received properly. It can work with Post Office Protocol 3 or Internet Message Access Protocol, bot of which control how an email server receives email messages.

6. Simple Network Management Protocol
   SNMP is a network management protocol that helps network admins manage and monitor devices, such as routers, switches, printers and firewalls. It gathers device information to monitor network performance and health. Network administrators often use SNMP to detect and trouble shoot network issues.

   SNMP uses a manager-agent model and the following components:
   - SNMP manager: This is the central system that communicates with the agents and requests or updates information.
   - SNMP agent: This is a software component installed on devices such as routers and switches and sends information to the manager
   - Management information base: The MIB acts as a database and contains device information.
  
   Here is how SNMP works:
   1. Manager Request: The SNMP manager sends a request using the SNMP protocol to an SNMP agent on a device. The request includes information, such as CPU use and interface status.
  
   2. Agent Response: The SNMP agent retrieves the requested information from the MIB and sends it back to the manager in an SNMP response.
  
   3. Manager Action: The manager is now able to display the information, log it or use it to trigger an action. For example, it can send an alert or change a configuration
  
7. Secure Shell
   The SSH protocol provides a way to securely connect to and send commands to a device or an insecure network, such as the internet. It uses cryptography for authentication and establishes an encrypted digital tunnel between devices, protecting communication from eavesdropping and tampering.

8. Telnet
   Telnet is designed for remote connectivity. It establishes connections between a remote endpoint and a host machine to enable a remote session. Telnet prompts the user at the remote endpoint to log on. Once the user is authenticated, Telnet gives the endpoint access to network resources and data at the host computer.

   **Telnet has existed since the 1960s and was the first draft of the modern internet. However, Telnet lacks sophisticated security protection as it transmits data in plaintext, including usernames and passwords.**

9. Transmission Control Protocol
    TCP is a connection-oriented transport layer protocol that offers reliable delivery throught packet sequencing, retransmission of lost packets and flow control.

   It arranges packets in order after IP has delivered them. TCP numbers individual packets because IP can send    packets to their destinations through different routes and get the packets out of order. TCP checks and reassembles the packets at the destination before delivering them to the application. IP's job is complete once the packet reaches the destination host; TCP's job begins at this point. It takes over to ensure reliable and in-order delivery to the application.

   TCP also detects errors in the sending process, including if any packets are missing based on TCP's numbered system, and it requires IP to retransmit missing packets. Through this process, the TCP/IP suite controls communication across the internet.

10. User Datagram Protocol
    UDP is an alternative to TCP and also works with IP to transmit time-sensitive data. UDP enables low-latency data transmissions between internet applications, making it ideal for real-time applications where low latency is important, but some data loss is acceptable, such as with VoIP, audio or video streaming, and onling gaming.

    UDP solely transmits packets and doesn't offer packet sequencing, organizing or retransmission. TCP, on the other hand, transmits, organizes and ensures the packets arrive. While UDP is a lightweight protocol and works faster than TCP, it's also less reliable.

11. Address Resolution Protocol
    ARP maps IP addresses to physical MAC address of devices and vice versa within a LAN so devices can communicate with one another. ARP is necessary because IP and MAC addresses are different lengths and operate on different layers of the OSI model.

    These addresses must be mapped for proper network communication and data transfer among connected devices. ARP isn't required every time devices attemp to communicate because the LAN's hsot system maps and stores the associations in its ARP cache. As a result, the ARP resolution process is mained used when new devices join the network.

12. Internet Control Message Protocol
    ICMP is a supporting protocol on the internet layer of the TCP/IP model. It's mainly used for network diagnostics, troubleshooting, error reporting and some limited control functions between network devices. It helps identify network connectivity issues and manage the flow of data packets. However, it doesn't transfer data, such as the content of a webpage or an email.

    ping and traceroute commands both use ICMP to test connectivity and trace packet routes. Common ICMP messages include the following:

    - Echo request and Echo Reply
   
    - Destination Unreachable
   
    - Time Exceeded
   
    - Redirected Message
   
13. Internet Protocol
    IP functions similar to a postal service. When users send and receive data from their devices, the data gets spliced into packets. Packets are like letters with two IP addresses: one for the sender and one for the recipient,

    After the packet leaves the sender, it goes to a gateway or router, similar to a post office, which guides it towards its destination. Packets continue to travel through several gateways until they reach their destinations.

    IP is commonly paired with TCP to ensure reliable data delivery. IP sends packets to their destinations as they arrive, while TCP makes sure they are in the correct sequence since IP is connectionless and can deliver them out of order if they take different routes across the network.

14. Border Gateway Protocol
    The Internet's functionality hinges on critical routing protocol called BGP (Border Gateway Protocol). BGP enables communication and coordination between independently managed networks, known as Autonomous Systems (ASes). An AS represents a collection of IP addresses and network segments governed by a single organization - this could be an ISP, a large corporation, a universtiy, or even a government body - that dictates its own routing rules.

     Data packets traversing the internet often need to pass through several ASes to reach their final destination. Within each AS, routers utilize BGP to share information about the networks they control with nerighboring devices. This sharing extends beyond an AS's boundaries as edge routers connect and exchange data, building a map of reachable networks. This internal routing is handled by IBGP (Internal Border Gateway Protocol), while communication between different ASes relies on EBGP (External Border Gateway Protocol)

    BGP's dynamic nature allows it to adapt to changes within the network; when routers are added or removed. BGP automatically updates routing tables and informs connected networks. The selection of optimal routes is based on factors like the number of ASes a packet must traverse and organizational policies. While primarily known for its role in internet-wide routing, BGP also plays an important part within large data centers, ensuring efficient traffic flow by advertising network availibility.

15. Open Shortest Path First
    OSPF (Open Shortest Path First) is a dynamic routing protocol crucial for efficient data transmission across IP networks. It works in conjunction with IP, which strives to deliver packets along the most expediant route - a goal that OSPF directly addresses. Essentially, OSPF prioritzes establishing the fastest or shortest path for packet delivery. A key function of OSPF is maintaining and updating routing tables--essentially, maps dictating where data should travel--and proactively notifying routers about any changes within these tables or the network itself.

    Unlike old protocols like RIP(Routing Information Protocol), which relies on a simple hop count to determine routes, OSPF offers a more advanced and scalable solution. RIP's periodic updates - ocurring every 30 seconds - are inefficient compared to OSPF's approach of transmitting updates only when changes occur and focusing solely on the affected portions of the routing table. Furthermore, OSPF employs sophisticated metrics beyond hop counts, considering factors like bandwidth availibility, netowrk latency(delay), and link cost to determine optimal paths.

### Next Steps
- [Common Ports and Their Uses](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Common_Ports_And_Their_Uses.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
