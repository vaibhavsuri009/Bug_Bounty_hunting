# CVSS Attack Complexity

- What it is: Attack Complexity captures prerequisites and external conditions outside the attacker's control.
- Where to look / how to identify it:
  - Count required setup, timing, race conditions, victim state, recon, and environmental dependencies.
- Exploitation / test pattern:
  - Classify repeatable attacks with little setup as Low and attacks dependent on specific conditions as High.
- Tools + exact CLI syntax (if mentioned):
  - CVSS calculator.
- Common false-positive / WAF / edge-case notes:
  - Many steps do not automatically mean High if the attacker fully controls them.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Document prerequisites alongside the score so severity decisions remain reviewable.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
