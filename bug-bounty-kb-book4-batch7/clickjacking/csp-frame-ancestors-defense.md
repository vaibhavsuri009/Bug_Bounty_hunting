# Clickjacking Defense with `frame-ancestors`

- What it is: CSP `frame-ancestors` prevents unauthorized origins from framing sensitive application pages.
- Where to look / how to identify it:
  - Review sensitive UI pages for an effective CSP framing policy.
- Exploitation / test pattern:
  - Use `'none'`, `'self'`, or a narrow allowlist matching real embedding requirements.
- Tools + exact CLI syntax (if mentioned):
  - `Content-Security-Policy: frame-ancestors 'none'`
- Common false-positive / WAF / edge-case notes:
  - Legitimate embedded widgets may require controlled exceptions.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use CSP frame-ancestors as the primary framing defense.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
