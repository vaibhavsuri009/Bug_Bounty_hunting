# Third-Party Dependency Inventory

- What it is: Modern web applications depend heavily on external client/server frameworks, libraries, and services that become part of the attack surface.
- Where to look / how to identify it:
  - Inventory SPA frameworks, JS libraries, CSS libraries, server frameworks, databases, and external services.
- Exploitation / test pattern:
  - Record both the dependency and the way it is integrated into the first-party application.
- Tools + exact CLI syntax (if mentioned):
  - Browser source/network inspection plus public package documentation.
- Common false-positive / WAF / edge-case notes:
  - A dependency being present is not a vulnerability; version and integration context matter.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain a software bill of materials and regularly patch/review third-party dependencies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
