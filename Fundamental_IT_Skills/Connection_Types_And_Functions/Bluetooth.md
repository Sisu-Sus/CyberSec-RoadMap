---
# Bluetooth
---
## Roadmap.sh Summary
Bluetooth is a short-range wireless technology standard used for exchanging data between fixed and mobile devices over short distances. While it offers convenience for connecting peripherals and transferring information, it also presents several security concerns in the cybersecurity landscape. Bluetooth vulnerabilities can potentially allow attackers to intercept comunications, execute malicious code, or gain unauthorized access to devices. Common attacks include bluejacking, bluesnarfing, and bluebugging. To mitigate these risks, cybersecurity professionals recommend regularly updating device firmware, using the latest Bluetooth protocols, enabling encryption, and turning off Bluetooth when not in use. Depsite ongoung security improvements, Bluetooth remains an attack vector that requires vigilant monitoring and protection in both personal and enterprise environments.

### Resource
[https://www.zenarmor.com/docs/network-basics/what-is-bluetooth](https://www.zenarmor.com/docs/network-basics/what-is-bluetooth)

### How does Bluetooth work?

Bluetooth uses non-ionizing electromagnetic waves in the radio frequenzy band between 2.40 GHz and 2.48 GHz as a low-power, short-distance radio transmission system. To convert data into a format that can be transferred by Bluetooth, the Bluetooth signal is first processed by software using a compression mechanism called a codec. To "pair", or link, neighboring devices, Bluetooth uses short-range radio waves. A computer chip in devices with Bluetooth functionality transmits a signal, so Bluetooth devices can identify one another this way.

The maximum communication distance for blue tooth varies depending on the environment and device class. The maximum ranfe for Class 1 devises is up to a hundred meters; Class 2 devices are limited to ten meters; and Class 3 devices are limited to 1 meter. However, for the majority of devices, the Bluetooth connection's range is around ten meters, Depending on the electromagnetic environment or barriers, the maximum distance for communication will change. You can achieve a range of up to a hundred  meters outside, in a wide-open space, although that is an uncommon circumstance. Obstacles like concrete walls in a household can considerably restrict the distance.

Various integrated elements of Bluetooth technology enhance the technology's security are listed below;

- Adaptive Frequency Hopping: Bluetooth's frequency hopping employs the 2.4 GHz ISM band, which has 79 channels and allows for hops at a rate of 1600 per second. Existing frequencies are omitted from the hopping. Jamming and interference are bother reduced by the ability to frequency hop.

- Pairing: Pairing permits communication between devices. For a pairing request to be made, the BD_ADDR address of a device is also hidden.

- E0 Cipher Suite: The cipher typically uses stream ciphering and has a key length of 128 bits.

### Bluetooth Attacks

- Bluesnarfing: In a bluesnarfing attack, the victim's Bluetooth software for drivers is vulnerable, allowing the hacker to access all the data on the victim's device. It has the power to turn off the battery or disable the device's features.

- Bluejacking: In a different scenario, when a Bluetooth device uses spam advertising to hijack another, is known as bluejacking. It may result in the installation of malware or the transfer of undesirable data.

- Bluebugging: In a bluebugging attack, a cybercriminal uses a covert Bluetooth connection to acquire backdoor access to your device, allowing them to eavesdrop on you and access your personal information. In some cirumstances, a hacker uses a Denial of Service (DoS) attack to overwhelm and disable a Bluetooth-enabled device.

- BlueSmacking: A DoS attack called BlueSmacking arms to overwhelm your device and shut it down. Large data packets are sent to your device by cybercriminals to penetrate. Once your device is turned off, hackers will use BlueSmacking as a launchpad for more serious attacks. Once restarted, your device will usually get back to normal.

- Car Whispering: Another Bluetooth security flaw known as car whispering attacks automobile radios with Bluetooth functionality. Hackers employ this method to listen to phone calls as well as conversations inside the vehicle.

### How to Prevent Bluetooth Attacks

- Don't set up pairing via public connections. Always pair two devices from a secure location when doing so for the first time.
- When not in use, turn off Bluetooth
- Steer clear of Bluetooth while exchanging private information
- Be cautios about who you share your Bluetooth connection with
- Always update your operating system and drivers when needed
- Removing previous uneccessary Bluetooth connections is advised
- Ensure that your device is untracable
- To prevent Bluetooth spying, set your device to undiscoverable

### Next Step
- [Infared](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Fundamental_IT_Skills/Connection_Types_And_Functions/Infared.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
