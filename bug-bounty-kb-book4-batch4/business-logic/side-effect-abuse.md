# Programmed Side-Effect Abuse

- What it is: Legitimate functionality can create exploitable side effects when developers fail to model how features interact at scale.
- Where to look / how to identify it:
  - Study recurring jobs, liquidity/refill processes, reconciliation logic, rewards, and secondary workflows triggered by normal actions.
- Exploitation / test pattern:
  - Model how repeated legitimate actions change global state and whether one user can influence later system decisions.
- Tools + exact CLI syntax (if mentioned):
  - Transaction logs and workflow notes.
- Common false-positive / WAF / edge-case notes:
  - Market/economic effects may be intentional behavior; prove conflict with business rules and impact.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Threat-model secondary effects, apply thresholds, and validate against external reference data where required.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
