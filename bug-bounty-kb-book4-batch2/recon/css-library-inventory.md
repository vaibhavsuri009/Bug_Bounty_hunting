# CSS Library Inventory

- What it is: Stylesheet links can reveal UI libraries, versions, and component frameworks in use.
- Where to look / how to identify it:
  - Enumerate `link` elements whose `rel` value is `stylesheet` and inspect their hrefs.
- Exploitation / test pattern:
  - Record recognizable framework names and versions for dependency mapping.
- Tools + exact CLI syntax (if mentioned):
  - `document.querySelectorAll('link')` plus `link.rel === 'stylesheet'`.
- Common false-positive / WAF / edge-case notes:
  - Renamed/minified local files can obscure the underlying framework.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep CSS/UI libraries current and remove unused dependencies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
