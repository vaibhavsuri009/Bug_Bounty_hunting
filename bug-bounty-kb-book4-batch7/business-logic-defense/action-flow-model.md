# Statistical Modeling of User Actions

- What it is: Business logic testing should model user actions as well as data values.
- Where to look / how to identify it:
  - Inventory page navigation, AJAX calls, buttons, links, forms, modals, WebSockets, RTC, and direct JavaScript actions.
- Exploitation / test pattern:
  - Represent possible action sequences programmatically for automated scenario generation.
- Tools + exact CLI syntax (if mentioned):
  - Analytics + model file.
- Common false-positive / WAF / edge-case notes:
  - Recorded production flows may omit malicious or extremely rare sequences.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Add security abuse sequences beside normal user paths.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 36
