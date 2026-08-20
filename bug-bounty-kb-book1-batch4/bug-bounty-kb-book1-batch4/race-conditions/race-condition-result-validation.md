# Race Condition Result Validation

- **What it is:** A race-condition finding is confirmed by proving that concurrent requests changed final state beyond what sequential business logic allows.
- **Where to look:** The destination balance, credit count, vote count, redemption state, inventory, or access-control result after the concurrent test.
- Establish the initial state before testing.
- Send the concurrent requests.
- Re-read the authoritative application state after processing completes.
- Compare the final state with the maximum outcome permitted by one valid request.
- If the action is nondeterministic, repeat the same controlled test several times.
- Record both the request batch and before/after state for the PoC.
- The book notes that scheduler timing makes races probabilistic, so a failed first attempt does not disprove the flaw.
- **False positives / edge cases:** Do not rely only on multiple `200` responses; some requests may later be rolled back.
- **Remediation:** Enforce consistency at the transaction/resource layer, not only in request handling code.

## Source: Bug Bounty Bootcamp, Ch. 12
