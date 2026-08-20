# `target=_blank` Tabnabbing Signal

- What it is: Links using `target='_blank'` can create an opener relationship that may permit reverse tabnabbing on affected browser patterns.
- Where to look / how to identify it:
  - Search user-generated/external links that open new tabs.
- Exploitation / test pattern:
  - Verify opener availability only with a harmless controlled external page.
- Tools + exact CLI syntax (if mentioned):
  - HTML/source inspection plus browser console.
- Common false-positive / WAF / edge-case notes:
  - Browser defaults have improved; behavior varies by browser/version.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Add `rel='noopener noreferrer'` to untrusted external new-tab links.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 16
