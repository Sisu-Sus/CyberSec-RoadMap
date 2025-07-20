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

   Another form of HTTP is HTTP Secure. HTTPS can encrypt a user's HTTP requests and webpages, providing greated network security and preventing common cybersecurity threats.

### Next Steps
- [Common Ports and Their Uses](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Common_Ports_And_Their_Uses.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
