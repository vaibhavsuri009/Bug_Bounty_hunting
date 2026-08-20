# Two-Account Authorization Testing

- **What it is:** A systematic way to detect horizontal and vertical IDORs by comparing access between controlled accounts.
- **Where to look:** Any feature that reads private data or modifies account state.
- Create two accounts for each available role or privilege level.
- Use one as the attacker and one as the victim.
- Test same-role access first, then cross-role access.
- Also repeat important checks while unauthenticated.
- Use separate browsers or profiles so both sessions remain active.
- Capture requests from the attacker session in Burp.
- Substitute identifiers belonging to the victim session.
- Observe the victim account separately to confirm unauthorized effects.
- **Tools:** Burp Proxy for interception and request modification.
- **False positives / edge cases:** Do not treat intentionally shared/public resources as IDORs.
- **Remediation:** Authorize the authenticated principal against the requested object on every request.

## Source: Bug Bounty Bootcamp, Ch. 10
