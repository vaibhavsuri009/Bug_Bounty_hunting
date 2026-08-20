# Indirect JSON-to-XML XXE Signal

- What it is: Modern JSON/REST APIs may internally convert user input to XML when integrating with legacy SOAP/CRM/enterprise systems.
- Where to look / how to identify it:
  - Look for legacy enterprise integrations, unusual formatting constraints, or downstream systems known to use XML.
- Exploitation / test pattern:
  - Use benign malformed values to detect XML-specific parser errors or transformations.
- Tools + exact CLI syntax (if mentioned):
  - Business/architecture recon plus response analysis.
- Common false-positive / WAF / edge-case notes:
  - Indirect XML use can be difficult to prove without source or error evidence.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate and encode before transformation, and disable external entities in downstream XML parsers.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 12
