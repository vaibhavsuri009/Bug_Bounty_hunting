# API: Excessive Data Exposure

- **What it is:** API responses contain sensitive fields that the client UI does not need or display.
- **Where to look:** Raw JSON/XML responses for profile, account, admin, and object-fetch endpoints.
- **Method:** Compare rendered UI with the full proxy response and identify private tokens, IDs, internal fields, or personal data.
- **Source pattern:** A public profile response can leak the profile owner’s private API token even when the page appears harmless.
- **Validate:** Determine whether the current caller is authorized to know each field.
- **False positives:** Some extra fields may be intentionally public; confirm confidentiality expectations.
- **Remediation:** Return only fields required by the caller and enforce field-level authorization.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
