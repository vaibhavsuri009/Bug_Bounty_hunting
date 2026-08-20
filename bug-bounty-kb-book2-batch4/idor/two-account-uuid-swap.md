# UUID IDOR with Two Controlled Accounts

- What it is: Unguessable UUIDs still fail authorization if one user's UUID works in another user's session.
- Create account A and account B.
- Obtain an object UUID from account A.
- While authenticated as B, replay the request using A's UUID.
- Compare the response with B's own object and an invalid UUID.
- This avoids random brute force and cleanly proves broken object authorization.
- False positive: the object may intentionally be shared/public between both accounts.
- Edge case: some programs treat unguessable IDs as adequate only until you show realistic ID leakage.
- Remediation: check ownership/permissions on every request regardless of identifier entropy.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 16
