# CVSS Base Scoring

- What it is: CVSS base scoring estimates intrinsic vulnerability severity using exploitability and impact metrics.
- Where to look / how to identify it:
  - Score Attack Vector, Attack Complexity, Privileges Required, User Interaction, Scope, Confidentiality, Integrity, and Availability.
- Exploitation / test pattern:
  - Use the score to support prioritization after the vulnerability has been reproduced.
- Tools + exact CLI syntax (if mentioned):
  - CVSS v3.1 calculator as used in the book.
- Common false-positive / WAF / edge-case notes:
  - CVSS is general-purpose and may not represent unusual chained or business-logic issues accurately.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Combine technical scoring with business context and asset criticality.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
