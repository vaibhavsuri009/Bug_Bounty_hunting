# OAuth Token Lifetime / Revocation Test

- **What it is:** Access tokens remain usable longer than intended, including after logout or password reset.
- **Where to look:** OAuth applications issuing reusable bearer/access tokens.
- **Test / exploitation:**
  - Obtain an access token from your own test account.
  - Use it once to confirm the normal authorized resource request.
  - Log out and retry the same token.
  - Reset the test account password and retry the same token.
  - Record whether the token remains valid after each security event.
- **False positives / edge cases:**
  - Some OAuth designs intentionally use long-lived tokens; impact depends on expected revocation policy and scope.
- **Remediation:** Expire and revoke tokens appropriately, especially after account security events.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
