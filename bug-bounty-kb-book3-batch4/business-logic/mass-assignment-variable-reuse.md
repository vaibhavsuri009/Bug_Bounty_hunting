# Mass Assignment Variable Reuse Across Endpoints

- What it is: Parameters observed in one endpoint may be accepted unexpectedly by another endpoint using the same backend model.
- Where to look / how to identify it:
  - Collect unknown/sensitive fields from GET/admin responses and reuse them in create/update requests, e.g. toggling `mfa`, changing account IDs, or role-like values on controlled accounts.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Response changes can come from generic schema handling rather than persistence.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Separate read models from write models and allowlist write fields.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
