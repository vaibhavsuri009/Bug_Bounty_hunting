# Origin + Referer CSRF Check

- What it is: Origin and Referer checks can provide a first-line CSRF defense by ensuring state-changing requests originate from trusted application URLs.
- Where to look / how to identify it:
  - Validate both headers when expected and reject missing/untrusted origins on protected actions.
- Exploitation / test pattern:
  - Test with controlled legitimate and foreign origins.
- Tools + exact CLI syntax (if mentioned):
  - Server middleware.
- Common false-positive / WAF / edge-case notes:
  - An XSS on an allowlisted origin can defeat this layer.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use origin checks in addition to CSRF tokens and SameSite cookies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 29
