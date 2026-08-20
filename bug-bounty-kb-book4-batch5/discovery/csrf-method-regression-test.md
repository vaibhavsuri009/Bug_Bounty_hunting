# CSRF HTTP-Method Regression Test

- What it is: A state-changing endpoint fixed by changing from GET to POST can be protected with a test asserting only the intended method remains accepted.
- Where to look / how to identify it:
  - Use a test endpoint or OPTIONS response to verify allowed verbs.
- Exploitation / test pattern:
  - Fail the test if GET reappears or multiple unintended verbs become accepted.
- Tools + exact CLI syntax (if mentioned):
  - Automated HTTP test framework.
- Common false-positive / WAF / edge-case notes:
  - Method checks alone do not prove CSRF protection; tokens/SameSite may still be required.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Test both allowed methods and complete anti-CSRF behavior.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 26
