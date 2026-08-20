# Referrer/Origin Validation Bypass Signal

- What it is: CSRF defenses that validate only `Referer` or `Origin` may mishandle absent or null values.
- Where to look / how to identify it:
  - Compare legitimate requests with requests where referrer information is omitted in a controlled test.
- Exploitation / test pattern:
  - Confirm whether the server incorrectly accepts missing origin metadata rather than requiring positive validation.
- Tools + exact CLI syntax (if mentioned):
  - Browser `rel='noreferrer'` can suppress referrer data in some navigation cases.
- Common false-positive / WAF / edge-case notes:
  - Modern browsers and request types differ in header behavior; test consistently.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use CSRF tokens and SameSite cookies; treat origin headers as an additional layer only.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
