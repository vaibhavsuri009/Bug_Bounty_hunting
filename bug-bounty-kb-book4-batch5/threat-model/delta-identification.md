# Threat Model Delta Identification

- What it is: Delta identification removes threats with sufficient controls and leaves the unmitigated risks that still require engineering work.
- Where to look / how to identify it:
  - Cross-reference the attack-vector list with verified existing mitigations.
- Exploitation / test pattern:
  - Create a remaining-risk list with severity, actor, component, owner, and required control.
- Tools + exact CLI syntax (if mentioned):
  - Threat-model table.
- Common false-positive / WAF / edge-case notes:
  - Partial controls may reduce severity without fully removing a threat.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Do not launch high-risk functionality until unacceptable deltas are mitigated or formally accepted.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
