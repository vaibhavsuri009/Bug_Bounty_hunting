# Numeric ID Swap IDOR

- **What it is:** Missing object-level authorization lets one user access another user's resource by changing a predictable ID.
- **Where to look:** URLs, form fields, JSON bodies, headers, cookies, and paths containing user IDs, message IDs, file IDs, group IDs, or similar references.
- Create two test accounts: attacker and victim.
- Capture a sensitive request from the attacker account.
- Replace the attacker's object ID with the victim's ID.

```http
GET /messages?user_id=1236
```

- Repeat for state-changing requests such as delete/update operations.
- **False positives / edge cases:** A changed response is not enough; confirm the returned or modified object actually belongs to the other test account.
- **Remediation:** Enforce server-side authorization for every object access, independent of client-supplied IDs.

## Source: Bug Bounty Bootcamp, Ch. 10
