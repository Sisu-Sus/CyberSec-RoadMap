# Infared
### Introduction & Fundamentals
Infrared (IR) communication represents a short-range wireless data transmission method employing modulated light waves within the infrared portion of the electromagnetic spectrum, typically between approximately 700 nm and 1000 nm. Unlike radio frequency (RF) based systems like Wi-Fi or Bluetooth, IR utilizes line-of-sight (LoS) communication; a direct path between transmitter and receiver is required for reliable data transfer. This characteristic significantly impacts its range and susceptibility to interference.

### Key Characteristics:

**Electromagnetic Spectrum Positioning:** The infrared band sits between visible light and microwaves. This placement dictates the technology's behavior – it’s not directly visible but can be detected with specialized equipment.

**Modulation Techniques:** Data is encoded onto the IR carrier wave through various modulation techniques, including:
Pulse-Width Modulation (PWM): Varies the width of light pulses to represent binary data (0 or 1). Simple and common in basic remote control applications.

**Phase Shift Keying (PSK):** Changes the phase of the carrier wave to encode data. Offers improved noise immunity compared to PWM.

**Frequency Shift Keying (FSK):** Shifts the frequency of the carrier wave. Also provides better noise resilience than PWM.

**Data Rates:** IR communication typically supports relatively low data rates, ranging from a few kilobits per second (kbps) in older systems to potentially several megabits per second (Mbps) with more advanced protocols like IrDA (see below). This limitation restricts its use cases compared to higher-bandwidth wireless technologies.

**Line of Sight Requirement:** The most critical constraint is the need for a clear, unobstructed path between the IR transmitter and receiver. Any physical barrier (wall, object) will significantly attenuate or block the signal.

### Common Protocols & Standards
While "IR communication" is a general term, specific protocols govern data formatting and transmission procedures. The most notable legacy standard is:

**Infrared Data Association (IrDA):** A now largely obsolete set of standards defining interoperability between IR devices. IrDA specified various physical layers (SIRF, MIPSO) offering different ranges and speeds. While once prevalent in computer peripherals (mice, keyboards, printers), its usage has dramatically declined due to the rise of Bluetooth and Wi-Fi. IrDA's security was minimal; data transmission was generally unencrypted.

### Cybersecurity Implications & Attack Vectors
The inherent characteristics of IR communication create several potential attack vectors:

**Eavesdropping:** Because IR signals are relatively weak, they can be intercepted with readily available equipment (e.g., a smartphone camera or dedicated IR receiver). While the LoS requirement limits range, an attacker positioned within line-of-sight can potentially capture transmitted data. The lack of encryption in many legacy IrDA implementations makes this captured data easily readable.

**Mitigation:** Encryption is the primary defense against eavesdropping. However, given the low bandwidth and limited processing power of devices often using IR, implementing robust encryption algorithms can be challenging.

**Replay Attacks:** Captured IR commands (e.g., a remote control signal to unlock a door) could be replayed later to gain unauthorized access. This is particularly concerning in systems controlling physical access or critical infrastructure.

**Mitigation:** Implementing sequence numbers or timestamps within the IR transmission protocol can help detect and prevent replay attacks. However, this requires modifications to existing hardware/firmware.

**Jamming:** While difficult due to the LoS requirement, an attacker could potentially disrupt communication by shining a bright light (e.g., laser pointer) directly at the receiver, effectively jamming the signal.

**Mitigation:** Physical security measures and environmental awareness can help mitigate this risk. Signal filtering techniques might also be employed in some applications.

**Man-in-the-Middle (MITM):** In scenarios where multiple IR devices communicate, an attacker could potentially position themselves between the devices to intercept and modify messages. This is less common due to the LoS requirement but remains a theoretical possibility.

**Mitigation:** Authentication mechanisms (if supported by the protocol) can help prevent MITM attacks.

### Modern Relevance & Considerations
While IR's prevalence has diminished, it still finds use in:

**Remote Controls:** The dominant application remains consumer electronics remote controls.
Short-Range Data Transfer (NFC Alternative): Some devices utilize IR for very short-range data transfer where NFC is not available or desirable.

**Near Field Communication (NFC) Emulation:** Certain systems use modulated infrared light to emulate NFC signals, providing a low-cost alternative in specific applications.
Modern security considerations include:

**Legacy System Vulnerabilities:** Many older devices still rely on unencrypted IR communication, presenting significant vulnerabilities if these devices control sensitive functions.

**Integration with IoT Devices:** As IoT expands, the potential for IR to be used as a communication channel increases, requiring careful consideration of security implications.


### Next Step
- [OS-Independent Troubleshooting](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Fundamental_IT_Skills/OS_Independent_Troubleshooting.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

## Resource 
- [https://www.larksuite.com/en_us/topics/cybersecurity-glossary/infrared](https://www.larksuite.com/en_us/topics/cybersecurity-glossary/infrared)
- [https://en.wikipedia.org/wiki/IEEE_802.15.4](https://en.wikipedia.org/wiki/IEEE_802.15.4)
