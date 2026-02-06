# PowerShell Incident Investigation (EDR Workflow)

PowerShell alerts are common in enterprise environments. This document
outlines my approach to investigating suspicious PowerShell activity
using EDR tools such as CrowdStrike Falcon or Microsoft Defender.

---

## Alert Validation
- Review alert severity and detection type
- Identify affected host, user, and timestamp
- Confirm detection source and confidence level

---

## Process Tree Analysis
- Analyze parent and child processes
- Identify suspicious parent processes (Office, browser, scripts)
- Review command-line arguments for encoded or obfuscated commands

---

## Behavioral Indicators
- Execution policy bypass
- Base64-encoded commands
- Download or execution of remote payloads
- Abnormal child process creation

---

## Endpoint Scope & Persistence
- Check if similar activity exists on other endpoints
- Look for persistence mechanisms (scheduled tasks, registry entries)
- Validate user context and privilege level

---

## Containment Actions
- Isolate affected host if malicious behavior is confirmed
- Terminate malicious processes
- Block hashes or command patterns where applicable

---

## IOC Documentation
- File hashes
- Suspicious command lines
- Associated IPs and domains
- User accounts involved

---

## Mapping & Reporting
- Map observed behavior to MITRE ATT&CK techniques
- Document investigation steps and findings
- Escalate confirmed incidents as per SOC playbooks
