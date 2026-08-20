# Stored XSS Against Privileged Viewers

- What it is: Stored input viewed by support staff, moderators, or administrators can execute in a more privileged browser context.
- Where to look / how to identify it:
  - Look for user-generated content that is later rendered in internal support, moderation, or admin interfaces.
- Exploitation / test pattern:
  - Use a harmless proof in a controlled/admin test account to demonstrate cross-role execution.
- Tools + exact CLI syntax (if mentioned):
  - Two-role test accounts and browser DevTools.
- Common false-positive / WAF / edge-case notes:
  - Do not target real staff accounts or exfiltrate real privileged data.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Render user content safely in every privileged UI, not only in public-facing pages.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
