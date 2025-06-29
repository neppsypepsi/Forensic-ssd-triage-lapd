# LAPD Task  – SSD Forensic Triage (Redacted)

> ⚠️ This is a redacted case study based on a real incident. All identifying details have been removed. This write-up is for educational and professional development purposes only.

---

## Objective

To investigate a Windows-based SSD obtained from a department machine suspected of unauthorized software installation or suspicious behavior. The goal is to:
- Preserve the original evidence
- Extract key forensic artifacts
- Build a timeline of relevant activity
- Apply the NIST 800-61 incident response model to the process

## Case Background

This case involves a suspected security incident tied to a high-ranking LAPD officer. A Windows-based workstation SSD was handed over to the cybersecurity team after reports surfaced that the officer may have been accessing unauthorized websites or clicking on suspicious links during work hours.

The device was removed from service and submitted for forensic analysis. At the time of this report:
- The exact websites visited are unknown.
- The nature of the links clicked or files downloaded is unclear.
- No formal disclosure was made by the officer in question.
- Direct questioning was discouraged, as the incident may result in disciplinary action or liability towards the officr.

---

## Nigel's Environment Setup

| Element        | Value |
|----------------|-------|
| Host Machine   | Intel MacBook Pro (2019) |
| Forensic OS    | Kali Linux (running in VM) |
| Adapter Used   | USB-C to SATA |
| Access Mode    | Read-only (`mount -o ro`) |
| SSD Type       | [REDACTED] |

---

## Artifact Targets to examine

- [ ] Event logs (`.evtx` files)
- [ ] Prefetch files
- [ ] Browser history database (Chrome SQLite)
- [ ] Downloads folder
- [ ] Program Files folders
- [ ] File metadata (timestamps, last accessed)

---

## Tools To Be Used

| Tool            | Purpose |
|------------------|---------|
| `evtx_dump.py`   | Parse Windows Event Logs |
| `WinPrefetchView`| Analyze Prefetch files |
| `sqlitebrowser`  | View browser history database |
| `stat`/`ls`      | View file metadata and timestamps |
| Bash scripting   | Automate evidence extraction |

---

## Next Step: Build Timeline

Will begin mapping out a timeline using:
- **Event ID 11707** – Software installed
- **Event ID 4624** – Logon events
- **Event ID 4688** – Process execution
- **Chrome visit timestamps** – User browsing activity

Timeline analysis will follow NIST SP 800-61 response phases:
1. Preparation  
2. Detection & Analysis  
3. Containment, Eradication, Recovery  
4. Post-Incident Activity

---

## 📌 Notes
All actions taken will be documented in `notes/` as a log. No actions will alter the original evidence source.
