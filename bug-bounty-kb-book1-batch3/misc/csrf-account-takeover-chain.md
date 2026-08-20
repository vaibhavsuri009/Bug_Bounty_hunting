# CSRF Account-Takeover Chain

- **What it is:** Turns CSRF on a credential-management endpoint into account takeover.
- **Where to look:** Set-password, change-password, email-change, password-reset, or account-linking actions.
- Prioritize flows that do not require the old password or fresh re-authentication.
- Verify with a dedicated test account whether a forged request can set attacker-chosen authentication data.

```text
POST /set_password
password=<TEST_VALUE>&csrf_token=
```

- After the state change, verify only on the test account that the new credential works.
- **False positives / edge cases:** Re-authentication, MFA, confirmation links, or existing-password checks can break the chain.
- **Remediation:** Require robust CSRF protection plus re-authentication for credential and account-recovery changes.

## Source: Bug Bounty Bootcamp, Ch. 9
