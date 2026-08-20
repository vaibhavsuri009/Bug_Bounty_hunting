# DDoS Blackhole Routing

- What it is: Blackhole systems route suspicious traffic away from productive application servers to preserve resources for legitimate users.
- Where to look / how to identify it:
  - Review routing/filter criteria and capacity during architecture/incident planning.
- Exploitation / test pattern:
  - Test with synthetic labeled traffic in a staging/network simulation.
- Tools + exact CLI syntax (if mentioned):
  - Network routing/load-balancer controls.
- Common false-positive / WAF / edge-case notes:
  - Overaggressive blackholing can discard legitimate users and is less effective against very large attacks.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Combine traffic baselines, upstream filtering, and carefully tuned diversion rules.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 32
