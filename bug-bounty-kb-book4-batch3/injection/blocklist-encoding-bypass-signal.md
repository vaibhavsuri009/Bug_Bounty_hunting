# Injection Blocklist Encoding Bypass Signal

- What it is: Plain-text blocklists can miss encoded representations that are later decoded by the target interpreter.
- Where to look / how to identify it:
  - Review custom filters for exact keyword matching before downstream decoding.
- Exploitation / test pattern:
  - Use benign encoded tokens to verify inconsistent normalization rather than executing harmful commands.
- Tools + exact CLI syntax (if mentioned):
  - Browser `btoa()`/`atob()` or local encoding tools.
- Common false-positive / WAF / edge-case notes:
  - Encoding acceptance alone does not prove command execution.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Normalize once, validate canonical input, and prefer allowlists/parameterized APIs.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
