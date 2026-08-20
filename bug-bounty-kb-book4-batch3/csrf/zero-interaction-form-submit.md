# Zero-Interaction Form Submission

- What it is: JavaScript can auto-submit a prepared form, removing user interaction from a CSRF proof of concept when script execution is available.
- Where to look / how to identify it:
  - Use only in a controlled lab or when a benign XSS/test page is explicitly authorized.
- Exploitation / test pattern:
  - Programmatically submit a harmless form and verify whether the target accepts it.
- Tools + exact CLI syntax (if mentioned):
  - DOM form `.submit()` is the key browser behavior.
- Common false-positive / WAF / edge-case notes:
  - This technique normally depends on script execution or a page the tester controls.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Protect the target endpoint with server-side CSRF validation rather than relying on user interaction.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
