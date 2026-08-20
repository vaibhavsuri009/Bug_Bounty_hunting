# MongoDB ObjectId Fingerprinting

- What it is: MongoDB ObjectIds have a recognizable 12-byte structure that can signal MongoDB use in requests/responses.
- Where to look / how to identify it:
  - Look for `_id` values resembling 24-character hexadecimal strings and recurring object-ID placement.
- Exploitation / test pattern:
  - Correlate the identifier shape with other MongoDB evidence before classifying the database.
- Tools + exact CLI syntax (if mentioned):
  - Example: `507f1f77bcf86cd799439011`.
- Common false-positive / WAF / edge-case notes:
  - Developers can override default key generation, and other systems can emit similar hex IDs.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Do not expose unnecessary database identifiers and avoid relying on identifier secrecy for authorization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
