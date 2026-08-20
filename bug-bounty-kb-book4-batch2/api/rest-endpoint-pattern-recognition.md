# REST Endpoint Pattern Recognition

- What it is: REST APIs tend to expose hierarchical resource-oriented endpoints rather than function-oriented routes.
- Where to look / how to identify it:
  - Look for repeated resource paths such as `/users/1234`, `/users/1234/payments`, and nested objects.
- Exploitation / test pattern:
  - Classify endpoints by resource, hierarchy, and HTTP verb before attempting deeper testing.
- Tools + exact CLI syntax (if mentioned):
  - Browser DevTools Network/XHR is enough for initial discovery.
- Common false-positive / WAF / edge-case notes:
  - A REST-like naming scheme is only a clue; confirm by observing multiple requests and stateless authorization.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep endpoint naming consistent and document resource relationships.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 5
