# Clickjacking Impact Chaining

- **What it is:** Chains multiple click-driven actions to turn a low-impact framing flaw into meaningful account impact.
- **Where to look:** Multiple frameable state-changing pages under the same authenticated application.
- Map which actions can be executed entirely by clicks.
- Look for sequences such as changing a notification/billing destination and then triggering a report or export.
- Build a PoC only with your own account and non-sensitive test data.

```text
1. Change destination setting
2. Trigger send/export action
3. Verify the test data reaches the controlled destination
```

- **False positives / edge cases:** Each additional required click lowers reliability; report actual interaction requirements.
- **Remediation:** Protect every state-changing page from cross-origin framing, not just the most obvious sensitive page.

## Source: Bug Bounty Bootcamp, Ch. 8
