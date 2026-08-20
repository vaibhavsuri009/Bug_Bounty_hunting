# Framebuster Fallback

- What it is: JavaScript framebusting can hide/unload a page when it detects that it is framed.
- Where to look / how to identify it:
  - Use only for legacy compatibility where CSP framing controls cannot be relied upon.
- Exploitation / test pattern:
  - Hide content by default and reveal it only when `self === top`.
- Tools + exact CLI syntax (if mentioned):
  - Browser JavaScript/CSS.
- Common false-positive / WAF / edge-case notes:
  - Framebusters can be bypassed and are weaker than CSP.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer CSP; treat framebusting only as defense-in-depth/legacy fallback.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
