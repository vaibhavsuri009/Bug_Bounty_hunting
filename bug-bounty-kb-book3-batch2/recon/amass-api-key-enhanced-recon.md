# Amass API-Key-Enhanced Recon

- What it is: Adding data-source API keys expands Amass passive reconnaissance coverage.
- Install Amass:
```bash
sudo apt-get install amass
```
- Store the configuration under `$HOME/.config/amass/config.ini`.
- Add API keys for supported sources such as GitHub, Twitter, Censys, URLScan, or VirusTotal.
- Use the target domain as the seed for associated-domain/subdomain discovery.
- Compare results from multiple data sources to reduce misses.
- False positive: passive sources can contain historical or unrelated domains.
- Edge case: some sources require paid API access while others work without keys.
- Remediation note: continuously inventory externally visible domains and subdomains.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
