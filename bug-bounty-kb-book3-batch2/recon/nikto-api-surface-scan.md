# Nikto API Surface Scan

- What it is: Nikto quickly fingerprints web/API services and highlights misconfigurations and interesting paths.
- Basic syntax:
```bash
nikto -h https://example.com
```
- Use `-output <file>` to save findings.
- Use `-maxtime <seconds>` to bound scan duration.
- Review allowed methods, headers, server details, possible API endpoints, and directories.
- Manually validate every interesting result.
- False positive: automated scanner findings can be inaccurate or low impact.
- Edge case: authentication can hide most application functionality.
- Remediation: harden server configuration and minimize unnecessary metadata/endpoints.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
