# CSRF State-Changing Request Discovery

- **What it is:** Identifies authenticated actions that may be forgeable cross-site.
- **Where to look:** Password/email changes, sends, deletes, transfers, profile updates, and other data mutations.
- Log in with a test account and browse every workflow while Burp/ZAP records requests.
- Build a list containing endpoint, method, and parameters for each state-changing action.

```text
POST /password_change    new_password
POST /send_email         draft_id,recipient_id
POST /delete_email       email_id
```

- Search intercepted requests for `csrf`, `state`, anti-CSRF headers, cookies, or hidden parameters.
- **False positives / edge cases:** SameSite cookies or origin/referer validation may protect an endpoint even without an obvious token.
- **Remediation:** Require robust CSRF defenses on every authenticated state-changing request.

## Source: Bug Bounty Bootcamp, Ch. 9
