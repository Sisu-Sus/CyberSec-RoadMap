# Operating Systems

### Introduction: The OS as a Critical Attack Surface
The operating system (OS) serves as the foundational layer upon which all other software and services operate. Consequently, it represents a critical attack surface. Compromise of an OS can lead to complete system control, data exfiltration, lateral movement within a network, and ultimately, significant business disruption. Understanding OS security requires moving beyond basic user account management and delving into core architectural components and their vulnerabilities.

## Core Security Concepts & Architectural Considerations
**Kernel Mode vs. User Mode:** Modern OSes employ a privilege separation model. The kernel, the heart of the OS, operates in kernel mode with unrestricted access to hardware and memory. User applications run in user mode, restricted by the kernel's protection mechanisms. Exploits often aim to elevate privileges from user mode to kernel mode (privilege escalation).

**Memory Management:** OSes utilize virtual memory, paging, and segmentation to manage memory resources. Vulnerabilities like buffer overflows (heap overflows, stack overflows) arise when applications write beyond allocated memory boundaries, potentially overwriting critical data or code within the OS's address space. Address Space Layout Randomization (ASLR) is a mitigation technique that randomizes memory addresses to make exploitation more difficult.

**Access Control Mechanisms:** OSes enforce access control policies using mechanisms like:
  - **Discretionary Access Control (DAC):** User-based permissions (e.g., file ownership, ACLs). Vulnerable to privilege escalation if user accounts are compromised or misconfigured.
  - **Mandatory Access Control (MAC):** System-wide policies that dictate access based on labels assigned to users and resources (e.g., SELinux, AppArmor). More restrictive than DAC but can be complex to manage.
  - **Role-Based Access Control (RBAC): Assigning permissions based on user roles within an organization.

**Authentication & Authorization:** Secure authentication is paramount. Common methods include:
  - **Password-based Authentication:** Susceptible to brute-force attacks, dictionary attacks, and credential stuffing. Multi-factor authentication (MFA) significantly strengthens this.
  - **Biometric Authentication:** Fingerprint scanning, facial recognition – introduces new vulnerabilities related to biometric data security.
  - **Certificate-Based Authentication:** Uses digital certificates for verification; more secure than passwords but requires robust certificate management.

### Common Attack Vectors & Vulnerabiiities
**Kernel Exploits:** These are the most severe as they grant direct control over the OS. Examples include:
  - **Null Pointer Dereferences:** Occur when code attempts to access memory at an invalid address, often leading to crashes or arbitrary code execution.
  - **Use-After-Free (UAF):** Occurs when a program accesses memory that has already been freed, potentially allowing attackers to overwrite data and gain control.
  - **Double Free:** Occurs when the same memory location is freed twice, leading to corruption of heap metadata.

**Driver Vulnerabilities:** Device drivers act as intermediaries between hardware and the OS kernel. Poorly written or outdated drivers are a frequent source of vulnerabilities.

**System Call Exploits:** System calls provide an interface for user-space applications to request services from the kernel. Flaws in system call handling can be exploited.

**Privilege Escalation Attacks:** Techniques used to gain higher privileges than initially assigned:
  - **Exploiting SUID/SGID binaries:** SUID (Set User ID) and SGID (Set Group ID) bits allow a program to run with the permissions of its owner or group, respectively. Misconfigured SUID/SGID binaries can be exploited for privilege escalation.
  - **Kernel Module Exploitation:** Loading malicious kernel modules can grant complete system control.

**Malware & Rootkits:** Rootkits are designed to hide malware's presence and activity from detection by the OS. They often operate at a low level, making them difficult to remove.

**Supply Chain Attacks:** Compromising software or hardware during development or distribution can introduce vulnerabilities into the OS itself.


### Next Step
- [Windows](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Operating_Systems/windows.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resource / Study Sources
- [https://en.wikipedia.org/wiki/Operating_system](https://en.wikipedia.org/wiki/Operating_system)
- [NIST Special Publication 800-63B: Digital Identity Guidelines](https://csrc.nist.gov/publications/detail/sp/800-63b/final)
- **Operating System Concepts** (Silberschatz, Galvin, Gagne): A classic textbook covering OS fundamentals, including security aspects.
- **The Shellcoder's Handbook**: While dated, it provides valuable insights into exploitation techniques targeting operating systems. (Use with caution and ethical considerations).
- [OWASP (Open Web Application Security Project)](https://owasp.org/)

