# Direct XXE File-Read Test

- What it is: Direct XXE occurs when user-supplied XML is parsed and external entity content is returned in the normal response.
- Where to look / how to identify it:
  - Prioritize XML-processing endpoints whose output reflects parsed content.
- Exploitation / test pattern:
  - Use a harmless local file such as a non-sensitive hostname/version file in a lab or explicitly authorized environment.
- Tools + exact CLI syntax (if mentioned):
  - Core XML feature: DTD external entity with `SYSTEM` URI.
- Common false-positive / WAF / edge-case notes:
  - Parser errors can mimic vulnerability signals; require returned controlled file content.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disable external entity resolution and DTD processing.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 12
