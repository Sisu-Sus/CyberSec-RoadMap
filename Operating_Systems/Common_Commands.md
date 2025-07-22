# Essential Command-Line Operations 
## Introduction
The command-line interface (CLI), or shell, provides direct interaction with an operating system’s kernel and underlying processes. Proficiency in CLI commands is crucial for cybersecurity professionals involved in incident response, forensic analysis, penetration testing, system administration, and security auditing. This guide outlines fundamental commands common to Unix/Linux and Windows environments, emphasizing their functionality and potential misuse within a security context. While graphical user interfaces (GUIs) offer convenience, the CLI provides granular control and access often unavailable through GUI tools.

## I. Navigating the File System
The ability to efficiently navigate the file system is paramount for any system interaction.
- **Unix/Linux**
  - `ls`: Lists files and directories within a specified location. Options like `-l`(long listing format, displaying permissions, ownership, size, modification time), `-a`(show hidden files - those starting with `.`), and `-R`(recursive listing) are frequently used. Understanding file attributes is critical for security auditing.
 
  - `cd`: Changes the current working directory. `cd ..` moves up one level; `cd ~` returns to the user's home directory.
 
  - `pwd`: Prints the absolute path of the current working directory. Useful for confirming location and avoiding errors when scripting.
 
- **Windows**
  - `dir`: Equivalent to `ls`. Options like `/a` (attribute display), `/b `(bare format, no header or summary information), and `/s` (recursive listing) are common.
 
  - `cd`: Identical functionality to the Unix/Linux command.
 
  - `echo %cd%`: Displays the current directory path using environment variable expansion.
 
## II. File and Directory Mangement
These commands enable manipulation of files and directories, a frequent target for malicious actors.

- **Unix/Linux**
    - `cp [options] source destination`: Copies files or directories. `-r` (recursive) is essential for copying entire directory structures. Improper use can lead to denial-of-service if large files are copied without sufficient disk space.

    - `mv [options] source destination`: Moves (renames) files or directories. Careless renaming can disrupt system functionality and data integrity.

    - `rm [options] file(s)`: Removes files. Extremely dangerous! The `-f` (force) option bypasses prompts, making accidental deletion irreversible. The `-r` option is required for removing directories recursively. Malware often uses `rm -rf` / as a destructive payload.

    - `mkdir [options] directory_name`: Creates new directories. Permissions assigned during creation are important for access control.

- **Windows:**
    - `copy [options] source destination`: Equivalent to `cp`. `/y` suppresses prompts for overwrite confirmation.

    - `move [options] source destination`: Equivalent to `mv`.

    - `del [options] file(s)`: Deletes files. `/f` (force) and `/q` (quiet mode, no prompting) are common options. Similar caution applies as with `rm`.

    - `mkdir directory_name`: Creates new directories.

## III. System Information and Process Management
Monitoring system resources and processes is vital for detecting anomalies indicative of compromise.

- **Unix/Linux**
    - `top / htop`: Real-time process monitoring, displaying CPU usage, memory consumption, and other metrics. `htop` provides a more user-friendly interface. Attackers often attempt to hide their processes by manipulating these displays.

    - `ps [options]`: Lists running processes. Options like `-e` (show all processes), `-f` (full format), and `-u username` (filter by user) are frequently used. Process analysis is a key forensic technique.

    - `df -h`: Displays disk space usage in human-readable format. Useful for identifying potential denial-of-service attacks or unauthorized data storage.

    - `uname -a`: Prints system information, including kernel version and architecture. Important for vulnerability assessment.

- **Windows**
    - `tasklist`: Lists running processes with details like process ID (PID), memory usage, and status.

    - `taskkill /pid <PID> /f`: Terminates a process by its PID. The `/f` option forces termination. Requires administrative privileges. Can be used maliciously to disrupt services.

`systeminfo`: Provides detailed system information, including OS version, hardware configuration, and network settings. Valuable for identifying potential vulnerabilities based on outdated software or configurations.

## IV. File Permissions and Ownership

Properly configured file permissions are a cornerstone of security.
- **Unix/Linux**
  - `chmod [options] mode file(s)`: Changes file permissions using octal notation (e.g., `chmod 755 myfile.txt`). Understanding the read, write, and execute bits is essential. Incorrect permissions can lead to unauthorized access or privilege escalation.

`chown [user:group] file(s)`: Changes file ownership. Requires root privileges. Malware often attempts to change ownership of critical system files to gain persistence.

- **Windows**
    - `icacls [options] file(s)`: Modifies Access Control Lists (ACLs), which define permissions for users and groups. Complex but powerful.

    - `attrib [options] file(s)`: Changes file attributes, such as read-only or hidden. Attackers may use this to conceal malicious files.
 
## V. Network Commands
Network connectivity testing and monitoring are essential for security assessments.

- **Unix/Linux**
  - `ping <hostname/IP>`: Tests network reachability by sending ICMP echo requests. Can be used to verify connectivity or perform basic reconnaissance. ICMP blocking is a common defense mechanism.

  - `ifconfig` / `ip addr`: Configures and displays network interface information (IP address, subnet mask, gateway). The `ip` command is the modern replacement for `ifconfig`.

  - `netstat -an`: Displays active network connections and listening ports. Useful for identifying suspicious outbound connections or unauthorized services. Replaced by `ss` in newer systems.

- **Windows**
  - `ping <hostname/IP>`: Equivalent to the Unix/Linux command.

  - `ipconfig /all`: Displays network configuration information, including IP address, DNS servers, and MAC address.

  - `netstat -an`: Displays active network connections and listening ports (similar functionality to `netstat` on Linux).
 
Mastering these fundamental command-line operations is a prerequisite for effective cybersecurity practice. Understanding not only their intended use but also potential misuse scenarios is crucial for identifying and mitigating security risks. Regular practice and experimentation in a controlled environment are highly recommended.


### Next Step
- [Networking Knowledge](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/Networking_Knowledge/Networking_Knowledge.md)
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)

### Resources / Study Sources
- [https://linuxcommandline.org/](https://linuxcommandline.org/)
- [https://learn.microsoft.com/en-us/windows-commandline/](https://learn.microsoft.com/en-us/windows-commandline/)
