# DDoS Bandwidth Management

- What it is: Volumetric DDoS is usually mitigated upstream by infrastructure capable of absorbing and filtering more traffic than the application itself.
- Where to look / how to identify it:
  - Assess CDN/WAF/DDoS-provider capacity, routing, failover, and attack visibility.
- Exploitation / test pattern:
  - Validate configuration using provider-approved exercises rather than generating real floods.
- Tools + exact CLI syntax (if mentioned):
  - CDN/DDoS protection provider.
- Common false-positive / WAF / edge-case notes:
  - No filter perfectly distinguishes malicious from legitimate traffic.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use upstream scrubbing, autoscaling, rate limits, and tested incident runbooks.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 32
