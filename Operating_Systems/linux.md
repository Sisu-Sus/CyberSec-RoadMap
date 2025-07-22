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

### Next Steps
- [MacOS](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Operating_Systems/macos.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resources
- [Linux Kernel Documentation](https://www.kernel.org/doc/)
- [SELinux Project](https://selinux.org/)
- [AppArmor Wiki](https://apparmor.net/wiki/Main_Page)
- [Open Source Security Foundation (OSSF)](https://www.ossf.org/)
- [CVE Database](https://cve.mitre.org/)
