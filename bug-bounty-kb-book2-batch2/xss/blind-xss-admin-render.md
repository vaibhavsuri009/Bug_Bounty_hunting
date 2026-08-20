# Blind XSS in Privileged Render Paths

- What it is: Stored input executes only when another user—often an administrator—views it.
- Look for profile fields, support tickets, logs, contact forms, or records likely rendered in back-office pages.
- Submit a callback-capable blind-XSS payload only within program rules.
- The book specifically mentions XSSHunter as a detection service for blind XSS.
- Prefer a minimal callback that records execution; avoid collecting unnecessary sensitive DOM/cookie data.
- Compare normal-user rendering with likely administrative rendering paths.
- False positive: a callback from your own session is not proof of cross-user execution.
- Edge case: `HttpOnly` cookies remain unreadable even when JavaScript executes.
- Record the origin, page path, and viewer context returned by the callback.
- Remediation: encode all user-controlled data in administrative interfaces as rigorously as public pages.
- Use a unique per-test identifier so callbacks can be correlated to the exact injected field.
- Remediation testing: confirm the same value is safely encoded in both user-facing and administrative views.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
