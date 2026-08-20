# Security Light Patterns

- What it is: Light patterns guide users toward safer choices at the moment risky functionality is used instead of relying on documentation alone.
- Where to look / how to identify it:
  - Identify optional controls such as transaction caps, MFA, privacy settings, or recovery protection.
- Exploitation / test pattern:
  - Place contextual prompts near high-risk actions and measure adoption without coercive dark patterns.
- Tools + exact CLI syntax (if mentioned):
  - UX design/analytics.
- Common false-positive / WAF / edge-case notes:
  - Light patterns are weaker than secure-by-default controls.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use secure defaults whenever feasible and contextual security prompts when choice is necessary.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 23
