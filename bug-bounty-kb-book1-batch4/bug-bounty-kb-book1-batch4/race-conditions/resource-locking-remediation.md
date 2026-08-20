# Race Condition Remediation with Resource Locking

- **What it is:** Synchronization prevents concurrent threads from modifying the same security-sensitive resource at the same time.
- **Where to apply:** Shared balances, counters, one-time tokens, redemption flags, inventory, and any check-then-update workflow.
- Lock the relevant resource before reading security-sensitive state.
- Keep the lock through the validation and state-changing update.
- Release the lock only after the operation has committed.
- A second request must wait until the first operation finishes.
- Use the language/framework/database synchronization primitives appropriate to the application.
- Apply least privilege so a race cannot escalate into broader compromise if another flaw exists.
- Prefer database transactions or equivalent atomic primitives when the shared resource is persisted.
- **False positives / edge cases:** Locking the wrong granularity can still leave independent shared resources exposed to races.
- **Remediation:** Make the security decision and corresponding update atomic under synchronization or transactional isolation.

## Source: Bug Bounty Bootcamp, Ch. 12
