# PBKDF2 Password Storage

- What it is: PBKDF2 uses repeated derivation iterations to make password guessing computationally expensive.
- Where to look / how to identify it:
  - Review iteration count, salt handling, underlying hash, and whether parameters are current for the deployment.
- Exploitation / test pattern:
  - Benchmark and select the highest practical iteration count that preserves acceptable login latency.
- Tools + exact CLI syntax (if mentioned):
  - Standard crypto library implementation.
- Common false-positive / WAF / edge-case notes:
  - Too few iterations can make PBKDF2 weak despite correct algorithm choice.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use a current recommended iteration count with unique salts and periodic review.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
