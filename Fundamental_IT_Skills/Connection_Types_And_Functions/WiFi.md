# Wi-Fi
## Deep Dive: Wireless Local Area Networks (WLANs) - IEEE 802.11 & Security Considerations

This document provides a technical overview of Wireless Local Area Networks (WLANs), commonly referred to as Wi-Fi, focusing on the underlying technology and associated security implications. It assumes a basic understanding of networking principles such as TCP/IP and common attack vectors.

### Technology Fundamentals: IEEE 802.11 Standards

Wi-Fi operates under the umbrella of the IEEE 802.11 standards, which define protocols for wireless data transmission.  These standards specify aspects like modulation techniques, frequency bands, data rates, and security mechanisms. Key versions include:

* **802.11b (Legacy):** Introduced in 1999, operating primarily on the 2.4 GHz band with a maximum theoretical speed of 11 Mbps.  Considered obsolete due to lower speeds and increased susceptibility to interference.
* **802.11a (Legacy):** Also introduced around 1999, but using the 5 GHz band with a theoretical maximum speed of 54 Mbps. Less common than 802.11b initially due to higher hardware costs.
* **802.11g:**  A significant improvement over 802.11b, operating on the 2.4 GHz band and offering speeds up to 54 Mbps while maintaining backward compatibility with 802.11b devices.
* **802.11n (WiFi 4):** Introduced in 2009, utilizing both 2.4 GHz and 5 GHz bands.  Introduced MIMO (Multiple-Input Multiple-Output) technology, allowing for multiple antennas to transmit and receive data simultaneously, significantly increasing throughput – theoretically up to 600 Mbps.
* **802.11ac (WiFi 5):** Introduced in 2013, exclusively using the 5 GHz band.  Expanded channel bandwidths (up to 160 MHz) and incorporated MU-MIMO (Multi-User MIMO), enabling simultaneous data transmission to multiple devices, improving network efficiency.
* **802.11ax (WiFi 6):** Introduced in 2019, operating on both 2.4 GHz and 5 GHz bands.  Focuses on improved performance in dense environments through technologies like OFDMA (Orthogonal Frequency-Division Multiple Access) which allows for more efficient resource allocation to individual devices. Also includes Target Wake Time (TWT) for power saving in IoT devices.
* **802.11be (WiFi 7):** The latest standard, introducing features such as Multi-Link Operation (MLO) and Enhanced Relaying for improved latency and throughput.

**Frequency Bands:**  The 2.4 GHz band is more susceptible to interference from other devices (e.g., Bluetooth, microwaves), while the 5 GHz band generally offers less congestion but has a shorter range due to higher frequency attenuation.

### WLAN Architecture & Components

A typical WLAN consists of:

* **Wireless Router/Access Point (AP):**  The central device that creates and manages the wireless network. It connects to a wired network (e.g., an internet service provider's connection) and broadcasts a wireless signal.
* **Station (STA):** Any device capable of connecting to the WLAN, such as laptops, smartphones, or IoT devices.
* **Service Set Identifier (SSID):** The name of the Wi-Fi network, broadcasted by the AP.  While often used interchangeably with "network name," it's a specific identifier within the 802.11 standard.
* **Basic Service Set (BSS):** A single WLAN network consisting of one AP and all associated STAs.
* **Extended Service Set (ESS):** Multiple BSSs interconnected via wired links, forming a larger WLAN network.

### Security Protocols & Vulnerabilities

Early Wi-Fi networks relied on WEP (Wired Equivalent Privacy), which was quickly found to be vulnerable to various attacks due to weak encryption algorithms.  Subsequently, WPA (Wi-Fi Protected Access) and WPA2 were introduced:

* **WPA:** Utilized TKIP (Temporal Key Integrity Protocol) for improved security over WEP but still had weaknesses.
* **WPA2:** Introduced AES (Advanced Encryption Standard) with CCMP (Counter Mode Cipher Block Chaining Message Authentication Code Protocol), significantly strengthening encryption and authentication.  Supports both Personal (PSK - Pre-Shared Key) and Enterprise (802.1X/EAP) modes.
* **WPA3:** The latest standard, offering enhanced security features such as Simultaneous Authentication of Equals (SAE) for more robust password protection against offline dictionary attacks and improved encryption protocols.

**Common Attack Vectors & Mitigation Strategies:**

* **Evil Twin Attacks:**  Attackers create a rogue AP with an SSID mimicking a legitimate network to lure users into connecting. *Mitigation:* Verify the authenticity of SSIDs, use VPNs on public networks.
* **Wardriving/Warwalking:** Using mobile devices or vehicles to scan for open or poorly secured Wi-Fi networks. *Mitigation:*  Disable SSID broadcasting (though not foolproof), implement strong passwords and WPA2/WPA3 encryption.
* **Dictionary Attacks:** Brute-forcing the pre-shared key (PSK) used in WPA/WPA2 Personal mode. *Mitigation:* Use long, complex passphrases; enable WPA3 SAE.
* **Deauthentication Attacks:**  Attackers send deauthentication frames to disconnect clients from the network, potentially forcing them to reconnect and retransmit credentials. *Mitigation:* Implement intrusion detection systems (IDS) to detect suspicious traffic patterns.
* **KRACK Attack (Key Reinstallation Attack):** A vulnerability in WPA2 that allows attackers to decrypt network traffic.  While largely mitigated by firmware updates, older devices may remain vulnerable. *Mitigation:* Ensure all devices are running the latest firmware.



### Future Trends

The evolution of Wi-Fi continues with a focus on:

* **Higher Speeds & Lower Latency:** Driven by increasing bandwidth demands for applications like AR/VR and cloud gaming.
* **Improved Network Efficiency:**  Optimizing resource allocation in dense environments to support the growing number of connected devices.
* **Enhanced Security:** Addressing emerging threats and vulnerabilities with stronger encryption protocols and authentication mechanisms.
* **Integration with IoT:** Facilitating seamless connectivity and management of a vast array of smart devices.



### Next Step
- [Bluetooth](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Fundamental_IT_Skills/Connection_Types_And_Functions/Bluetooth.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resource
[https://computer.howstuffworks.com/wireless-network.htm](https://computer.howstuffworks.com/wireless-network.htm)






















