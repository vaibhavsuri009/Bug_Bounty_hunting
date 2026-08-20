# Postman Collection Runner

- What it is: Collection Runner executes an entire API request collection in a controlled sequence.
- Select the target collection and corresponding environment.
- Set request order, iteration count, and an optional delay.
- Use delay settings to respect documented rate limits.
- Run the collection and review the summary for failures or unexpected responses.
- Add tests to automatically flag status/body/timing anomalies.
- False positive: a failed request may simply depend on state created by an earlier skipped request.
- Edge case: state-changing requests can produce side effects across repeated iterations.
- Remediation note: provide deterministic test environments and enforce idempotency where appropriate.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
