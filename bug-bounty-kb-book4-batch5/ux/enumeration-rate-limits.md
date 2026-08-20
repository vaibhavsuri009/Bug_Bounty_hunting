# Enumeration Rate Limits

- What it is: Rate limits reduce the ability to repeatedly query endpoints and accumulate small information leaks.
- Where to look / how to identify it:
  - Identify endpoints where repeated requests can enumerate users, objects, reset tokens, or search data.
- Exploitation / test pattern:
  - Measure legitimate usage and test only below non-disruptive limits.
- Tools + exact CLI syntax (if mentioned):
  - API gateway/application rate limiting.
- Common false-positive / WAF / edge-case notes:
  - Overly strict limits can block real users; IP-only limits may fail with distributed clients.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Rate-limit by user/token/device/IP and monitor anomalous enumeration patterns.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 23
