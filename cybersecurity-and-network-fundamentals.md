

🌐 1. Networking Fundamentals

Networking is the foundation of cybersecurity. You must understand how computers talk to each other before you can protect them.


---

🔹 A. TCP/IP Model

TCP/IP (Transmission Control Protocol / Internet Protocol) defines how data travels across networks.

Layer	Purpose	Example Protocols

Application	What users interact with	HTTP, HTTPS, FTP, DNS, SMTP, SSH
Transport	Handles data delivery	TCP (reliable), UDP (faster, no check)
Internet	Routing across networks	IP, ICMP
Network Access	Physical delivery	Ethernet, Wi-Fi


TCP: reliable, connection-based (e.g., web browsing, email).
UDP: fast, connectionless (e.g., streaming, games).


---

🔹 B. OSI Model (7 Layers)

Think of this as a “map” of how data travels through a network.

#	Layer	Function	Example

7	Application	User-level programs	HTTP, FTP
6	Presentation	Data formatting, encryption	SSL, JPEG
5	Session	Connection management	Session tokens
4	Transport	Data delivery	TCP, UDP
3	Network	IP addressing, routing	IP, ICMP
2	Data Link	Frames, MAC addressing	Ethernet
1	Physical	Cables, signals	Wi-Fi, fiber


Tip: memorize with “All People Seem To Need Data Processing.”


---

🔹 C. Ports & Protocols

Ports are like doors on a computer used for network communication.

Port	Protocol	Description

20 / 21	FTP	File Transfer
22	SSH	Secure remote login
25	SMTP	Email sending
53	DNS	Domain name resolution
80	HTTP	Web traffic
443	HTTPS	Secure web traffic
3389	RDP	Remote Desktop Protocol


🔐 Security Tip: Always close unused ports — open ports = possible attack entry.


---

🔹 D. Subnetting, Routing, Firewalls, NAT

Subnetting: Dividing large networks into smaller ones using IP ranges.
Example:
192.168.1.0/24 → 256 IPs (usable: 192.168.1.1–192.168.1.254)

Routing: Directing network traffic between subnets or networks.

Static routes = manually configured

Dynamic = uses routing protocols (e.g., RIP, OSPF)


Firewall: Filters traffic by rules (e.g., block port 23 Telnet).

Types: hardware, software, and next-gen firewalls.

Common commands:

Windows: netsh advfirewall firewall show rule name=all

Linux: ufw, iptables



NAT (Network Address Translation):

Converts private IPs → public IPs (used by routers to share one internet connection).



---

🔹 E. Wireshark & Network Sniffing

Wireshark: A tool for capturing and analyzing network packets.

You can see:

Source/destination IP

Protocol used

Ports, payloads, and errors


Use cases:

Detect malware communication

Analyze suspicious traffic

Troubleshoot connection issues


Example filters:

http – show only web traffic

ip.addr == 192.168.1.10 – show packets from a specific host



⚠️ Ethical note: Only sniff traffic on networks you own or have permission to test.


---

🔹 F. Network Diagramming & Troubleshooting

Use tools like draw.io, Lucidchart, or Microsoft Visio to visualize:

Routers, switches, firewalls, clients, servers.


Troubleshooting commands:

Command	Purpose

ping <ip>	Test connectivity
traceroute <ip>	Shows path to destination
nslookup <domain>	Shows DNS resolution
ipconfig / ifconfig	Shows IP settings
netstat -an	Shows open ports/connections



---

🔐 2. Cybersecurity Concepts

Now we move from how networks work → how to protect them.


---

🔹 A. CIA Triad

The core of cybersecurity principles:

Principle	Meaning	Example

Confidentiality	Data privacy	Encryption, passwords
Integrity	Data accuracy	Checksums, hashing
Availability	System uptime	Redundancy, backups, firewalls


If any of these 3 are broken → you have a security incident.


---

🔹 B. AAA Model (Authentication, Authorization, Accounting)

1. Authentication: Verifying who you are (password, biometrics).


2. Authorization: What you’re allowed to do (permissions, access level).


3. Accounting: Tracking actions (logs, audits).



Example:

Login to network (AuthN)

Access certain files (AuthZ)

Log activity in SIEM (Acct)



---

🔹 C. Threats vs Vulnerabilities vs Risks

Term	Meaning	Example

Threat	Potential cause of harm	Hacker, malware
Vulnerability	Weakness that can be exploited	Unpatched software
Risk	Probability of a threat exploiting a vulnerability	High risk = outdated Windows server exposed online


💡 Formula:
Risk = Threat × Vulnerability × Impact


---

🔹 D. Security Policies & Frameworks

These define best practices for organizations.

Framework	Purpose

ISO 27001	International standard for Information Security Management Systems (ISMS)
NIST CSF (Cybersecurity Framework)	U.S. guideline for identifying, protecting, detecting, responding, and recovering from threats
CIS Controls	18 actionable steps for securing systems (used globally)


Examples of policies:

Password Policy (minimum length, complexity)

Access Control Policy

Incident Response Policy

Backup & Recovery Policy



---

🧠 Summary Table

Category	Learn	Tools / Examples

TCP/IP & OSI	Data communication layers	Wireshark, ping
Ports & Protocols	Identify common network services	nmap, netstat
Subnetting & Routing	IP management	ipcalc, route
Firewalls & NAT	Control access & translation	iptables, ufw
Wireshark	Packet capture	Filtering & analysis
CIA Triad	Core security goals	Encryption, backups
AAA	Access control	Authentication servers
Threats/Vulns/Risks	Security assessment	Penetration testing
Frameworks	Standards & policies	ISO 27001, NIST, CIS



---

