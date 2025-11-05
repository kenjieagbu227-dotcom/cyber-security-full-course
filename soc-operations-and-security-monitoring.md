🛡️ Lesson 12.1: Security Monitoring & SOC Operations

## Purpose
- Continuous monitoring to detect, triage, and respond to threats.

## SOC Roles
- Tier 1 (triage), Tier 2 (investigation), Tier 3 (threat hunting & IR).

## Key Activities
- Alert triage, playbook execution, escalation, reporting.

## Metrics
- Mean time to detect (MTTD), mean time to respond (MTTR).

SIEM Tools (Splunk, ELK, QRadar)

## Why SIEM
- Centralize logs, correlate events, generate alerts, enable search.

## Examples
- **Splunk:** search and dashboarding (SPL queries).
- **ELK (Elasticsearch, Logstash, Kibana):** open-source alternative.
- **QRadar:** enterprise correlation & offense management.

## Basic Splunk search example

index=wineventlog EventCode=4625 | stats count by Account_Name, ComputerName



 Threat Hunting & Intelligence

## Threat Hunting
- Proactive searching for threats using hypotheses and IOCs.

## Threat Intelligence
- Use open-source feeds (OSINT), commercial intel, and internal telemetry.

## Example hunt
- Look for unusual parent-child process relationships (e.g., cmd spawned from outlook.exe).


# ⚙️  Behavioral Analysis & EDR

## Behavioral Analytics
- Detect anomalies in process behavior, user activity, network flows.

## EDR Role
- Endpoint telemetry, automated response (isolate host), rollback.

## Tools
- CrowdStrike, SentinelOne, Carbon Black — configure detection rules and response actions.

