# SSO Mechanism Fingerprinting

- **What it is:** Determines whether an application uses shared cookies, SAML, or OAuth for single sign-on.
- **Where to look:** Authentication traffic, cookies, redirects, XML messages, and OAuth authorization requests.
- **Test / exploitation:**
  - Inspect Set-Cookie Domain attributes for parent-domain cookie sharing.
  - Intercept login traffic and search for saml or XML-like SAML messages.
  - Search authentication requests for oauth, client_id, redirect_uri, scope, state, or response_type.
  - Map which service acts as identity provider and which acts as service provider.
  - Use the mechanism-specific tests only after identification.
- **False positives / edge cases:**
  - A generic third-party login button does not prove the exact protocol in use.
- **Remediation:** Use well-maintained SSO implementations and enforce protocol-specific validation.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
