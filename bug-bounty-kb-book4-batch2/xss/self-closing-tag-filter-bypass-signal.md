# Browser Tag Auto-Closure Bypass Signal

- What it is: Browsers repair malformed or unclosed HTML tags, which can undermine simplistic filters that only inspect well-formed tag pairs.
- Where to look / how to identify it:
  - Compare raw submitted markup, sanitized output, and final DOM structure.
- Exploitation / test pattern:
  - Use harmless malformed-tag probes to determine whether browser repair changes meaning.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Elements/View Source.
- Common false-positive / WAF / edge-case notes:
  - Browser repair differs by engine/version and malformed HTML alone is not a vulnerability.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use standards-aware parsers/sanitizers rather than regex-based HTML filtering.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
