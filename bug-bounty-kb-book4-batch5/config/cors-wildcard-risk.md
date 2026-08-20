# CORS Wildcard Scope Risk

- What it is: Broad CORS origin configuration can expose responses to untrusted web origins.
- Where to look / how to identify it:
  - Inspect `Access-Control-Allow-Origin` and how it changes when different Origin values are supplied.
- Exploitation / test pattern:
  - Use only controlled origins and non-sensitive test data to validate whether the policy is too broad.
- Tools + exact CLI syntax (if mentioned):
  - DevTools/Burp-like request editing.
- Common false-positive / WAF / edge-case notes:
  - `*` can be valid for genuinely public unauthenticated resources.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Allowlist only the exact trusted origins needed by the application.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
