# Data Transfer Object Defense

- What it is: A DTO constrains client data to a predefined shape before it reaches internal models or database update logic.
- Where to look / how to identify it:
  - Use DTOs on update/create endpoints that receive complex objects from clients.
- Exploitation / test pattern:
  - Construct a new object containing only permitted properties, then pass only that DTO to persistence code.
- Tools + exact CLI syntax (if mentioned):
  - Language/framework DTO/schema facilities.
- Common false-positive / WAF / edge-case notes:
  - DTOs can still be unsafe if privileged fields are included by mistake.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use separate read/write DTOs and exclude security-sensitive properties by default.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 33
