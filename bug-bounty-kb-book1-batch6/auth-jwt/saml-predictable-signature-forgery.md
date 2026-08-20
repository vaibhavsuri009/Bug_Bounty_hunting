# SAML Predictable Signature Forgery

- **What it is:** A weak/predictable signing scheme lets an attacker recalculate a signature after changing the identity assertion.
- **Where to look:** SAML responses where signatures show an obvious deterministic relationship to user-controlled identity data.
- **Test / exploitation:**
  - Collect multiple SAML responses from your own test identities.
  - Compare identity fields with corresponding signatures.
  - Look for trivial encodings or predictable transformations.
  - If the relationship is confirmed, recalculate the signature for a controlled alternate identity.
  - Submit the re-encoded response and verify whether it is accepted.
- **False positives / edge cases:**
  - Base64 is encoding, not a secure signature; however, do not assume predictability from one sample.
- **Remediation:** Use standard cryptographic XML signatures with protected signing keys.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 20
