# Linux

## Linux: Deep Dive For Cybersecurity Personnel

### Introduction
Linux is not an operating system per se, but rather the kernel – the core component – of numerous operating systems known as distributions (distros). Its open-source nature, robust security features when properly configured, and widespread adoption across servers, embedded devices, and cloud infrastructure make it a critical area of study for cybersecurity professionals. This document provides an in-depth look at Linux architecture, key components, common vulnerabilities, and relevant attack vectors.

### Core Architecture & Components
**Kernel Space vs. User Space:** Linux operates on a dual-space model. The kernel resides in protected memory (kernel space) managing hardware resources. User applications run in user space with limited access to system resources, enhancing stability and security through privilege separation.

**System Calls (Syscalls):** User programs request services from the kernel via syscalls – defined interfaces for interacting with hardware and other OS functions (e.g., read(), write(), open()). Exploiting vulnerabilities in syscall handlers is a common attack vector.

**Memory Management:** Linux employs virtual memory, paging, and swapping to manage RAM efficiently. Understanding these mechanisms is crucial for analyzing memory-related exploits (buffer overflows, heap corruption).

**Process Management:** The kernel manages processes – instances of running programs. Processes have IDs (PIDs), priorities, and resource limits. Process manipulation can be used in denial-of-service attacks or privilege escalation.

**File System:** Linux supports a wide range of file systems (ext4, XFS, Btrfs, etc.). File permissions are controlled by the owner, group, and others using read (r), write (w), and execute (x) bits. Improperly configured file permissions are a frequent vulnerability.

**Device Drivers:** These modules allow the kernel to interact with hardware devices. Vulnerabilities in device drivers can provide attackers with low-level access to the system.

### Key Security Features & Concepts
**User and Group Management:** Linux uses user accounts, groups, and permissions to control access to resources. The `root` account has unrestricted privileges; compromising this account is a critical security breach.

**Access Control Lists (ACLs):** Provide more granular permission control than traditional Unix permissions. ACLs allow specifying permissions for individual users or groups on specific files or directories.

**SELinux/AppArmor:** Mandatory Access Control (MAC) systems that enforce stricter access controls beyond the discretionary access control (DAC) of standard Linux permissions. SELinux and AppArmor define security policies that restrict what processes can do, even if they are running with elevated privileges. Bypassing these MACs is a significant challenge for attackers.

**Capabilities:** Fine-grained privilege management mechanism allowing specific capabilities to be granted to programs instead of granting full root access. This reduces the attack surface by limiting potential damage from compromised processes.

**Auditing (auditd):** A subsystem that records system calls and other security-relevant events, providing valuable information for intrusion detection and forensic analysis.

**Firewalling (iptables/nftables):** Linux firewalls control network traffic based on rules defined by the administrator. Misconfigured firewalls can expose services to unauthorized access.

### Common Vulnerabilites & Attack Vectors
**Kernel Exploits:** Vulnerabilities in the kernel itself are highly dangerous, as they often allow attackers to gain root privileges directly. Examples include:
  - **Race Conditions:** Occur when multiple processes or threads access shared resources concurrently, leading to unpredictable behavior and potential exploits.
  - **Null Pointer Dereferences:** Occur when a program attempts to access memory at address 0 (NULL), often resulting in crashes or exploitable conditions.
  - **Integer Overflows:** Occur when arithmetic operations result in values that exceed the maximum representable value, leading to unexpected behavior and potential buffer overflows.

**Shellshock (Bash Vulnerability):** A vulnerability in the Bash shell allowing arbitrary code execution through environment variables. (CVE-2014-6271)

**Log4j-like vulnerabilities:** While Log4j is a Java library, similar injection flaws can exist within Linux system utilities and configuration files that process user input without proper sanitization.

**Privilege Escalation:** Exploiting vulnerabilities to gain higher privileges than initially authorized (e.g., from a standard user to root). Common techniques include:
  - **SUID/SGID Binaries:** Executables with the SUID or SGID bit set run with the permissions of the owner or group, respectively. Misuse can lead to privilege escalation.
  - **Exploiting Weak File Permissions:** Gaining access to files or directories that should be restricted.

**Denial-of-Service (DoS):** Overwhelming system resources to make them unavailable to legitimate users. Can target network services, file systems, or the kernel itself.

**Malware & Rootkits:** Malicious software designed to compromise a Linux system and maintain persistent access. Rootkits often hide their presence from standard detection methods.

**Supply Chain Attacks:** Compromising software packages or dependencies used by Linux distributions can introduce vulnerabilities into systems that rely on them.

### Mitigation Strategies
| Strategy | Implmentations |
|---|---|
| Regular Patching | Keeping the kernel, libraries, and applications up-to-date is crucial to address known vulnerabilities. |
| Hardening | Implementing security best practices such as disabling unnecessary services, restricting user privileges, and configuring firewalls. |
| Intrusion Detection System (IDS) |  Monitoring system activity for suspicious behavior and automatically blocking malicious traffic. |
| Security Auditing | Regularly reviewing system configurations and logs to identify potential vulnerabilities. |
| Least Privilege Principle | Granting users and processes only the minimum necessary privileges to perform their tasks. |
| Secure Coding Practices | Developing software with security in mind, avoiding common pitfalls such as buffer overflows and SQL injection. |

### Next Steps
- [MacOS](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Operating_Systems/macos.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resources
- [Linux Kernel Documentation](https://www.kernel.org/doc/)
- [SELinux Project](https://selinux.org/)
- [AppArmor Wiki](https://apparmor.net/wiki/Main_Page)
- [Open Source Security Foundation (OSSF)](https://www.ossf.org/)
- [CVE Database](https://cve.mitre.org/)
