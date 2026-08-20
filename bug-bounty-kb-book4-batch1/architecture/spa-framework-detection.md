# SPA Framework Detection

- What it is: Single-page application frameworks such as React, Vue, Angular, and Ember create stateful client applications with reusable components.
- Where to look / how to identify it:
  - Inspect source bundles, DOM markers, network patterns, package metadata, and framework-specific globals.
- Exploitation / test pattern:
  - Add the framework and version evidence to the recon map for dependency and client-side testing.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Sources/Network/Console.
- Common false-positive / WAF / edge-case notes:
  - Framework detection may be approximate when bundles are minified or customized.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep frameworks patched and avoid unsafe escape hatches around default output protections.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
