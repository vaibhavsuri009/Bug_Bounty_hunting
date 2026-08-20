# Statistical Modeling of Inputs

- What it is: Input modeling uses observed or hypothesized user data distributions to systematically test common and rare values.
- Where to look / how to identify it:
  - Model all interactive fields including dropdowns, free text, radio buttons, ranges, and unusual character/length cases.
- Exploitation / test pattern:
  - Store modeled values in a machine-readable format for automated testing.
- Tools + exact CLI syntax (if mentioned):
  - JSON/YAML/CSV/XML model.
- Common false-positive / WAF / edge-case notes:
  - Analytics can overrepresent common users and miss novel attacker behavior.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Combine real distributions with deliberately rare adversarial edge cases.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 36
