# Mass Assignment + BFLA Chain

- What it is: A BFLA that edits another user's profile can become account takeover if hidden security fields are also mass-assignable.
- Where to look / how to identify it:
  - On controlled accounts, first prove B can modify A's profile; then test sensitive fields such as email or MFA state; verify only through your own password-reset flow.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Profile modification alone does not prove account takeover.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce object authorization and property-level authorization on every update.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
