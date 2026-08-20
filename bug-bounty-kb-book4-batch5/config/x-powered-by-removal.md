# Remove `X-Powered-By`

- What it is: `X-Powered-By` can expose server/framework technology and versions, simplifying fingerprinting.
- Where to look / how to identify it:
  - Inspect response headers across routes and error pages.
- Exploitation / test pattern:
  - Confirm the header is absent after production hardening.
- Tools + exact CLI syntax (if mentioned):
  - Server/framework configuration.
- Common false-positive / WAF / edge-case notes:
  - Removing banners does not patch vulnerabilities; it only reduces unnecessary disclosure.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disable framework/server technology banners and keep components patched.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
