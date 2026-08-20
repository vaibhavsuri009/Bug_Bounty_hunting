# Autorize Two-User Authorization Check

- What it is: Burp Autorize replays User A actions using User B credentials to surface BOLA-style authorization failures.
- Create two controlled accounts with separate session tokens.
- Configure Autorize with the alternate account token.
- Browse the application normally as User A and create/access resources.
- Let Autorize replay those requests as User B.
- Review highlighted requests where B receives data/actions intended only for A.
- Manually reproduce interesting cases in Repeater before reporting.
- False positive: shared/public resources can legitimately work for both users.
- Edge case: CSRF tokens or per-request nonces may need normalization before replay.
- Remediation: perform object-level authorization on every endpoint.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
