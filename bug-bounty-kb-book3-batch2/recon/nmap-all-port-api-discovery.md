# Nmap All-Port API Discovery

- What it is: APIs and supporting services often run on uncommon ports missed by default scans.
- First fingerprint common services:
```bash
nmap -sC -sV TARGET_IP -oA api_scan
```
- Then scan all TCP ports:
```bash
nmap -p- TARGET_IP
```
- Investigate every HTTP-speaking port in a browser/Burp.
- Treat `Content-Type: application/json`, token errors, and API-like server responses as clues.
- Note exposed databases, mail interfaces, and other supporting services for later authorized testing.
- False positive: uncommon ports can host unrelated management or third-party services.
- Edge case: confirm scope before interacting with non-web services.
- Remediation: firewall unnecessary services and restrict databases/admin interfaces.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
