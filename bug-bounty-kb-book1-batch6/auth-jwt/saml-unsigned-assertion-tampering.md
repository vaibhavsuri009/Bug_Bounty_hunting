# SAML Unsigned Assertion Tampering

- **What it is:** A service provider accepts identity assertions without verifying a cryptographic signature.
- **Where to look:** SAML responses carrying username, email, userID, or other identity attributes.
- **Test / exploitation:**
  - Intercept the SAML response during login.
  - Decode it if transported in base64 or another encoding.
  - Identify the attribute used as the user identity.
  - Modify only your test assertion to another test identity/role value.
  - Re-encode the message and submit it to determine whether the service provider accepts the tampered identity.
- **False positives / edge cases:**
  - A modified response that is rejected indicates signature/integrity validation may be working.
- **Remediation:** Require and verify trusted SAML signatures on every authentication response/assertion.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
