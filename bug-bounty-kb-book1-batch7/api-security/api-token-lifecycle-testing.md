# API: Access-Token Lifecycle Testing

- **What it is:** Check whether API tokens are issued, validated, generated, and invalidated securely.
- **Recon questions from source:** Which endpoints require tokens? How are tokens generated? Can a token be obtained without login? Do tokens expire after password reset/update?
- **Method:** Capture a valid token, test endpoint access with/without it, then repeat after logout and credential changes.
- **Also inspect:** Predictability/randomness and whether the server actually validates presented tokens.
- **False positives:** Long-lived tokens may be intentional, but impact depends on privilege and revocation model.
- **Edge case:** Different privilege levels can use different token types/scopes.
- **Remediation:** Generate high-entropy scoped tokens, validate every request, and revoke on security-relevant events.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
