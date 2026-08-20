# Concurrent Request Limit Bypass with Burp

- What it is: Multiple simultaneous requests pass the same quota check before the counter is decremented.
- Look for actions limited by count: invitations, coupons, redemptions, withdrawals, or API quotas.
- Capture one valid request in Burp.
- Generate multiple requests with different controlled payload values.
- Send them concurrently/near-concurrently and compare the final server-side count.
- The Keybase example exceeded a three-invite limit by racing invite requests.
- False positive: temporary success responses may later be rolled back asynchronously.
- Edge case: concurrency support differs by Burp version/tooling.
- Remediation: lock or atomically decrement the quota before fulfilling each request.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 15
