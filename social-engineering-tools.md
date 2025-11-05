Purpose:** simulate human-targeted attacks (phishing, pretexting).

**Sample Tools**
- **SET (Social-Engineer Toolkit)** — email phishing, credential harvesting.
- **Gophish** — phishing campaign framework.

**Ethics:** Social engineering requires strict authorization and clear rules of engagement.


---

Password Cracking Tools

**Purpose:** test password strength and recovery.

**Sample Tools**
- **John the Ripper** — password cracker for many hash types.
- **Hydra** — online brute force (services).
- **Hashcat** — GPU-accelerated cracking.

**Example hashcat usage (rockyou wordlist):**
```bash
hashcat -m 0 hash.txt /path/to/rockyou.txt

---

  Forensics Tools

**Purpose:** analyze compromised systems and recover artifacts.

**Sample Tools**
- **Autopsy** — GUI for disk forensics.
- **Volatility** — memory forensics framework.

**Example:** use Volatility to list processes in a memory dump.
```bash
volatility -f memdump.raw --profile=Win7SP1x64 pslist

---

 Network Sniffing Tools

**Purpose:** capture and analyze network traffic.

**Sample Tools**
- **Wireshark** — GUI packet analyzer.
- **tcpdump** — command-line packet capture.

**Example tcpdump capture:**
```bash
sudo tcpdump -i eth0 -w capture.pcap
# open capture.pcap in Wireshark for analysis

---
