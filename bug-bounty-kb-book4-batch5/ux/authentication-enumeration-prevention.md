# Authentication Enumeration Prevention

- What it is: Different login errors for nonexistent users versus wrong passwords let attackers identify valid accounts.
- Where to look / how to identify it:
  - Compare failed authentication responses for a known test user and a deliberately nonexistent one.
- Exploitation / test pattern:
  - Check body, status, length, and timing for distinguishable signals.
- Tools + exact CLI syntax (if mentioned):
  - Browser/Proxy timing and response comparison.
- Common false-positive / WAF / edge-case notes:
  - Rate limiting alone does not remove enumeration if one request reveals validity.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Return the same generic authentication failure and normalize timing where practical.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 23
