# Temporary Monitoring During Remediation

- What it is: Known vulnerabilities may be exploited while engineering teams are still developing a fix.
- Where to look / how to identify it:
  - After triage, identify observable exploit indicators and add temporary targeted logging/alerting.
- Exploitation / test pattern:
  - Monitor until the remediation is verified and regression coverage exists.
- Tools + exact CLI syntax (if mentioned):
  - Application/SIEM logging.
- Common false-positive / WAF / edge-case notes:
  - Logging does not mitigate the vulnerability itself and should not delay the fix.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Add compensating controls, monitoring, and clear escalation paths while patching.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 20
