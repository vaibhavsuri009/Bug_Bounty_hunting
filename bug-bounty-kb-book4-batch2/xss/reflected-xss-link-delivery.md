# Reflected XSS Link Delivery

- What it is: Reflected XSS can be delivered through a crafted URL when the vulnerable input is controlled by query/path data.
- Where to look / how to identify it:
  - Identify a reflected parameter and confirm that a crafted link recreates the execution in a controlled account/browser.
- Exploitation / test pattern:
  - Use non-destructive proof and avoid sending crafted links to third parties.
- Tools + exact CLI syntax (if mentioned):
  - Browser and local HTML link if needed.
- Common false-positive / WAF / edge-case notes:
  - Some payloads require additional user interaction or specific browser behavior.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Encode reflected values by context and validate allowed input.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
