# Subdomain Brute Force as Last Resort

- What it is: Subdomain brute forcing tests candidate labels to discover hosts not exposed through passive sources.
- Where to look / how to identify it:
  - Use it only after browser traffic, public records, archives, certificate/DNS sources, and other passive techniques are exhausted.
- Exploitation / test pattern:
  - Prefer a relevant dictionary before attempting exhaustive combinations.
- Tools + exact CLI syntax (if mentioned):
  - DNS resolution can be automated asynchronously; the book demonstrates Node.js `dns.resolve()`.
- Common false-positive / WAF / edge-case notes:
  - Brute force is noisy, rate-limited, easy to detect, and may trigger bans; use only with explicit permission.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Monitor and rate-limit enumeration activity and avoid relying on hidden hostnames as a security boundary.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
