# External JavaScript Script Inventory

- What it is: Third-party JavaScript dependencies can be enumerated from script tags already loaded into the DOM.
- Where to look / how to identify it:
  - Query all `script` elements and record non-empty `src` values.
- Exploitation / test pattern:
  - Use the resulting URLs to identify libraries, analytics, payments, and other integrations.
- Tools + exact CLI syntax (if mentioned):
  - `document.querySelectorAll('script')` and inspect each `script.src`.
- Common false-positive / WAF / edge-case notes:
  - Bundled code may hide dependencies inside one local file.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Minimize third-party scripts and apply dependency monitoring/SRI where practical.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
