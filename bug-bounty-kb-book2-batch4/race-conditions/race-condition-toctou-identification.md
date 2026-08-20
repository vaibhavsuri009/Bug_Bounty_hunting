# Race Condition / TOCTOU Identification

- What it is: A condition is checked, then becomes stale before the action using it completes.
- Look for workflows that do: database lookup -> logic -> database update.
- High-value cases include one-time tokens, balances, quotas, inventory, invitations, and verification states.
- Identify the "time of check" and "time of use" separately.
- Try sending two equivalent requests nearly simultaneously.
- Repeat tests because timing-sensitive flaws may not trigger every attempt.
- False positive: duplicate client responses do not matter if the backend commits only one state change.
- Edge case: asynchronous jobs can widen the race window.
- Remediation: perform condition check and state update atomically with locking/transactions.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 15
