Advanced Penetration Testing

## Focus
- Emulate real attackers: long-term stealth campaigns, persistence, data exfiltration.

## Techniques
- Custom tooling, living-off-the-land binaries, staging pivots, OPSEC.

## Deliverable
- Full adversary emulation report with risk-based recommendations.

13.2 Privilege Escalation Techniques

File name: lesson13-2-privilege-escalation.md

# 🔓 Lesson 13.2: Privilege Escalation Techniques

## Windows
- Misconfigured services, weak service permissions, unquoted service paths, token manipulation.

## Linux
- SUID binaries, sudo misconfigs, kernel exploits, weak file permissions.

## Tools
- Windows: PowerUp, Sherlock
- Linux: LinEnum, GTFOBins

Lateral Movement Simulation

## Techniques
- Credential harvesting, pass-the-hash, pass-the-ticket, remote service abuse.

## Tools
- **Mimikatz** — extract credentials on Windows (dangerous; authorized use only).
- **BloodHound** — map AD relationships and attack paths.

## Note
- Always have permission; these tools are highly sensitive.

OPSEC, Reporting & Debriefing

## OPSEC
- Avoid detection: randomized timing, living-off-the-land, encrypted C2 channels.

## Reporting
- Include executive summary, technical findings, PoC, remediation, risk rating.

## Debrief
- Walk stakeholders through findings, answer questions, plan remediation timeline.
