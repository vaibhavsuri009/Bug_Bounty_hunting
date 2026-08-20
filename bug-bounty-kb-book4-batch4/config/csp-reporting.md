# CSP Violation Reporting

- What it is: CSP can report blocked resource/script violations to a collection endpoint, providing useful attack telemetry.
- Where to look / how to identify it:
  - Review whether CSP reporting is configured and whether reports are monitored.
- Exploitation / test pattern:
  - Trigger only a harmless blocked resource in a test environment to verify telemetry.
- Tools + exact CLI syntax (if mentioned):
  - CSP reporting endpoint/logging.
- Common false-positive / WAF / edge-case notes:
  - Report volume can be noisy and may include benign browser extensions.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize CSP reports, deduplicate noise, and alert on high-confidence patterns.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
