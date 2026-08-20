# Attack Vector Cross-Analysis

- What it is: Attack vectors are best derived by cross-referencing logic design, technical design, and threat actors.
- Where to look / how to identify it:
  - For every actor, ask which feature rules and technical components they can influence.
- Exploitation / test pattern:
  - Record potential attacks, affected component, actor prerequisites, and severity before implementation.
- Tools + exact CLI syntax (if mentioned):
  - Threat-model matrix.
- Common false-positive / WAF / edge-case notes:
  - Attack vectors are potential risks, not confirmed vulnerabilities.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prioritize high-severity plausible vectors and implement mitigations before release.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
