# Clickjacking Framing Signal

- What it is: Clickjacking overlays or hides a framed target UI so user clicks land on unintended controls.
- Where to look / how to identify it:
  - Check whether sensitive authenticated pages can be embedded in an iframe and whether important actions require only clicks.
- Exploitation / test pattern:
  - Use a controlled page/account and visually demonstrate framing without invoking destructive actions.
- Tools + exact CLI syntax (if mentioned):
  - Simple local HTML/CSS iframe test.
- Common false-positive / WAF / edge-case notes:
  - Frameability alone is not a vulnerability when no meaningful action can be triggered.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use CSP `frame-ancestors`, X-Frame-Options, confirmation steps, and SameSite cookies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 16
