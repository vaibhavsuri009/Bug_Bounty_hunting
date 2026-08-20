# Malformed Tag Parser Repair

- What it is: Browsers may repair malformed quotes and tag syntax into executable DOM structures after a weak filter has approved them.
- Where to look / how to identify it:
  - Inspect whether malformed HTML changes between network/source representation and the rendered DOM.
- Exploitation / test pattern:
  - Use harmless malformed markup to study parser behavior before attempting any script proof.
- Tools + exact CLI syntax (if mentioned):
  - View Source versus DevTools Elements comparison.
- Common false-positive / WAF / edge-case notes:
  - Results are browser-specific and can change between versions.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use a proven HTML sanitizer and avoid regex-only parsing.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
