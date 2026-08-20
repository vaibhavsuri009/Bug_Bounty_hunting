# Autoscaling Cost-Abuse Risk

- What it is: Cloud autoscaling can turn traffic spikes into significant infrastructure costs even when service remains available.
- Where to look / how to identify it:
  - Review autoscale thresholds, rate limits, queue depth, and per-user request costs in a controlled environment.
- Exploitation / test pattern:
  - Model cost impact rather than generating abusive traffic.
- Tools + exact CLI syntax (if mentioned):
  - Cloud monitoring/billing simulation.
- Common false-positive / WAF / edge-case notes:
  - High autoscaling spend is not necessarily a vulnerability if rate and budget controls are intentional.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply per-user quotas, WAF/rate limiting, budget alarms, and scaling safeguards.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 14
