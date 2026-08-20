# Security Blocklist Anti-Pattern

- What it is: Blocklists only deny known bad inputs and fail when attackers choose new representations or unknown values.
- Where to look / how to identify it:
  - Search validation logic for arrays/regexes of forbidden domains, commands, strings, or payload signatures.
- Exploitation / test pattern:
  - Test harmless alternate values to determine whether the intended policy is truly enforced.
- Tools + exact CLI syntax (if mentioned):
  - Source review/unit tests.
- Common false-positive / WAF / edge-case notes:
  - Blocklists can be useful as supplementary detection but should not be the primary security boundary.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer allowlists and positive validation of permitted inputs.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 25
