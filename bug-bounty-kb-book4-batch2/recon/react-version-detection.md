# React Version Detection

- What it is: React may expose a global object or JSX-related artifacts that identify the framework.
- Where to look / how to identify it:
  - Check for the `React` global, React-specific development artifacts, or JSX references.
- Exploitation / test pattern:
  - Record the version only when the evidence is direct.
- Tools + exact CLI syntax (if mentioned):
  - `console.log(React.version)`
- Common false-positive / WAF / edge-case notes:
  - Modern bundlers may not expose the global object.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep React dependencies current and avoid unsafe rendering escape hatches.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
