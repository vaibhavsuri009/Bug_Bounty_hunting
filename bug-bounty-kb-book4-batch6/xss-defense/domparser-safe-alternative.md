# DOMParser Safe Alternative

- What it is: `DOMParser.parseFromString` turns text into DOM structure and can create XSS exposure when fed user content.
- Where to look / how to identify it:
  - Review all parser inputs and determine whether structure really needs to be user-controlled.
- Exploitation / test pattern:
  - Construct expected elements directly and allow user input to control text values only.
- Tools + exact CLI syntax (if mentioned):
  - `document.createElement()` and `appendChild()`.
- Common false-positive / WAF / edge-case notes:
  - Parsing inert documents can reduce risk in some contexts but does not make arbitrary user HTML universally safe.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer explicit DOM construction and sanitize structured HTML before parsing.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
