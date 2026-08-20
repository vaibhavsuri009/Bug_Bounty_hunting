# Data-in-Transit Encryption Requirement

- What it is: Credentials, PII, financial data, and session material must be protected while crossing networks.
- Where to look / how to identify it:
  - Map every network hop including browser-to-server and service-to-service communication.
- Exploitation / test pattern:
  - Require HTTPS/TLS for all sensitive flows and reject downgrade/cleartext paths.
- Tools + exact CLI syntax (if mentioned):
  - TLS configuration/server settings.
- Common false-positive / WAF / edge-case notes:
  - HTTPS at the edge is insufficient if internal hops carrying secrets remain cleartext.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use modern TLS everywhere sensitive data travels and automate certificate management.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
