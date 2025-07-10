# 🧰 Tools Used – LAPD Malware Forensics Case

This folder documents the tools I actively used during analysis of the compromised HP Windows system.

---

## 🕵️‍♂️ Endpoint Detection & Malware Removal

- **SentinelOne** – Pre-installed EDR agent that generated threat detection logs.
- **Malwarebytes** – Used for scanning and cleaning malware infections.

## 🛠️ Forensic Analysis

- **Windows Event Viewer** – Inspected System and Application logs related to BSODs and suspicious activity.
- **Registry Editor** – Manually examined keys for signs of malware persistence and startup behavior.

## 🔎 Threat Analysis

- **VirusTotal** – Used to analyze file hashes and scan suspicious executables.

## 💻 Analysis Environment

- **macOS + Windows Dual Boot** – Main setup used for log analysis and data access.
- **Kali Linux VM** – Used for isolated analysis, command-line tooling, and general red team utilities.

---

📌 Screenshots, logs, and related outputs are stored in the `/evidence/` folder and referenced in `lapd_ssd_case.md`.
