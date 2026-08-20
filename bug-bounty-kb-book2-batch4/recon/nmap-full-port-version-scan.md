# Nmap Full-Port Version Scan

- What it is: A host is scanned across all TCP ports with service-version detection to find unexpected exposed services.
- The exact command shown in the book:
```bash
nmap -sV -p- TARGET_IP -oA stage__ph -T4
```
- `-sV`: detect service versions.
- `-p-`: scan all 65,535 TCP ports.
- `-oA stage__ph`: save normal, grepable, and XML outputs.
- `-T4`: faster timing profile than the default.
- Use only against explicitly in-scope hosts/IPs.
- False positive: Nmap service guesses can be wrong; manually validate unusual ports.
- Remediation: firewall non-public services and bind internal daemons to private interfaces.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
