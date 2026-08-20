# File Compression DoS Risk

- What it is: Malformed media or archive inputs can trigger excessive CPU/memory usage in third-party compression/parsing libraries.
- Where to look / how to identify it:
  - Map upload workflows that invoke FFMPEG, ImageMagick, archive handlers, or document converters.
- Exploitation / test pattern:
  - Test only with vendor-provided harmless regression samples in an isolated lab.
- Tools + exact CLI syntax (if mentioned):
  - Dependency/version inventory plus local resource monitoring.
- Common false-positive / WAF / edge-case notes:
  - Do not upload crash/DoS samples to production bug bounty targets without explicit permission.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Patch parser libraries, sandbox workers, limit file size/complexity, and enforce CPU/memory timeouts.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 14
