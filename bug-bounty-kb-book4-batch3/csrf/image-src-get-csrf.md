# Image-Source GET CSRF

- What it is: HTML elements that automatically fetch a URL can trigger GET requests without an explicit click.
- Where to look / how to identify it:
  - Look for state-changing GET endpoints and consider whether browser-loaded URL attributes could invoke them.
- Exploitation / test pattern:
  - On an authorized test account, use a harmless state change and confirm whether loading the resource triggers it.
- Tools + exact CLI syntax (if mentioned):
  - Relevant browser behavior: `<img src=...>` performs a GET automatically.
- Common false-positive / WAF / edge-case notes:
  - Browser caching or SameSite cookie settings can change behavior.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Never perform sensitive actions via GET and require CSRF defenses on all state-changing routes.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
