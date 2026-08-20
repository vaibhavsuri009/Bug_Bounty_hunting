# Resource-Intensive Endpoint Mapping

- What it is: Logical DoS vulnerabilities often exist in endpoints that trigger expensive CPU, memory, disk, database, or synchronous work.
- Where to look / how to identify it:
  - Prioritize database writes, joins, file writes, backups, conversions, and loops.
- Exploitation / test pattern:
  - Measure ordinary response time across controlled account sizes without intentionally overwhelming the service.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Timing or server-side lab metrics.
- Common false-positive / WAF / edge-case notes:
  - Slow requests may be expected for large operations and are not automatically vulnerabilities.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply quotas, asynchronous processing, caching, timeouts, and per-request resource limits.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 14
