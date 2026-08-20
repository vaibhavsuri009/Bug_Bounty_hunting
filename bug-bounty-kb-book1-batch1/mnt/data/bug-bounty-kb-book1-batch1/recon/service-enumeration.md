# Service Enumeration

- What it is: Identify network services exposed by discovered hosts, usually by scanning ports or querying third-party datasets.
- Active baseline scan:
```bash
nmap target.example.com
```
- Review open/filtered ports and mapped service names.
- Active alternatives mentioned: Nmap and Masscan.
- Passive sources mentioned: Shodan, Censys, Project Sonar.
- Use passive results when direct scanning is restricted or you want lower-noise recon.
- Correlate hostnames, IPs, certificates, ports, and software versions across sources.
- Prioritize unexpected/admin/debug services for later validation.
- Scope warning: active port scanning can generate substantial traffic; verify program authorization first.
- False-positive trap: third-party scan data can be stale and services may have changed.
- Remediation: expose only required services and restrict management interfaces appropriately.

## Source: Bug Bounty Bootcamp, Ch. 5
