# Skippable Authentication Step

- **What it is:** A multi-step authentication flow lets a user jump directly to a later step without completing earlier checks.
- **Where to look:** MFA, security-question, password-reset, onboarding, approval, and other multi-step flows.
- **Test / exploitation:**
  - Map every URL in the intended authentication sequence.
  - Complete the flow once normally and record redirects and state transitions.
  - Request a later-stage URL directly before completing earlier stages.
  - If the later stage grants a session or privileged state, the earlier control is bypassable.
  - Repeat with a fresh session to rule out cached authentication state.
- **False positives / edge cases:**
  - A redirect to a later page is not enough; confirm the server grants the resulting authenticated state.
- **Remediation:** Enforce every prerequisite server-side at each stage, not only through redirects or client flow.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 17
