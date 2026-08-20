# Iframe Sandbox Attribute

- What it is: The iframe sandbox attribute adds restrictions including script blocking, form blocking, origin isolation, and navigation restrictions.
- Where to look / how to identify it:
  - Inspect third-party/user-controlled iframe embeds for `sandbox` and enabled exceptions.
- Exploitation / test pattern:
  - Use a benign test embed to confirm dangerous capabilities remain disabled.
- Tools + exact CLI syntax (if mentioned):
  - `<iframe src='https://third-party.example' sandbox></iframe>`
- Common false-positive / WAF / edge-case notes:
  - Adding `allow-*` tokens can selectively restore dangerous capabilities.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Sandbox untrusted frames and grant only the minimum required capabilities.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
