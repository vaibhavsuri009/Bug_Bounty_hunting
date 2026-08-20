# Stored XSS

- What it is: Attacker-controlled script is stored server-side and later rendered in another user's browser.
- Where to look: Comments, profiles, posts, support messages, logs, message boards, and any persistent user-controlled field.
- Test with a harmless proof-of-concept marker:
```html
<script>alert('XSS')</script>
```
- Submit the payload, then revisit every page/context where that value is displayed.
- Test with separate low-privilege accounts to see whether one user's input executes for another user.
- Stored XSS is higher impact when it reaches many users or privileged/admin interfaces.
- False-positive/edge note: Mere storage is not enough; the payload must execute in a victim-relevant browser context.
- WAF/edge note: Execution may happen later or only in an admin/logging interface.
- Remediation: Contextually encode output and validate/sanitize untrusted input before rendering.

## Source: Bug Bounty Bootcamp, Ch. 6
