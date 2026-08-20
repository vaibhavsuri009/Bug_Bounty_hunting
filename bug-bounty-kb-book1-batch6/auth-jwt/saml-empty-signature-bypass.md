# SAML Empty/Removed Signature Bypass

- **What it is:** Signature validation runs only when a signature field exists, so emptying or removing it skips the check.
- **Where to look:** SAML responses that normally contain Signature/SignatureValue elements.
- **Test / exploitation:**
  - Intercept and decode a legitimate SAML response.
  - Change a test identity attribute.
  - First empty the SignatureValue element and submit the response.
  - If rejected, remove the Signature element entirely and retry.
  - Re-encode before sending; confirm only with controlled test accounts.
- **Tools / syntax:**
```text
<saml:Signature><saml:SignatureValue></saml:SignatureValue></saml:Signature>
```
- **False positives / edge cases:**
  - Successful decoding/re-encoding alone is not a bypass; the altered identity must be accepted.
- **Remediation:** Reject unsigned responses and validate signatures unconditionally.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
