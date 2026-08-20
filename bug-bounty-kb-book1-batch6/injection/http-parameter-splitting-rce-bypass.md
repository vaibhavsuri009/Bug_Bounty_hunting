# Duplicate-Parameter RCE Filter Bypass

- **What it is:** A filter inspects individual duplicate parameters, while the backend concatenates their values into one executable string.
- **Where to look:** Endpoints that accept duplicate parameter names and normalize/merge them server-side.
- **Test / exploitation:**
  - Confirm the application accepts duplicate parameters.
  - Split a blocked keyword across two parameters with the same name.
  - Intercept the request to verify the literal blocked keyword is absent on the wire.
  - Observe whether backend processing concatenates the values.
  - Confirm execution with a harmless command.
- **Tools / syntax:**
```text
GET /calculator?calc="__import__('os').sy"&calc="stem('ls')"
```
- **False positives / edge cases:**
  - Frameworks may keep only first/last values instead of concatenating them.
- **Remediation:** Reject ambiguous duplicate parameters and enforce security validation after canonicalization.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
