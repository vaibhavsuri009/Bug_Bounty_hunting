# Bearer Token as REST Stateless Signal

- What it is: A token sent on every request is a strong signal that a REST API is using stateless authentication/authorization.
- Where to look / how to identify it:
  - Inspect request headers for `Authorization: Bearer ...` or equivalent credentials repeated across API calls.
- Exploitation / test pattern:
  - Record which resources and methods require the same token and which behave differently without it.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network request headers.
- Common false-positive / WAF / edge-case notes:
  - Some non-REST APIs also use bearer tokens, so do not classify solely from this header.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use short-lived scoped tokens and validate authorization per request.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 5
