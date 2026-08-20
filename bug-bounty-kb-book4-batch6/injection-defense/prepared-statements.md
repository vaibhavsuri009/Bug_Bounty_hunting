# Prepared Statements as Primary SQLi Defense

- What it is: Prepared statements compile SQL structure before user-controlled values are bound, preventing input from changing query intent.
- Where to look / how to identify it:
  - Review every query containing external input for bind variables/placeholders.
- Exploitation / test pattern:
  - Replace string concatenation with parameterized query APIs.
- Tools + exact CLI syntax (if mentioned):
  - MySQL example uses PREPARE/SET/EXECUTE with `?` placeholders.
- Common false-positive / WAF / edge-case notes:
  - Some dynamic identifiers or query fragments cannot be parameterized directly and require allowlisting.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use prepared statements for values and strict allowlists for non-parameterizable identifiers.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 31
