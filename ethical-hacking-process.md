This lesson explains the standard phases used in penetration testing and ethical hacking: Reconnaissance → Scanning → Exploitation → Post-Exploitation → Reporting.

---

Phases

### 1. Reconnaissance (Information Gathering)
- **Goal:** collect information about the target (domains, IPs, open ports, technologies).  
- **Passive methods:** WhoIs, public websites, Shodan, Google dorking.  
- **Active methods:** ping, nmap service discovery (be careful — active may be intrusive).

**Example commands:**
```bash
# Passive: whois
whois example.com

# Active: simple nmap scan
nmap -sV -T4 example.com


---

2. Scanning & Enumeration

Goal: identify live hosts, open ports, and services; enumerate users, shares, and software versions.

Tools: Nmap, Nikto, theHarvester, enum4linux.


Example:

nmap -sC -sV -oN scan_results.txt 192.168.1.0/24


---

3. Exploitation

Goal: use identified vulnerabilities to gain access.

Tools: Metasploit, SQLmap, custom exploits.

Ethics: Only exploit targets when you have explicit authorization.



---

4. Post-Exploitation

Goal: maintain access, escalate privileges, gather sensitive data, map the internal network.

Activities: privilege escalation, password dumps, lateral movement.



---

5. Reporting

Goal: document findings, proof-of-concept, risk rating, remediation steps.

Deliverable: clear, actionable penetration test report for stakeholders.



---

⚖️ Legal & Ethical Boundaries

Never test systems you do not own or have explicit permission to test.

Use written authorization (scope, duration, allowed tests).

Follow responsible disclosure for discovered vulnerabilities.



---

Next → Tools & Practical Labs

---

## 🧰 9. TOOLS TO LEARN — breakdown per category

### 🔹 9.1 Reconnaissance Tools  

Reconnaissance Tools

**Purpose:** discover targets and gather public information.

**Sample Tools**
- **Nmap** — host discovery & port scanning.
- **Shodan** — search internet-facing devices.
- **theHarvester** — emails, subdomains, public data.
- **Recon-ng** — modular reconnaissance framework.

**Example nmap usage:**
```bash
nmap -Pn -sS -p1-65535 --open -T4 target.com

Tip: Start passive (avoid detection) then move to active with permission.

---

### 🔹 9.2 Scanning / Vulnerability Assessment Tools  

*Purpose:** find known vulnerabilities and misconfigurations.

**Sample Tools**
- **Nessus** — commercial vulnerability scanner.
- **OpenVAS** (Greenbone) — open-source vulnerability scanner.
- **Nikto** — web server scanner for common issues.

**Quick example:**
- Run Nikto against a web server:
```bash
nikto -h https://target.com

---

### 🔹  Exploitation Tools  

**Purpose:** exploit vulnerabilities to gain access (use only with authorization).

**Sample Tools**
- **Metasploit Framework** — exploit development & execution.
- **Burp Suite** — web app testing & proxy (has active scanning in Pro).
- **SQLmap** — automated SQL injection exploitation.

**Example Metasploit start:**
```bash
msfconsole
search type:exploit name:ms08_067
use exploit/windows/smb/ms08_067_netapi
set RHOST 10.0.0.5
run

---
 Wireless Tools  

**Purpose:** assess Wi-Fi networks and wireless vulnerabilities.

**Sample Tools**
- **Aircrack-ng** — capture and crack WEP/WPA handshakes.
- **Kismet** — wireless network detector/sniffer.

**Basic aircrack flow overview:** capture handshake with airodump-ng → deauth to force reconnection → use aircrack-ng to crack handshake with wordlist.
