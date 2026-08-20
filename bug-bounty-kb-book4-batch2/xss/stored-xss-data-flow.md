# Stored XSS Data Flow

- What it is: Stored XSS persists attacker-controlled content server-side and later executes when another user's client renders it.
- Where to look / how to identify it:
  - Trace user input from submission → database storage → retrieval → client DOM insertion.
- Exploitation / test pattern:
  - Use two controlled accounts to verify whether one account's stored input is rendered by another.
- Tools + exact CLI syntax (if mentioned):
  - Browser + DevTools; database/source review if available.
- Common false-positive / WAF / edge-case notes:
  - Stored markup without script-capable execution may be HTML injection rather than XSS.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Sanitize at output, use safe sinks, and consider scanning stored user content as an additional layer.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
