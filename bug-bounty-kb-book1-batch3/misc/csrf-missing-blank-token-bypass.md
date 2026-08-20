# CSRF Missing or Blank Token Bypass

- **What it is:** Exploits validation logic that checks a token only when the parameter is present/non-empty.
- **Where to look:** Requests containing an anti-CSRF parameter that appears mandatory.
- Send the state-changing request with the token parameter removed.
- Repeat with the parameter present but blank.

```text
new_password=test-value
new_password=test-value&csrf_token=
```

- If either request succeeds, the validation likely has a presence-check logic flaw.
- Confirm only against your own test account.
- **False positives / edge cases:** Some frameworks return success-like responses while silently ignoring the state change; verify the actual account state.
- **Remediation:** Reject missing/blank tokens before any state-changing logic executes.

## Source: Bug Bounty Bootcamp, Ch. 9
