# EmberJS Detection

- What it is: EmberJS can expose distinctive global and DOM markers that reveal framework usage and version.
- Where to look / how to identify it:
  - Check for the global `Ember` object and DOM IDs such as `ember1` inside an `ember-application` element.
- Exploitation / test pattern:
  - Read the framework version when available and add it to dependency notes.
- Tools + exact CLI syntax (if mentioned):
  - `console.log(Ember.VERSION)`
- Common false-positive / WAF / edge-case notes:
  - Production builds may hide or alter some markers.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep Ember updated and avoid exposing unnecessary framework/debug metadata.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
