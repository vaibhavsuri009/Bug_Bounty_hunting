# Direct Source Integration Risk

- What it is: Copying OSS source directly into an application can make upstream security fixes difficult to track and apply.
- Where to look / how to identify it:
  - Search code for vendored libraries, copied utility code, and embedded third-party modules.
- Exploitation / test pattern:
  - Compare embedded code against upstream versions and security advisories.
- Tools + exact CLI syntax (if mentioned):
  - Git diff/source comparison.
- Common false-positive / WAF / edge-case notes:
  - Small, stable helper code may be intentionally vendored and low risk.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Track provenance/version, automate upstream monitoring, and patch vendored code promptly.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
