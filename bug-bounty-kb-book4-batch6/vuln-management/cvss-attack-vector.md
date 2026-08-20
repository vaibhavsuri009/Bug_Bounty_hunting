# CVSS Attack Vector

- What it is: Attack Vector measures how remotely or physically an attacker must interact with a system to exploit a vulnerability.
- Where to look / how to identify it:
  - Classify the exploit as Network, Adjacent, Local, or Physical based on delivery requirements.
- Exploitation / test pattern:
  - Use the most accurate reachable attack path demonstrated during reproduction.
- Tools + exact CLI syntax (if mentioned):
  - CVSS calculator.
- Common false-positive / WAF / edge-case notes:
  - Do not score a hypothetical remote path when only local access is actually proven.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Re-evaluate attack vector if architecture or exposure changes.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
