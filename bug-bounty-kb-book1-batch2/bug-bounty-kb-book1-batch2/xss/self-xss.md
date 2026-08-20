# Self-XSS

- What it is: Script execution occurs only when the victim manually inserts the attack payload into their own context.
- Where to look: User-only profile/dashboard fields, browser console pasting, or values visible only to the same account.
- Verify whether any technical path exists for another attacker to deliver the payload automatically.
- If execution requires the victim to copy/paste code or manually modify their own field, classify it as self-XSS.
- Check whether another bug can convert self-XSS into cross-user XSS, such as CSRF or broken access control.
- Re-test the same sink from a second account to determine whether the value is truly private to the submitting user.
- Record the exact user interaction required before JavaScript executes.
- Do not overstate impact when no cross-user delivery path exists.
- Common false-positive trap: Many bug bounty programs reject pure self-XSS because it requires social engineering.
- WAF/edge note: Successful `alert()` in your own account alone does not prove exploitable XSS against another user.
- Remediation: Encode untrusted output anyway, and prevent unsafe client-side rendering paths.

## Source: Bug Bounty Bootcamp, Ch. 6
