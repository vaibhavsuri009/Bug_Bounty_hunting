# Predictable Randomized ID Analysis

- **What it is:** Supposedly random or hashed object IDs may still be guessable if generated with insufficient entropy.
- **Where to look:** UUID-like, token-like, hashed, or randomized identifiers used directly to retrieve resources.
- Generate several controlled accounts or objects.
- Record their identifiers in creation order.
- Compare length, prefixes, suffixes, timestamps, counters, and repeated segments.
- Look for a deterministic pattern or low-entropy component.
- Predict a neighboring identifier only for a controlled victim object.
- Request that object through the normal endpoint.
- Compare both read and write endpoints because one route may authorize correctly while another does not.
- **False positives / edge cases:** A predictable ID is not exploitable if access control rejects unauthorized users.
- **Remediation:** Use strong random identifiers as defense-in-depth and enforce authorization independently.

## Source: Bug Bounty Bootcamp, Ch. 10
