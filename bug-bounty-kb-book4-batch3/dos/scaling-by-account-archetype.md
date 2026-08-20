# Endpoint Scaling by Account Archetype

- What it is: An endpoint may become disproportionately expensive as user-controlled data volume grows.
- Where to look / how to identify it:
  - Compare the same request for new, average, and synthetic high-volume test accounts in a lab.
- Exploitation / test pattern:
  - Plot response time/resource usage against object count to identify nonlinear scaling.
- Tools + exact CLI syntax (if mentioned):
  - Timing table/script; local test environment preferred.
- Common false-positive / WAF / edge-case notes:
  - Never create extreme production data volumes solely to test DoS.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use bounded queries, pagination, indexes, quotas, and background jobs.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 14
