# Manual Two-Browser Race Test

- What it is: Two authenticated sessions trigger the same one-time action almost simultaneously.
- Create only accounts/resources you control.
- Open the same one-use action (for example, an invitation) in two separate sessions.
- Align the action buttons and trigger them as close together as possible.
- Verify whether both sessions receive the protected benefit.
- The HackerOne example required multiple attempts before both invite accepts succeeded.
- False positive: both pages may show success while only one backend record is committed.
- Edge case: network latency makes manual timing unreliable for very small race windows.
- Remediation: atomically consume one-time tokens before granting the action.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 15
