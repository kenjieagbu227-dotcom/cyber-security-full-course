
🧩 1. Windows Fundamentals

Windows is the most common OS targeted by hackers, so you need to understand how it really works under the hood.

🔹 A. Registry

What it is: A database where Windows stores configuration settings for the OS and installed apps.

Learn:

Registry structure:

HKEY_LOCAL_MACHINE (HKLM) – system-wide settings

HKEY_CURRENT_USER (HKCU) – current user settings


How to open/edit it: regedit

Common paths to explore:

HKLM\Software\Microsoft\Windows\CurrentVersion\Run → startup programs

HKLM\SYSTEM\CurrentControlSet\Services → system services


Security: Malware often hides in the registry (e.g., startup persistence).



🔹 B. File Systems

What it is: How Windows stores and organizes files (mainly NTFS and FAT32).

Learn:

File structure: drives (C:\), folders, and system files.

File permissions (NTFS permissions: Full Control, Modify, Read, Write).

System files:

C:\Windows\System32 → core OS files

C:\Users\<username> → user data


Command prompt basics: dir, cd, del, copy, attrib



🔹 C. Services

What it is: Background programs that perform system tasks (e.g., Windows Update, Print Spooler).

Learn:

View with services.msc or sc query

Start/Stop services:

net start <service>
net stop <service>

Check startup type: automatic, manual, disabled.

Security: Attackers often disable security services or create fake ones.




---

🐧 2. Linux Fundamentals

Most servers and cybersecurity tools run on Linux — so this is critical.

🔹 A. Terminal Commands

Learn to navigate and manage Linux using the terminal (shell/Bash).

Purpose	Command Examples

Navigation	pwd, cd, ls, tree
File management	cp, mv, rm, mkdir, touch, cat, nano, less
System info	uname -a, top, ps aux, df -h, free -m
Network	ping, ifconfig / ip a, netstat, curl, wget, ssh
User management	whoami, adduser, passwd, su, sudo


🔹 B. Permissions

Linux uses Owner / Group / Others permission system.

Example:

-rwxr-xr--

means:

Owner can read/write/execute

Group can read/execute

Others can read only


Commands:

Change permissions: chmod

Change owner: chown

View permissions: ls -l



🔹 C. Networking

Check network interfaces: ifconfig or ip addr

Check open ports: netstat -tuln

Test connectivity: ping <ip>, traceroute <ip>

SSH remote login: ssh user@ip

Security: Know how to harden Linux (disable root SSH login, firewall with ufw or iptables)



---

🧱 3. Virtual Machines (VMWare / VirtualBox)

VMs let you safely test, hack, or experiment without damaging your real system.

🔹 A. What They Are

A virtual machine is like a “computer inside your computer.”

It uses virtualization to simulate hardware.


🔹 B. Why It’s Important

Used for testing malware, creating lab environments, or learning OSes.

You can run Windows and Linux side by side.


🔹 C. Learn:

How to install and configure VMs:

Create a new VM → choose ISO → allocate CPU/RAM → install OS.


Snapshots: Save VM state before experiments.

Networking modes:

NAT – uses host internet connection.

Bridged – connects directly to local network.

Host-only – isolated from internet, used for labs.


Shared folders – transfer files between host and VM.

Security tip: Always isolate VMs when testing malware or penetration tools.



---

🧠 Summary Cheat Sheet

Area	Learn	Why

Windows Registry	System settings, persistence locations	Detect malware + configuration control
Windows Services	Background system tasks	Identify disabled or fake services
Windows File System	NTFS, permissions, structure	Understand file storage & access control
Linux Terminal	Commands, navigation, file ops	Foundation of all server & cybersecurity tasks
Linux Permissions	chmod, chown, sudo	Secure file access
Linux Networking	ping, ssh, netstat	System communication & network security
Virtual Machines	Setup, snapshots, networking modes	Safe learning and testing



---

Would you like me 
