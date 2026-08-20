# OAuth Token Theft via Open Redirect

- **What it is:** An allowlisted redirect_uri contains an open redirect that forwards an OAuth token/code to an attacker-controlled origin.
- **Where to look:** OAuth authorization flows using redirect_uri and an allowlist of callback URLs.
- **Test / exploitation:**
  - Identify the OAuth authorization request and its redirect_uri.
  - Find an open redirect under an allowed callback/domain.
  - Set redirect_uri to the vulnerable callback plus its redirect parameter.
  - Complete the flow using only your own test account.
  - Verify whether the token/code survives the redirect and reaches your controlled destination.
- **Tools / syntax:**
```text
redirect_uri=https://example.com/callback?next=attacker.com
```
- **False positives / edge cases:**
  - A redirect is not enough if the provider strips sensitive OAuth values before leaving the trusted origin.
- **Remediation:** Require exact callback matching and eliminate open redirects from allowed redirect targets.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
