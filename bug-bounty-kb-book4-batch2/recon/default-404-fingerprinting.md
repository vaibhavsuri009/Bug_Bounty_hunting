# Default 404 Fingerprinting

- What it is: Default error pages can fingerprint server-side frameworks and sometimes narrow their version range.
- Where to look / how to identify it:
  - Trigger a harmless nonexistent path and compare HTML/CSS/text markers with historical framework defaults.
- Exploitation / test pattern:
  - Use open-source history to date when specific markers appeared or disappeared.
- Tools + exact CLI syntax (if mentioned):
  - Git history/release notes plus browser View Source.
- Common false-positive / WAF / edge-case notes:
  - Custom error pages and reverse proxies can invalidate the fingerprint.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use generic custom error pages and avoid exposing framework/version-specific details.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
