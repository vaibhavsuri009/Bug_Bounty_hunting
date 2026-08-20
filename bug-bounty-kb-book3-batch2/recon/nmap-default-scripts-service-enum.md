# Nmap Default Scripts + Service Enumeration

- What it is: Nmap `-sC -sV` identifies exposed services and runs default discovery scripts.
- Start with a basic scan to identify open ports.
```bash
nmap TARGET_IP
nmap -sC -sV TARGET_IP
```
- `-sC` runs default NSE scripts.
- `-sV` performs service/version detection.
- Inspect HTTP responses for titles, frameworks, server headers, and API clues.
- False positive: service fingerprints can be wrong on unusual/nonstandard ports.
- Edge case: deeper enumeration may trigger defensive monitoring.
- Remediation: expose only required services and patch/version-manage them.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 5
