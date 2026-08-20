# Internal API Enumeration from Response Differences

- What it is: Subtle status-code differences can reveal that a proxy reached a real internal route.
- Where to look / how to identify it:
  - Build a baseline of nonexistent paths and compare candidate paths by code, body, length, and timing.
- Exploitation / test pattern:
  - Investigate only anomalous responses and keep enumeration constrained to the authorized environment.
- Tools + exact CLI syntax (if mentioned):
  - Burp Intruder + Comparer.
- Common false-positive / WAF / edge-case notes:
  - Do not infer a vulnerability from one status code; confirm the route with a harmless request.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Standardize proxy errors and avoid leaking internal routing distinctions.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
