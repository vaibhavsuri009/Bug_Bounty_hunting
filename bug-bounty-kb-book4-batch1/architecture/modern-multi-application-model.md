# Modern Multi-Application Architecture Model

- What it is: Modern web applications are often multiple client/server applications communicating through APIs rather than a single monolith.
- Where to look / how to identify it:
  - Map separate UI, authentication, data, media, API, logging, and third-party servers whenever they appear.
- Exploitation / test pattern:
  - Treat each communicating application as a separate security boundary and document trust relationships.
- Tools + exact CLI syntax (if mentioned):
  - Browser Network tab and API request tracing.
- Common false-positive / WAF / edge-case notes:
  - Different hostnames do not automatically mean different owners; verify scope before interacting.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Document trust boundaries and authenticate/authorize every service-to-service interaction.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
