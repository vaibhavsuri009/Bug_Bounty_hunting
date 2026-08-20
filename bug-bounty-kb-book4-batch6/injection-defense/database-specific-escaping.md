# Database-Specific Escaping as Secondary Defense

- What it is: Database-specific encoding/escaping can reduce injection risk when a query fragment cannot be parameterized.
- Where to look / how to identify it:
  - Identify unavoidable literal-string construction and use the vendor's official escaping API.
- Exploitation / test pattern:
  - Treat escaping as mitigation, not as the primary security boundary.
- Tools + exact CLI syntax (if mentioned):
  - Examples from source: Oracle ESAPI SQL encoder; MySQL QUOTE/escape functions.
- Common false-positive / WAF / edge-case notes:
  - Incorrect character-set assumptions can make escaping incomplete.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer parameterization; use official context-aware escaping only when necessary.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 31
