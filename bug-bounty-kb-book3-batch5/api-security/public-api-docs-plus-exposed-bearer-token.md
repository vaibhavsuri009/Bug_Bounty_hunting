# Public API Docs + Exposed Bearer Token Chain

- What it is: Public administrative documentation becomes far more dangerous when an authorization token is also exposed.
- Where to look / how to identify it:
  - Use documentation to map admin functions, then verify whether the exposed token can perform only the permissions explicitly authorized for testing.
- Exploitation / test pattern:
  - Demonstrate the smallest safe privileged action needed to prove impact.
- Tools + exact CLI syntax (if mentioned):
  - Burp/Postman for controlled replay.
- Common false-positive / WAF / edge-case notes:
  - Documentation alone is usually informational; the exploitable chain is docs plus broken authentication/authorization.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Protect sensitive docs, rotate leaked tokens, and enforce BFLA on every administrative function.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
