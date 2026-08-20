# BFF Proxy Path Traversal Signal

- What it is: A backend-for-frontend proxy can accidentally forward path traversal sequences to internal services.
- Where to look / how to identify it:
  - Establish a normal proxy request, then test benign traversal variants and compare status/error changes.
- Exploitation / test pattern:
  - Treat a unique error among uniform 404 responses as a signal to investigate the path-handling logic further.
- Tools + exact CLI syntax (if mentioned):
  - Burp Intruder/Comparer can highlight response-code and body differences.
- Common false-positive / WAF / edge-case notes:
  - A different error is only a clue; it does not prove internal access.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Normalize paths before routing, reject traversal sequences, and allowlist internal destinations.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
