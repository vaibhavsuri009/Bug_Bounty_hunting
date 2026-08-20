# CVSS Confidentiality/Integrity/Availability Impact

- What it is: CVSS impact metrics estimate what data, state, and service availability can be compromised.
- Where to look / how to identify it:
  - Identify what information can be read, what state can be changed, and whether legitimate use can be interrupted.
- Exploitation / test pattern:
  - Score None/Low/High based on validated impact and application context.
- Tools + exact CLI syntax (if mentioned):
  - CVSS calculator plus data-classification inventory.
- Common false-positive / WAF / edge-case notes:
  - An exploit may affect only one of the CIA dimensions significantly.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Tie impact statements to concrete assets and reproducible evidence.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
