# PII and Financial Data Minimization

- What it is: Sensitive personal and financial data increases regulatory and breach impact and should be minimized or delegated when practical.
- Where to look / how to identify it:
  - Inventory what PII/financial data is stored, where, why, for how long, and who can access it.
- Exploitation / test pattern:
  - Remove unnecessary data and consider compliant specialist providers for high-risk storage.
- Tools + exact CLI syntax (if mentioned):
  - Data inventory/classification.
- Common false-positive / WAF / edge-case notes:
  - Outsourcing storage does not outsource all security or compliance responsibility.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Minimize collection, encrypt sensitive data, restrict access, and enforce retention policies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
