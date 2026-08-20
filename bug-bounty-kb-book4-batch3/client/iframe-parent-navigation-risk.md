# Iframe Parent Navigation Risk

- What it is: A framed untrusted page may be able to navigate its parent when sandbox/CSP restrictions are missing.
- Where to look / how to identify it:
  - Identify application features that embed third-party or user-controlled URLs in iframes.
- Exploitation / test pattern:
  - Use a harmless test page to determine whether `window.parent` navigation is permitted.
- Tools + exact CLI syntax (if mentioned):
  - Browser/DevTools in a controlled environment.
- Common false-positive / WAF / edge-case notes:
  - Cross-origin policies restrict data reads but may still allow some navigation behavior depending on context.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use iframe sandboxing and restrictive CSP/frame policies for untrusted content.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 16
