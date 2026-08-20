# API Active Recon Checklist

- What it is: Active API recon focuses on ports/services, intended application use, DevTools, API directories, and endpoint discovery.
- Where to look / how to identify it:
  - Start from authorized hosts, enumerate services, browse normally, inspect client traffic, then map API-specific routes.
- Exploitation / test pattern:
  - Preserve an evidence trail of endpoint, method, auth requirement, and response behavior.
- Tools + exact CLI syntax (if mentioned):
  - Common tools in the book: Nmap, DevTools, Burp, ZAP, Gobuster, Kiterunner.
- Common false-positive / WAF / edge-case notes:
  - Avoid high-rate scans unless the engagement explicitly permits them.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain an accurate API inventory and retire or restrict obsolete services.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. A
