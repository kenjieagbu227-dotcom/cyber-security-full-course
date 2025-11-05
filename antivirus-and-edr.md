Antivirus detects and removes known malware using signature-based detection.

EDR (Endpoint Detection & Response) provides real-time monitoring, detects suspicious behavior, and allows remote incident response.


Example:

Antivirus → finds known virus like “Trojan.Win32.Agent.”

EDR → notices unusual process behavior even if it’s new malware.


Tip:
Use both together: antivirus for prevention, EDR for detection and response.


---

🔹 6.2 System Hardening (Windows & Linux)



Explanation:
System hardening = removing weaknesses in your OS.
Goal: reduce attack surface.

Windows Hardening:

Disable unnecessary services.

Turn on Windows Defender & Firewall.

Use Group Policy for user restrictions.


Linux Hardening:

Disable root login via SSH.

Keep /etc/ssh/sshd_config secure.

Use strong file permissions (chmod, chown).


Command Example:

# Disable root SSH login
sudo nano /etc/ssh/sshd_config
PermitRootLogin no
sudo systemctl restart sshd


---

🔹 6.3 Patch Management



Explanation:
Patch management = regularly updating software to fix vulnerabilities.

Why Important:
Hackers exploit unpatched systems — e.g., WannaCry ransomware spread via an unpatched Windows SMB flaw.

Best Practices:

Schedule automatic updates.

Test patches before deployment.

Maintain patch logs.


Example:

# Linux update command
sudo apt update && sudo apt upgrade -y


---

🔹 6.4 Secure Configuration Baselines


Explanation:
Baseline = standard secure settings applied across all systems.

Example:
Organizations follow CIS Benchmarks or NIST standards.

Benefits:

Consistency across all systems.

Easier auditing and compliance.


Sample Windows Policy:

Enforce password length ≥ 12.

Disable USB autorun.

Require screen lock after 10 minutes.


