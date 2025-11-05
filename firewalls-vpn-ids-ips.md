 Firewall: filters traffic based on rules (e.g., block ports, IPs).

VPN: encrypts internet traffic between your device and network.

IDS (Intrusion Detection System): monitors network for attacks.

IPS (Intrusion Prevention System): detects and blocks malicious traffic in real time.


Example:

Firewall blocks port 23 (Telnet).

VPN hides your IP.

IDS detects port scanning activity.


Command Example:

sudo ufw enable
sudo ufw allow 22/tcp
sudo ufw deny 23/tcp


---

🔹 7.2 Secure Network Architecture (DMZ, VLAN, Segmentation)


Explanation:
Secure architecture prevents attackers from reaching internal systems.

Key Components:

DMZ (Demilitarized Zone): public-facing zone (web servers).

VLAN: separates networks logically.

Network Segmentation: isolates systems to contain breaches.


Example:

Public web servers → DMZ

Database servers → internal VLAN

Admin systems → management VLAN


Visual Concept:

[Internet] → [Firewall] → [DMZ] → [Internal Network]


---

🔹 7.3 Proxy Servers & Content Filtering


Explanation:

Proxy server: acts as a middleman between users and the internet.

Content filtering: blocks malicious or inappropriate sites.


Example:
Companies use proxy servers to:

Cache content for speed.

Monitor user web traffic.

Block social media or malware sites.


Linux Example:
Use Squid Proxy:

sudo apt install squid -y
sudo nano /etc/squid/squid.conf

