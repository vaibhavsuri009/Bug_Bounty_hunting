# Race Condition Target Selection

- **What it is:** Race-condition testing is most effective against actions that should succeed once but fail when repeated concurrently.
- **Where to look:** Numerical balances, one-time redemptions, voting, payment, transfer, credit, coupon, inventory, and access-control workflows.
- Map state-changing endpoints while browsing with Burp.
- Record the request that updates the sensitive number or state flag.
- Choose a test where one request is valid by itself.
- Ensure the same operation should not be valid multiple times in parallel.
- Avoid tests where every request would independently be allowed.
- Avoid tests where even one request should always be rejected.
- Copy the request for controlled concurrent replay.
- **Tools:** In Burp, right-click the request and use **Copy as curl command**.
- **False positives / edge cases:** Business rules may intentionally permit repeated actions; confirm expected semantics first.
- **Remediation:** Serialize conflicting operations around the shared resource.

## Source: Bug Bounty Bootcamp, Ch. 12
