# OAuth Token Theft via Redirect Chain

- **What it is:** Multiple allowed/open redirects are chained so an OAuth token eventually reaches an external attacker origin.
- **Where to look:** OAuth flows where the immediate callback must remain on the trusted domain but later redirects are possible.
- **Test / exploitation:**
  - Locate an allowed OAuth callback that can redirect only within the trusted domain.
  - Locate another open redirect elsewhere on that trusted domain.
  - Chain the first redirect into the second redirect.
  - Run the flow with a test account.
  - Confirm whether the token/code reaches the final controlled origin.
- **Tools / syntax:**
```text
redirect_uri=https://example.com/callback?next=example.com/logout?next=attacker.com
```
- **False positives / edge cases:**
  - Redirect behavior and fragment/query preservation differ by implementation.
- **Remediation:** Validate every redirect hop and use exact registered callback URLs.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
