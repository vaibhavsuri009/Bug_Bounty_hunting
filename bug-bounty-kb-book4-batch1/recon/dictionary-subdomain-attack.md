# Dictionary-Based Subdomain Enumeration

- What it is: A dictionary attack uses likely subdomain names instead of exhausting every character combination.
- Where to look / how to identify it:
  - Build a wordlist from common infrastructure names plus target-specific terms discovered during recon.
- Exploitation / test pattern:
  - Resolve dictionary entries and add live in-scope results to the recon map.
- Tools + exact CLI syntax (if mentioned):
  - Use the same asynchronous DNS resolution method demonstrated for brute force.
- Common false-positive / WAF / edge-case notes:
  - Wildcard DNS can make every candidate appear valid; establish a random-name baseline first.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use DNS wildcarding carefully and protect discovered services with real authentication/authorization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
