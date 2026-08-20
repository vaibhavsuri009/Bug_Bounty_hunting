# Prefer Text-Only DOM Insertion

- What it is: Treating user-supplied data as text rather than DOM dramatically reduces XSS exposure.
- Where to look / how to identify it:
  - Review rendering code for cases where plain text is inserted using HTML-capable APIs.
- Exploitation / test pattern:
  - Replace unsafe HTML insertion with text-based DOM APIs when formatting is unnecessary.
- Tools + exact CLI syntax (if mentioned):
  - `innerText`/`textContent` instead of `innerHTML`.
- Common false-positive / WAF / edge-case notes:
  - Browser-specific behavior still matters, but text APIs remove most markup interpretation.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Default user-generated content to text and explicitly opt into sanitized HTML only when required.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
