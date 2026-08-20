# Frontend-Only Permission Enforcement

- What it is: A permission hides a UI control but the backend endpoint still accepts the action.
- Use a privileged controlled account to capture the legitimate HTTP request.
- Remove the permission or switch to a restricted controlled account.
- Replay the same request directly with Burp Repeater.
- The Shopify example showed a hidden phone-number field while the backend endpoint still accepted updates.
- Verify the protected action actually took effect server-side.
- False positive: a `200` response may be generic while the update is silently rejected.
- Edge case: different API versions may enforce permissions inconsistently.
- Remediation: enforce authorization on the server for every sensitive action.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
