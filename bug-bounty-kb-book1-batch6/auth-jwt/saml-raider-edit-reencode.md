# SAML Response Editing and Re-encoding

- **What it is:** SAML testing requires decoding, editing, and restoring the transport encoding before replaying the response.
- **Where to look:** SAML login flows where the response is encoded rather than plain XML.
- **Test / exploitation:**
  - Intercept the response as the browser sends it to the service provider.
  - Decode the SAML message to inspect XML fields.
  - Make one controlled change at a time.
  - Restore the message to its original encoding.
  - Replay it and compare the authentication outcome.
- **Tools / syntax:**
  - Burp Suite extension: SAML Raider can assist with editing and re-encoding SAML messages.
- **False positives / edge cases:**
  - Malformed encoding may cause parser errors unrelated to signature validation.
- **Remediation:** Use strict SAML libraries that validate structure, signature, issuer, audience, and replay conditions.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
