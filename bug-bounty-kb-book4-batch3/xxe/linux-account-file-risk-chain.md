# XXE Linux Account-File Risk Chain

- What it is: XXE file-read access to Linux account files can escalate from basic host information to credential compromise.
- Where to look / how to identify it:
  - Assess whether the parser can access files such as account metadata or restricted authentication stores without retrieving real secrets in production.
- Exploitation / test pattern:
  - Demonstrate impact with a non-sensitive file and explain the theoretical escalation instead of extracting passwords.
- Tools + exact CLI syntax (if mentioned):
  - No destructive tooling required.
- Common false-positive / WAF / edge-case notes:
  - Access depends on the parser process permissions; least privilege can significantly limit impact.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Run parsers as low-privilege users and disable external entities/file URI access.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 12
