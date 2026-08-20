# Asynchronous DNS Resolution Enumeration

- What it is: Asynchronous DNS resolution can greatly reduce the time needed to test a controlled subdomain candidate list.
- Where to look / how to identify it:
  - Populate a candidate list, resolve each label concurrently, and record only names that return an IP.
- Exploitation / test pattern:
  - The book favors Node.js `dns.resolve()` with Promises over `dns.lookup()` for this pattern.
- Tools + exact CLI syntax (if mentioned):
  - Core pattern: `dns.resolve(`${subdomain}.target.tld`, callback)` inside Promises.
- Common false-positive / WAF / edge-case notes:
  - High concurrency can overload DNS or trigger detection; throttle to the authorized engagement limits.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Rate-limit DNS queries and monitor abnormal enumeration patterns.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
