# Business-Aware Vulnerability Scoring

- What it is: Organizations with unusual physical, IoT, financial, or contractual risk may need scoring factors beyond general-purpose CVSS.
- Where to look / how to identify it:
  - Identify business consequences that CVSS does not capture well, such as physical safety or partner obligations.
- Exploitation / test pattern:
  - Extend scoring carefully while keeping a mapping to a standard baseline.
- Tools + exact CLI syntax (if mentioned):
  - Internal risk model + CVSS baseline.
- Common false-positive / WAF / edge-case notes:
  - Custom models can become subjective and inconsistent if not calibrated over time.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Document formulas, review outcomes, and recalibrate against real incidents.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
