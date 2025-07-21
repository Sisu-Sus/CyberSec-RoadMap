# Windows

## The Windows Operating System - Security Considerations
This document provides a technical overview of the Microsoft Windows operating system, focusing on security-relevant aspects and potential attack vectors. It assumes a foundational understanding of networking principles, common security threats, and basic OS concepts.

### Architecture & Core Components
Windows is a hybrid kernel architecture combining elements of monolithic and microkernel designs. Key components include:
| Component | Description |
|---|---|
| Kernel | The core of the OS, responsible for memory management, process scheduling, device drivers, and system calls. Vulnerable drivers are a frequent attack vector (see section 4). |
| Hardware Abstraction Layer (HAL) | Provides an interface between the kernel and hardware, simplifying driver development but also creating a potential point of compromise if exploited. |
| Executive | A collection of core subsystems providing essential OS services like memory management, process object management, I/O manager, etc. |
| User Mode Subsystems | These include Win32 (the traditional Windows API), POSIX subsystem (for Unix-like applications), and others. Applications run within these subsystems with restricted privileges. |
| Windows Registry | A hierarchical database storing configuration settings for the OS and applications. Its structure and accessibility make it a target for malware persistence mechanisms and privilege escalation attacks. |
| System File Protection (SFP) | Designed to prevent unauthorized modification of critical system files, but can be bypassed with sufficient privileges or vulnerabilities. |

### Security Features & Mechanisms
Windows incorporateds several security features:
| Feature/Mechanism | Description |
|---|---|
| User Account Control (UAC) | A mechanism requiring administrative approval for actions that require elevated privileges. While intended to mitigate unauthorized changes, UAC can be bypassed through social engineering or exploiting vulnerabilities in applications requesting elevation. |
| Windows Defender | A built-in antivirus and anti-malware solution. Effectiveness depends on signature updates and behavioral analysis capabilities; evasion techniques are constantly evolving. |
| BitLocker Drive Encryption | Full disk encryption protecting data at rest. Key management is critical – compromised recovery keys render the protection ineffective. |
| Windows Firewall | A stateful firewall controlling network traffic based on predefined rules. Configuration errors can create vulnerabilities. |
| Secure Boot | Verifies digital signatures of boot loaders and operating system components to prevent rootkits from loading during startup. Can be bypassed with compromised firmware or UEFI exploits. | 
| Credential Guard | Uses virtualization-based security (VBS) to isolate LSA (Local Security Authority) processes, protecting credentials from theft. Requires specific hardware capabilities. |
| Device Guard/Hypervisor-Protected Code Integrity (HVCI) | Enforces code integrity policies, preventing unsigned or untrusted applications from running. Can impact compatibility with older software. |

### Common Attack Vectors & Vulnerabilities
**Exploitation of Kernel Mode Drivers:** Drivers operate in a privileged mode and are often poorly written, making them attractive targets for attackers to gain system-level control. DoubleFault exploits are a prime example.
**Privilege Escalation:** Exploiting vulnerabilities or misconfigurations (e.g., weak ACLs, insecure services) to elevate user privileges from standard user to administrator or SYSTEM level. Tools like Mimikatz are frequently used for credential theft and privilege escalation.
**Malware Persistence Mechanisms:** Malware utilizes various techniques to ensure survival across reboots, including registry modifications, scheduled tasks, startup folders, and driver installation.
**Phishing & Social Engineering:** Tricking users into executing malicious code or revealing credentials. UAC bypasses are often achieved through social engineering.
**Remote Code Execution (RCE):** Exploiting vulnerabilities in network services or applications to execute arbitrary code on the target system. EternalBlue, used in WannaCry ransomware, is a notable example.
**Pass-the-Hash/Pass-the-Ticket:** Stealing password hashes or Kerberos tickets to authenticate as another user without knowing their actual password.
**DLL Hijacking:** Replacing legitimate DLL files with malicious ones to execute code when an application loads the hijacked library.
**Zero-Day Exploits:** Attacks exploiting previously unknown vulnerabilities before a patch is available.




### Next Step
- [Linux](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Operating_Systems/linux.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

## Resource / Study Sources
- [https://learn.microsoft.com/en-us/windows/security/](https://learn.microsoft.com/en-us/windows/security/)
- [National Vulnerability Database (NVD)](https://nvd.nist.gov/)
- SANS Institute Courses (SEC504, SEC617): While paid courses, they offer in-depth coverage of Windows security. Look for related materials online.
- Cybersecurity Blogs & Forums: Search for articles on specific Windows vulnerabilities and attack techniques (e.g., "Windows privilege escalation," "Windows kernel exploitation").

