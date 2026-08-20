# Isolate Risky Third-Party Components

- What it is: Running high-risk integrations separately reduces blast radius if a dependency is compromised.
- Where to look / how to identify it:
  - Prioritize parsers, converters, analytics, plugins, and third-party code requiring broad resources.
- Exploitation / test pattern:
  - Place the dependency in its own process/server/container and communicate through a constrained data interface.
- Tools + exact CLI syntax (if mentioned):
  - Service/container architecture.
- Common false-positive / WAF / edge-case notes:
  - Isolation adds latency and does not protect data intentionally sent to the isolated service.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use process/network boundaries and least privilege for high-risk dependencies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
