# XSS Source Inventory

- What it is: Common XSS sources include URL data, location fields, browser storage, referrer data, history state, and IndexedDB.
- Where to look / how to identify it:
  - Search client code for reads from URL/location/storage/referrer/window APIs.
- Exploitation / test pattern:
  - Trace each source forward to determine whether it reaches a dangerous sink.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Sources search.
- Common false-positive / WAF / edge-case notes:
  - Untrusted sources are normal; exploitability depends on downstream handling.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate and encode all untrusted client-side data before DOM insertion or execution.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
