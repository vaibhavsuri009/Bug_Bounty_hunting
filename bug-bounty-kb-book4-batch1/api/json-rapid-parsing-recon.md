# JSON Rapid Parsing for Recon

- What it is: JSON is the dominant lightweight format for client/server API communication and often reveals objects, identifiers, roles, and nested relationships.
- Where to look / how to identify it:
  - Inspect API responses for keys that identify resources, authorization state, user roles, integration names, and hidden metadata.
- Exploitation / test pattern:
  - Pretty-print responses and add important fields to the recon map.
- Tools + exact CLI syntax (if mentioned):
  - Browser DevTools Preview/Response; JSON formatter/editor.
- Common false-positive / WAF / edge-case notes:
  - Returned metadata may be intentional; classify sensitivity before treating it as a finding.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Return only fields required by the client and perform field-level authorization where needed.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
