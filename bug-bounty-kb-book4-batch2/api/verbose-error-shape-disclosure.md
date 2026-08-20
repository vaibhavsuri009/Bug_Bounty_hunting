# Verbose Error Payload-Shape Disclosure

- What it is: API errors may reveal missing parameters, accepted enum values, or required authorization fields.
- Where to look / how to identify it:
  - Send malformed but harmless requests to controlled endpoints and inspect body/error details.
- Exploitation / test pattern:
  - Use each error to reduce the unknown request-shape search space rather than guessing blindly.
- Tools + exact CLI syntax (if mentioned):
  - Example signals: `auth_token not supplied`, allowed enum values, missing-field messages.
- Common false-positive / WAF / edge-case notes:
  - An error disclosure may be informational until it enables unauthorized behavior.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Return generic external errors while logging detailed diagnostics internally.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 5
