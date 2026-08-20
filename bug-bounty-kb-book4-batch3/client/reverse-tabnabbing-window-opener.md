# Reverse Tabnabbing via `window.opener`

- What it is: A newly opened page may receive a reference to the opener and can navigate the original tab if protections are missing.
- Where to look / how to identify it:
  - Identify links or scripts opening untrusted external pages in new tabs.
- Exploitation / test pattern:
  - Use a benign controlled destination to verify whether the opened page can modify the opener location.
- Tools + exact CLI syntax (if mentioned):
  - Browser DevTools; local controlled pages.
- Common false-positive / WAF / edge-case notes:
  - Modern browsers/frameworks may automatically imply `noopener` in some cases.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use `rel='noopener noreferrer'`, explicit `noopener`, and avoid exposing opener references.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 16
