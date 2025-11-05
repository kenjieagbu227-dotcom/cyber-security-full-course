
**Purpose:** collect and preserve digital evidence so it remains admissible and trustworthy.

## Key Concepts
- **Chain of custody:** record who collected, handled, transferred, and analyzed evidence (timestamps, signatures).
- **Forensic image:** bit-for-bit copy of storage (dd, FTK Imager).
- **Write-blocking:** prevent modification of original media during acquisition.

## Basic Steps
1. Document scene & system state (screenshots, network status).  
2. Use a hardware write-blocker or mount read-only.  
3. Acquire forensic image:
```bash
# Example using dd (careful with parameters)
dd if=/dev/sda of=/mnt/forensic/images/sda.dd bs=4M conv=sync,noerror

4. Hash images (SHA256) and record hashes in log.



Tools

FTK Imager, dc3dd, Guymager, EnCase (commercial)


Disk & Memory Forensics

## Disk Forensics
- Analyze filesystem artifacts (MFT, $LogFile, deleted files).
- Tools: Autopsy, sleuthkit, bulk_extractor.

## Memory Forensics
- Analyze running processes, loaded DLLs, credentials in memory.
- Capture physical memory (WinPMEM, fmem).
- Example Volatility command:
```bash
volatility -f memdump.raw --profile=Win10x64 pslist

Goals

Recover deleted files, timeline of activity, running malware traces.


 Log Analysis (Windows Event Logs, Sysmon, SIEM)

## What to look for
- Suspicious logins, privilege escalations, process creations, network connections.

## Tools & Tips
- **Windows Event Viewer** / exported EVTX files.
- **Sysmon** for detailed process/network/file events.
- Aggregate logs into **SIEM** (Splunk, ELK, QRadar) for correlation and alerting.

## Example: search for PowerShell suspicious activity
- In Splunk: `index=wineventlog EventCode=4104 OR EventID=4103 "Invoke-Expression"`

11.4 Malware Analysis (Sandboxing, Static & Dynamic Analysis)

 Malware Analysis

## Static Analysis
- Inspect binary without running (strings, binwalk, IDA/JADX for mobile).
- Check hashes, PE headers, imports.

## Dynamic Analysis
- Run in isolated VM or sandbox (Cuckoo, Any.Run).
- Monitor network, file, and process behavior.

## Tools
- strings, hexdump, radare2, Ghidra, IDA, Cuckoo, Procmon, Wireshark.

## Safety
- Use air-gapped VMs, snapshots, and no production connectivity.

11.5 Incident Response Lifecycle (Prepare, Detect, Contain, Recover, Lessons Learned)

 Incident Response Lifecycle

## Phases
1. **Prepare:** policies, playbooks, backups, IR team.  
2. **Detect & Analyze:** alerts, triage, scope.  
3. **Contain:** short-term (isolate host) & long-term (patch, reconfigure).  
4. **Eradicate & Recover:** remove artifacts, restore from backups, validate systems.  
5. **Lessons Learned:** post-incident report, improve controls.

## Deliverables
- Incident report, IOC list, remediation checklist, updated playbooks.
