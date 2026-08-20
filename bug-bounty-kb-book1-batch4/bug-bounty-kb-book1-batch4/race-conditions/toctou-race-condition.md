# TOCTOU Race Condition

- **What it is:** A time-of-check/time-of-use flaw occurs when a sensitive action is separated from its authorization or state check and concurrent requests slip between them.
- **Where to look:** Operations that check a limit, balance, eligibility flag, usage count, or "already used" state before modifying data.
- Identify the check and the subsequent state-changing action.
- Ask whether two requests can both pass the check before either commits the update.
- Typical targets mentioned in the book include transfers, payments, gift-card balances, votes, and score/credit systems.
- Capture the exact state-changing request in a proxy.
- Send multiple copies concurrently.
- Check whether the application performs an action more times than its business rule permits.
- Measure the final authoritative state rather than trusting per-request success responses.
- **False positives / edge cases:** Multiple successful requests are expected if the action is legitimately repeatable.
- **Remediation:** Make check-and-update operations atomic using synchronization/locking or equivalent transactional controls.

## Source: Bug Bounty Bootcamp, Ch. 12
