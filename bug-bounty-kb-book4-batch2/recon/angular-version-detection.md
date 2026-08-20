# Angular Version Detection

- What it is: Angular applications expose different runtime markers depending on generation.
- Where to look / how to identify it:
  - Older Angular can expose `angular.version`; newer Angular can expose root elements with an `ng-version` attribute.
- Exploitation / test pattern:
  - Use root-element attributes to identify the running version when the global object is absent.
- Tools + exact CLI syntax (if mentioned):
  - `getAllAngularRootElements()[0].attributes['ng-version']`
- Common false-positive / WAF / edge-case notes:
  - Build tooling may remove some debug helpers in production.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep Angular patched and disable development/debug artifacts in production.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
