# Vue Version Detection

- What it is: Vue may expose a `Vue` global and configuration properties useful for recon.
- Where to look / how to identify it:
  - Check the browser console for `Vue`, version data, and development-tool configuration.
- Exploitation / test pattern:
  - Record the discovered version and whether development tooling appears enabled.
- Tools + exact CLI syntax (if mentioned):
  - `console.log(Vue.version)`
- Common false-positive / WAF / edge-case notes:
  - Production builds may disable or remove debug visibility.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disable unnecessary dev tooling in production and keep Vue updated.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
