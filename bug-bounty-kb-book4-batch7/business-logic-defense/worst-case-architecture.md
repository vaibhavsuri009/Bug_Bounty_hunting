# Worst-Case Scenario Architecture

- What it is: Business logic vulnerabilities are best prevented by designing for malicious and extreme use cases rather than the median expected user.
- Where to look / how to identify it:
  - For every feature, list intended behavior and the worst realistic misuse/edge cases before coding.
- Exploitation / test pattern:
  - Choose designs that remain safe when rare inputs, repeated actions, or adversarial sequences occur.
- Tools + exact CLI syntax (if mentioned):
  - Threat modeling/design review.
- Common false-positive / WAF / edge-case notes:
  - Overengineering impossible threats can waste resources; focus on plausible high-impact cases.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Require abuse cases and worst-case paths in architecture reviews.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 36
